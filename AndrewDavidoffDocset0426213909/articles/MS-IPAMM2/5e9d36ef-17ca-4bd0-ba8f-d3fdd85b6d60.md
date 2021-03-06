<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.100 GetSchemaConversionInfo</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation is used to check whether a conversion of the
IPAM data store schema is required. This check is performed before the IPAM
system update. </p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetSchemaConversionInfo&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetSchemaConversionInfo&quot; message=&quot;ipam:IIpamServer_GetSchemaConversionInfo_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetSchemaConversionInfoResponse&quot; message=&quot;ipam:IIpamServer_GetSchemaConversionInfo_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt; 
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetSchemaConversionInfo_InputMessage request message, the server
performs the following processing steps. Upon successful completion of these
steps, the server MUST respond with the
IIpamServer_GetSchemaConversionInfo_OutputMessage message. In the event of a
failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP
fault</a> MUST be sent to the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>Get the current
IPAM data store version and the current OS version and the schema version to
which IPAM can be upgraded to by reading the properties <b>ADM_IPAMSchemaVersion</b>,
<b>ADM_IPAMServerVersion</b>, and <b>ADM_IPAMTargetSchemaVersion</b>
respectively.</p>

</li><li><p><span> </span>Assign these to
GetSchemaConversionInfoResponse.configuredVersion,
GetSchemaConversionInfoResponse.installedVersion, and
GetSchemaConversionInfoResponse.nextVersion respectively.</p>

</li><li><p><span> </span>If
GetSchemaConversionInfoResponse.configuredVersion is not the same as
GetSchemaConversionInfoResponse.installedVersion then conversion of IPAM data
schema would be required. Set
GetSchemaConversionInfoResponse.GetSchemaConversionInfoResult to true. Else,
set it to false.</p>

<div><pre>  
</pre></div>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>