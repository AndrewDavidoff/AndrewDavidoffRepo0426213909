<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.11 CreateIPAddressFromDnsResourceRecords</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation creates IP addresses from DNS resource
records and also update the IPAM data store accordingly.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;CreateIPAddressFromDnsResourceRecords&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/CreateIPAddressFromDnsResourceRecords&quot; message=&quot;ipam:IIpamServer_CreateIPAddressFromDnsResourceRecords_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/CreateIPAddressFromDnsResourceRecordsResponse&quot; message=&quot;ipam:IIpamServer_CreateIPAddressFromDnsResourceRecords_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>The protocol client sends an
IIpamServer_CreateIPAddressFromDnsResourceRecords_InputMessage request. The
server then performs the following processing steps. When the operation
completes successfully, the protocol server MUST respond with the
IIpamServer_CreateIPAddressFromDnsResourceRecords_OutputMessage response. In
the event of a failure, an appropriate SOAP fault MUST be sent to the client as
specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>If any of the
following conditions is not met, an appropriate SOAP fault MUST be generated.</p>

<ul><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.records
is not NULL.</p>

</li><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.records.Count
is not equal to 0.</p>

</li><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.dnsZoneId
is not equal to 0.</p>

</li><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.addressSpaceId
is not equal to 0.</p>

</li><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.managedByValueId
is not equal to 0.</p>

</li><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.serviceInstanceValueId
is not equal to 0.</p>

</li><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.deviceTypeValueId
is not equal to 0.</p>

</li><li><p><span><span> </span></span>CreateIPAddressFromDnsResourceRecords.ipAddressStateValueId
is not equal to 0.</p>

</li></ul></li><li><p><span> </span>For each element
in CreateIPAddressFromDnsResourceRecords.records, call the
GetDnsResourceRecordsbyRecordId procedure of <b>ADM_DnsResourceRecordTable</b>
with CreateIPAddressFromDnsResourceRecords.records.m_Item1 as a parameter. Add
the output in temporary variable temp_Var.recordCollection. Iterate through
each record returned in temp_Var.recordCollection and remove it from
temp_Var.recordCollection if the RecordType of the record is not equal to A or
AAAA.</p>

</li><li><p><span> </span>Group the
temp_Var.recordCollection based on their associated IP address. This creates a
collection of DNS resource records grouped by their associated IP addresses.</p>

</li><li><p><span> </span>For each group
of resource records, temp_Var.records from temp_var.recordCollection, assign
the associated IP address to temp_Var.IPAddressValue and do the following:</p>

<ol><li><p><span> 
</span>Enumerate the row in <b>ADM_IPAddressTable</b> where IPAddress,
ManagedByValue and ManagedByEntityValue value is the same as
temp_Var.IPAddressValue, CreateIPAddressFromDnsResourceRecords.managedByValueId
and CreateIPAddressFromDnsResourceRecords.serviceInstanceValueId, respectively.</p>

</li><li><p><span> 
</span>If a record is returned for the above query, call GetIPAddressFromTable
from <b>ADM_IPAddressTable</b>. Store the result in temp_Var.IPAddress.</p>

</li><li><p><span> 
</span>If no record is returned for the query, create a temp_Var.IPAddress of
type IpamIPAddres and set the following:</p>

<ol><li><p><span> </span>temp_Var.IPAddress.Address
equals temp_Var.IPAddressValue</p>

</li><li><p><span> </span>temp_Var.IPAddress.AddressSpaceRecordId
equals CreateIPAddressFromDnsResourceRecords.addressSpaceId</p>

</li><li><p><span> </span>temp_Var.IPAddress.CreatedFromDnsResourceRecord
equals TRUE</p>

</li><li><p><span> </span>If
CreateIPAddressFromDnsResourceRecords.addressSpaceId.Value ! equals
ProviderAddressSpace.DefaultProviderAddressSpaceRecordId then set
temp_Var.IPAddress.VirtualizationType equals IPVirtualizationType.Fabric</p>

</li><li><p><span> </span>Use
SetCustomFieldValues of <b>ADM_CustomFieldValuesAssociationTable</b> to
associate CreateIPAddressFromDnsResourceRecords.managedByValueId and
CreateIPAddressFromDnsResourceRecords.serviceInstanceValueId with custom field
with identifiers <b>ADM_ManagedByCustomFieldId</b> and <b>ADM_ManagedByEntityCustomFieldId</b>
respectively for temp_Var.IPAddress.</p>

</li><li><p><span> </span>Validate the
temp_Var.IPAddress using the processing rules listed under
ValidateIpamIPAddress, passing temp_Var.IPAddress as Param_address. If any of
the processing rules are not met, an appropriate SOAP fault (as specified in
section 2.2.2.1) MUST be returned.</p>

</li><li><p><span> </span>Add a new record
in <b>ADM_IPAddressTable</b> using the details of temp_Var.IPAddress.</p>

</li></ol></li><li><p><span> 
</span>Use SetCustomFieldValues of <b>ADM_CustomFieldValuesAssociationTable</b>
to associate CreateIPAddressFromDnsResourceRecords. deviceTypeValueId and
CreateIPAddressFromDnsResourceRecords. ipAddressStateValueId with custom field
with appropriate identifiers for temp_Var.IPAddress.</p>

</li><li><p><span> 
</span>Perform the address update as specified under the
UpdateIpamIPAddressDelegate operation.</p>

</li><li><p><span> 
</span>For each resource record, temp_Var.record in temp_Var.records, do the
following:</p>

<ol><li><p><span> </span>If
temp_Var.IPAddress.RecordId is NULL or temp_Var.record.AssociatedIPAddressId is
not NULL and not the same as temp_Var.IPAddress.RecordId, add temp_Var.record
to temp_Var.alreadyMappedRecords list.</p>

</li><li><p><span> </span>Otherwise, set
temp_Var.record.AssociatedIPAddressId to temp_Var.IPAddress.RecordId and add
temp_Var.record to temp_Var.toMapRecords list.</p>

</li></ol></li><li><p><span> 
</span>Update all records in temp_Var.toMapRecords list in <b>ADM_DNSResourceRecordTable</b>.</p>

</li></ol></li></ol>
 </div>
 </div>
 </div>
 </body>
</html>