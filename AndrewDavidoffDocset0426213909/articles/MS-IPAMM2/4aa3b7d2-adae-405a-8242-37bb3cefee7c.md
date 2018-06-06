<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.9.1.2 IIpamServer_CreateDNSHostRecord_OutputMessage</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The IIpamServer_CreateDNSHostRecord_OutputMessage message is
sent in reply to the request that is initiated by the
IIpamServer_CreateDNSHostRecord_InputMessage message.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:message name=&quot;IIpamServer_CreateDNSHostRecord_OutputMessage&quot;&gt;
   &lt;wsdl:part name=&quot;parameters&quot; element=&quot;ipam:CreateDNSHostRecordResponse&quot; /&gt;
 &lt;/wsdl:message&gt;
</pre></div>
</dd></dl>

<p>The <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_c1358651-96c1-4ce0-8e1f-b0b7a94145e3">SOAP
action</a> value of the message MUST be as follows:</p>

<dl>
<dd>
<div><pre> http://Microsoft.Windows.Ipam/IIpamServer/CreateDNSHostRecordResponse
</pre></div>
</dd></dl>

<p>The body of the <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_96185df3-4677-478c-b239-f72fcf514c59">SOAP message</a> MUST contain
the CreateDNSHostRecordResponse element, specified in section <a href="0d7f5436-8442-4392-b8f3-4b0eea920ee7.md">3.3.4.9.2.2</a>.</p>


 </div>
 </div>
 </div>
 </body>
</html>