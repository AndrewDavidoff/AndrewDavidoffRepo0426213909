<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.155 UpdateUserRole</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation is used to update an ipam:UserRole in the
IPAM data store.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;UpdateUserRole&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/UpdateUserRole&quot; message=&quot;ipam:IIpamServer_UpdateUserRole_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/UpdateUserRoleResponse&quot; message=&quot;ipam:IIpamServer_UpdateUserRole_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>The protocol client sends an
IIpamServer_UpdateUserRole_InputMessage request. The server then performs the
following processing steps. When the operation completes successfully, the
protocol server MUST respond with the IIpamServer_UpdateUserRole_OutputMessage response.
In the event of a failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a> MUST be sent to
the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>Call method <b>ValidateUserRole</b>
to validate <b>UpdateUserRole.role</b>.</p>

</li><li><p><span> </span>If <b>UpdateUserRole.role</b>
is NULL or if <b>UpdateUserRole.role.IsBuiltinRole</b> is true then a SOAP
fault MUST be generated as specified in section 2.2.2.1.</p>

</li><li><p><span> </span><b>UpdateUserRole.role.UserRoleID</b>
is used to identify the row in ADM_RoleDefinitionTable to be updated. After the
updation is done, the number of rows modified are returned in the response
message to indicate if the update was successful or not.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>