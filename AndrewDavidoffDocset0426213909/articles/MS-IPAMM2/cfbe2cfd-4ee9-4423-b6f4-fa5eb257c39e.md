<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.99 GetResourceRecords</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation retrieves the DNS resource record objects
corresponding to the given record IDs.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetResourceRecords&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetResourceRecords&quot; message=&quot;ipam:IIpamServer_GetResourceRecords_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetResourceRecordsResponse&quot; message=&quot;ipam:IIpamServer_GetResourceRecords_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetResourceRecords_InputMessage request message, the server
performs the following processing steps. Upon successful completion of these
steps, the server MUST respond with the
IIpamServer_GetResourceRecords_OutputMessage message. In the event of a
failure, an appropriate SOAP fault MUST be sent to the client as specified in
section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>If GetResourceRecords.BaseDnsZone
is NULL, GetResourceRecords.BaseDnsZone.recordId is 0, or
GetResourceRecords.resourceRecordCollection is NULL, an appropriate SOAP fault
MUST be generated.</p>

</li><li><p><span> </span>Call the
GetDNSResourceRecordById procedure of <b>ADM_DnsResourceRecordTable</b> with
the <b>m_Item1</b> fields of the elements in
GetResourceRecords.resourceRecordCollection as input parameters and put the
output in GetResourceRecordsResponse.GetResourceRecordsResult.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>