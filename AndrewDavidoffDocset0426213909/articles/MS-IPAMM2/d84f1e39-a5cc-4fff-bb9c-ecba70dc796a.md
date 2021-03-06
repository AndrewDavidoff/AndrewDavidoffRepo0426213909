<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.69 GetCommonPropertyValue</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation can be used to retrieve the global property
being requested.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetCommonPropertyValue&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetCommonPropertyValue&quot; message=&quot;ipam:IIpamServer_GetCommonPropertyValue_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetCommonPropertyValueResponse&quot; message=&quot;ipam:IIpamServer_GetCommonPropertyValue_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetCommonPropertyValue_InputMessage request message, the server
performs the following processing steps. Upon successful completion of the
steps specified below, the server MUST respond with the
IIpamServer_GetCommonPropertyValue_OutputMessage message. In the event of a
failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP
fault</a> MUST be sent to the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>Retrieve the
value corresponding to the property specified as <b>GetCommonPropertyValue.property</b>
from <b>ADM_CommonProperties</b> and assign it to <b>GetCommonPropertyValueResponse.GetCommonPropertyValueResult</b>.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>