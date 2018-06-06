<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.19.4.7 SetSubTaskStatus</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation MUST NOT be invoked by the management client
and MUST be ignored by the server. The management server calls SetSubTaskStatus
of the management client interface when it needs to communicate the status of a
subtask.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation msc:isInitiating=&quot;true&quot; msc:isTerminating=&quot;false&quot; name=&quot;SetSubTaskStatus&quot;&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamOperationWithProgress/SetSubTaskStatus&quot; message=&quot;ipam:IIpamOperationWithProgress_SetSubTaskStatus_OutputCallbackMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>


 </div>
 </div>
 </div>
 </body>
</html>