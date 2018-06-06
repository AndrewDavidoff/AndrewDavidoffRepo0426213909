<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.19.4.4.1.12 CreateServerPolicyDelegate</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This is the processing done when the
IpamOperationWithProgressParameter.OperationId is
AdminOperationId.CreateDhcpServerPolicy. The IpamOperationWithProgressParameter
instance in this case MUST be of type CreateDhcpServerPolicyParameters. </p>

<p>This operation is used to create a new server-level DHCP
policy. The following are the steps involved. In these steps, any time a fault
is generated, the SetOverallStatus SHOULD be called with the fault details.</p>

<ol><li><p><span> </span>If
IpamOperationWithProgressParameter is NULL or not of type
CreateDhcpServerPolicyParameters, generate an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a> (as specified in
section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>).
Project IpamOperationWithProgressParameter in a local variable as
CreateDhcpServerPolicyParameters.</p>

</li><li><p><span> </span>If
CreateDhcpServerPolicyParameters.Policy is NULL or CreateDhcpServerPolicyParameters.ServerList
is NULL or CreateDhcpServerPolicyParameters.ServerList.Count = 0, generate an
appropriate SOAP fault (as specified in section 2.2.2.1).</p>

</li><li><p><span> </span>Validate the
CreateDhcpServerPolicyParameters.Policy using the processing rules listed under
ValidateDhcpPolicy by passing CreateDhcpServerPolicyParameters.Policy as
Param_policy. If any of the processing rules are not met, an appropriate SOAP
fault (as specified in section 2.2.2.1) MUST be returned.</p>

</li><li><p><span> </span>For each server
in the CreateDhcpServerPolicyParameters.ServerList, put the server object in a
local variable dhcpServer and do the following steps for each server:</p>

</li><li><p><span> </span>Create a new row
in the table <b>ADM_DhcpPolicyTable</b>, assigning a new policyId to this row.
Populate this row as follows:</p>

<ul><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.Server</b>
= dhcpServer</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.Scope</b>
is NULL</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.PolicyName</b>
= CreateDhcpServerPolicyParameters.Policy.PolicyName</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.PolicyDescription</b>
= CreateDhcpServerPolicyParameters.Policy.PolicyDescription</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.ProcessingOrder</b>
= CreateDhcpServerPolicyParameters.Policy.ProcessingOrder</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.State</b>
= CreateDhcpServerPolicyParameters.Policy.State</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.LeaseDurationType</b>
= CreateDhcpServerPolicyParameters.Policy.LeaseDurationType</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.LeaseDuration</b>
= CreateDhcpServerPolicyParameters.Policy.LeaseDuration</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.DnsUpdateType</b>
= CreateDhcpServerPolicyParameters.Policy.DnsUpdateType</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.DiscardDnsRecordOnLeaseDeletionStatus</b>
= CreateDhcpServerPolicyParameters.Policy.DiscardDnsRecordOnLeaseDeletionStatus</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.DnsNameProtectionStatus</b>
= CreateDhcpServerPolicyParameters.Policy.DnsNameProtectionStatus</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.DnsNotRequestingClientUpdateType</b>
= CreateDhcpServerPolicyParameters.Policy.DnsNotRequestingClientUpdateType</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.DnsDisableDynamicPtrUpdate</b>
= CreateDhcpServerPolicyParameters.Policy.DnsDisableDynamicPtrUpdate</p>

</li><li><p><span><span> </span></span><b>ADM_DhcpPolicyTable.DnsSuffix</b>
= CreateDhcpServerPolicyParameters.Policy.DnsSuffix</p>

</li></ul></li><li><p><span> </span>Create a new row
in <b>ADM_DhcpOptionsTable</b> with the details set from
CreateDhcpServerPolicyParameters.Policy and the PolicyId set to the policy ID
of the configured policy.</p>

</li><li><p><span> </span>Call
SetOverallStatus with Success and 100 percent completion.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>