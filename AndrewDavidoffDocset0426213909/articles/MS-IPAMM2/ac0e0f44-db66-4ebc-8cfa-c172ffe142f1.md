<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.97 GetRangeUtilization</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation is used to retrieve the utilization data for
a specified address range.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetRangeUtilization&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetRangeUtilization&quot; message=&quot;ipam:IIpamServer_GetRangeUtilization_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetRangeUtilizationResponse&quot; message=&quot;ipam:IIpamServer_GetRangeUtilization_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetRangeUtilization_InputMessage request message, the server
performs the following processing steps. Upon successful completion of these
steps, the server MUST respond with the
IIpamServer_GetRangeUtilization_OutputMessage message. In the event of a
failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP
fault</a> MUST be sent to the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>Get the address
range for which the address utilization is requested by calling the <b>GetIPRangeFromTable</b>
procedure of <b>ADM_IPRangeTable</b> with the <i>Param_id</i> input parameter
set to <b>GetRangeUtilization.ipRangeRecordId</b> and the <i>Param_addressfamily</i>
input parameter set to <b>GetRangeUtilization.addressFamily</b>. Store the <b>result</b>
to requestedRange.</p>

</li><li><p><span> </span>If the
requestedRange is NULL, an appropriate SOAP fault MUST be returned.</p>

</li><li><p><span> </span>Initialize <b>GetRangeUtilizationResponse.GetRangeUtilizationResult</b>
to IPCumulativeUtilization.</p>

</li><li><p><span> </span>If the <b>GetRangeUtilization.addressFamily</b>
is InterNetworkV6, the <b>GetRangeUtilization. requestedIPUtilizationType</b>
MUST be IPUtilizationType.Current. Otherwise an appropriate SOAP fault MUST be
returned.</p>

</li><li><p><span> </span>If <b>GetRangeUtilization.requestedIPUtilizationType</b>
is <b>IPUtilizationType.Current</b></p>

<ol><li><p><span> 
</span>Set <b>GetRangeUtilizationResponse.GetRangeUtilizationResult.</b> <b>IPUtilizationType</b>
to <b>IPUtilizationType.Current</b>.</p>

</li><li><p><span> 
</span>Add <b>requestedRange.UtilizationStatistics</b> to <b>GetRangeUtilizationResponse.GetRangeUtilizationResult.IPUtilization</b>.</p>

</li><li><p><span> 
</span>Return the <b>GetRangeUtilizationResponse</b> element as a part of the
output message.</p>

</li></ol></li><li><p><span> </span>The <b>GetRangeUtilization.startDate</b>
and <b>GetRangeUtilization.endDate</b> MUST be specified according to the
IPUtilizationType requested. For example, if <b>GetRangeUtilization.requestedIPUtilizationType</b>
is IPUtilizationType.OneMonth, the <b>GetRangeUtilization.startDate</b> and <b>GetRangeUtilization.endDate</b>
MUST be one month apart.</p>

</li><li><p><span> </span>Compute the
ManagedBy of the requestedRange to be the custom field value whose custom field
record identifier is <b>ADM_ManagedByCustomFieldId</b>.</p>

</li><li><p><span> </span>Compute the
ManagedByEntity of the requestedRange to be the custom field value whose custom
field record identifier is <b>ADM_ManagedByEntityCustomFieldId</b>.</p>

</li><li><p><span> </span>Enumerate the
rows in <b>ADM_IPv4AddressUtilizationTable</b> having the following condition
ordered by Timestamp in ascending order.</p>

<ul><li><p><span><span> </span></span><b>StartIPAddress</b>
is equal to requestedRange.StartIPAddress.</p>

</li><li><p><span><span> </span></span><b>EndIPAddress</b>
is equal to requestedRange.EndIPAddress.</p>

</li><li><p><span><span> </span></span><b>PrefixLength</b>
is equal to requestedRange.PrefixLength.</p>

</li><li><p><span><span> </span></span><b>ManagedBy</b>
is ManagedBy value of requestedRange.</p>

</li><li><p><span><span> </span></span><b>ManagedByValue</b>
is ManagedByEntity value of requestedRange.</p>

</li><li><p><span><span> </span></span><b>Timestamp</b>
is greater than or equal to GetRangeUtilization.startDate and TimeStamp is
lesser than or equal to GetRangeUtilization.endDate.</p>

</li></ul></li><li><p><span> </span>If there are no rows meeting
the previous criteria, return the current utilization as the <b>GetRangeUtilizationResponse.GetRangeUtilizationResult</b>
by following step 5.</p>

</li><li><p><span> </span>Divide the duration between <b>GetRangeUtilization.startDate</b>
and <b>GetRangeUtilization.endDate</b> into 12 durations. For each duration,
sum the AddressUtilizationData of the rows and add the IPUtilization to <b>GetRangeUtilizationResponse.GetRangeUtilizationResult.IpUtilization</b>.
There can be multiple rows that match the conditions listed in step 9. This
could mean the range is configured on multiple servers for dynamic address
assignment and they are configured with exclusion ranges so that the addresses
assigned by either of the servers do not overlap though they might belong to
the same range. The other possibility is that for the given duration, the
utilization data for the range was collected multiple times. The utilization
data under this circumstance can be averaged in an implementation-specific manner
to give the utilization for an address range, representative of a time period.</p>

</li><li><p><span> </span>Set the <b>GetRangeUtilizationResponse.GetRangeUtilizationResult.IPUtilizationType</b>
to  <b>GetRangeUtilization.requestedIPUtilizationType</b>.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>