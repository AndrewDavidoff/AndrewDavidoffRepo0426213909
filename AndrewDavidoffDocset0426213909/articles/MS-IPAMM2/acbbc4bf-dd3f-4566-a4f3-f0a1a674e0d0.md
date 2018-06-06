<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.17 DBGetDhcpServerFromServerInfoRecordId</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation can be used to retrieve the DhcpServer
instance for the specified ServerInfo RecordId.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;DBGetDhcpServerFromServerInfoRecordId&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/DBGetDhcpServerFromServerInfoRecordId&quot; message=&quot;ipam:IIpamServer_DBGetDhcpServerFromServerInfoRecordId_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/DBGetDhcpServerFromServerInfoRecordIdResponse&quot; message=&quot;ipam:IIpamServer_DBGetDhcpServerFromServerInfoRecordId_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_DBGetDhcpServerFromServerInfoRecordId_InputMessage request message,
the server performs the following processing steps. Upon successful completion
of the steps specified below, the server MUST respond with the
IIpamServer_DBGetDhcpServerFromServerInfoRecordId_OutputMessage message. In the
event of a failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a> MUST be sent to
the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>Validate <b>DBGetDhcpServerFromServerInfoRecordId.serverInfoRecordId</b>
is not 0 and <b>DBGetDhcpServerFromServerInfoRecordId.addressFamily</b> is
either InterNetwork or InterNetworkV6. If either of the conditions is not met,
an appropriate SOAP fault MUST be returned.</p>

</li><li><p><span> </span>Look up in the <b>ADM_ServerRolesTable</b>
the row with ServerRecordID equal to <b>DBGetDhcpServerFromServerInfoRecordId.serverInfoRecordId</b>
and <b>ServerRoleDetails.ServerRoleFlag</b> equal to <b>ServerRoleType.Dhcp</b>.</p>

</li><li><p><span> </span>If the row is
found, look up <b>ADM_DHCPServersTable</b> for the row that has the
ServerRoleRecordId to be the <b>RecordId</b> of the row found in
ADM_ServerRolesTable. The DBGetDhcpServerFromServerInfoRecordId.addressFamily
is used to select the simple table within the <b>ADM_DHCPServersTable</b>
against which the lookup is being done.</p>

</li><li><p><span> </span>Use the RecordId
of the row as <i>Param_Id</i> and <b>DBGetDhcpServerFromServerInfoRecordId.addressFamily</b>
as <i>Param_addressfamily</i> and call the procedure GetDHCPServerFromTable in <b>ADM_DHCPServersTable</b>.
Assign the Result_server to <b>DBGetDhcpServerFromServerInfoRecordIdResponse.
DBGetDhcpServerFromServerInfoRecordIdResult</b>.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>