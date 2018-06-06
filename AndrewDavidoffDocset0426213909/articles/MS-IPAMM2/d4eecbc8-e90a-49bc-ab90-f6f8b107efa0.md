<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.81 GetIpamVersion</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation can be used to retrieve the IPAM server
version.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetIpamVersion&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetIpamVersion&quot; message=&quot;ipam:IIpamServer_GetIpamVersion_InputMessage&quot; /&gt;      &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetIpamVersionResponse&quot; message=&quot;ipam:IIpamServer_GetIpamVersion_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the IIpamServer_GetIpamVersion_InputMessage
request message, the server performs the following processing steps. Upon
successful completion of the steps specified below, the server MUST respond
with the IIpamServer_GetIpamVersion_OutputMessage message. In the event of a
failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP
fault</a> MUST be sent to the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<p>Set GetIpamVersionResponse.GetIpamVersionResult to the
version of the IPAM server<a id="Appendix_A_Target_80"></a><a href="3b257e05-6300-4286-a090-0f9949d290bf.md#Appendix_A_80" aria-label="Product behavior note 80">&lt;80&gt;</a></p>


 </div>
 </div>
 </div>
 </body>
</html>