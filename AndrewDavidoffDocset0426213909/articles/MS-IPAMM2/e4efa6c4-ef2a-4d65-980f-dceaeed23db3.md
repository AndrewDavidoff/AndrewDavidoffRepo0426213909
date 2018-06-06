<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.19.6.1 User Authorization</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This section lists the user authorization requirements for
the various operations defined in this port type. After the user authentication
is complete, the user MUST be authorized for the operation that is being
requested. If the required authorization is not present, the user MUST be
denied access to perform the operation by returning an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a> as specified in
section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<table>
 <thead>
 <tr>
 <th>
 <p>IIpamOperationWithProgress Operation</p>
 </th>
 <th>
 <p>ADM States to be checked</p>
 </th>
 </tr>
 </thead>
 <tr>
 <td>
 <p>InitializeOperationParameters</p>
 </td>
 <td>
 <p>Allowed for all users</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>StartOperationWithCallback</p>
 </td>
 <td>
 <p>Permission determined as mentioned below</p>
 </td>
 </tr>
</table>

<p>The following steps determine if the user is authorized to
perform the operation. This check is done after the steps listed in section <a href="38d575e6-46e1-4de4-8ab2-ab1eb985a101.md">3.1.4.3</a> are complete.</p>

<ol><li><p><span> </span>Determine the
mapping OperationId of the operation with the help of the table listed below.
Call GetOperationById procedure of <b>ADM_AdminOperationsTable</b> by passing
OperationId as <i>Param_operationId</i>. Process the results from the procedure
as follows:</p>

<ul><li><p><span><span> </span></span>Assign
<i>Param_OperationGroupId</i> to OperationGroupId</p>

</li><li><p><span><span> </span></span>Assign
<i>Param_IsAdminRoleOnlyOperation</i> to AdminRoleOnlyOperation</p>

</li><li><p><span><span> </span></span>Assign
<i>Param_IsNonRBACOperation</i> to IsNonRBACOperation</p>

</li><li><p><span><span> </span></span>Assign
<i>Param_IsAccessScopeAgnosticOperation</i> to IsAccessScopeAgnosticOperation</p>

</li><li><p><span><span> </span></span>Assign
<i>Param_NonRBACAdminAccessRequirement</i> to NonRBACAdminAccessRequirement</p>

</li></ul></li><li><p><span> </span>If either
AdminRoleOnlyOperation or IsNonRBACOperation is set to TRUE, then based on the
requirements of the security group mentioned in NonRBACAdminAccessRequirement,
check that <b>ADM_UserAuthorizationData</b> has the appropriate role value set
to TRUE. If the appropriate role value is set to TRUE, the operation is
allowed; otherwise the access to perform operation is denied.</p>

</li><li><p><span> </span> If both
AdminRoleOnlyOperation and IsNonRBACOperation set to FALSE, then based on the
requirements of the security groups mentioned in NonRBACAdminAccessRequirement,
evaluate that <b>ADM_UserAuthorizationData</b> has the appropriate role value
set to TRUE. If the appropriate role value is set to TRUE, the operation is
allowed.</p>

</li><li><p><span> </span>If
IsAccessScopeAgnosticOperation set to FALSE, determine the AccessScope
association of the object by calling the procedure
GetAccessScopeForObjectIdAndType of <b>ADM_AccessScopeAssociationTable</b>
passing the following parameters:</p>

<ol><li><p><span> 
</span><i>Param_objectId</i> is set to the appropriate <b>RecordId.</b></p>

</li><li><p><span> 
</span><i>Param_objectType</i> is set to the appropriate Object Type.</p>

</li><li><p><span> 
</span><i>Param_accessScopeId.</i></p>

</li><li><p><span> 
</span><i>Param_objectInheritanceStatus.</i></p>

</li><li><p><span> 
</span><i>Param_inheritanceId.</i></p>

</li></ol></li><li><p><span> </span>Assign <i>Param_accessScopeI</i>d
to ObjectAccessScopeId, which is a 64 bit signed integer to represent the
AccessScopeId associated to a specific object.</p>

</li><li><p><span> </span>Initialize a
collection UserAccessPolicies of type AccessScopeToUserRoleMapping.</p>

</li><li><p><span> </span>For each entry
in the <b>ADM_UserAuthorizationData</b>.MappingPolicyId collection, call
procedure GetPolicyMapEntriesForPolicyId by assigning <i>Param_policyId</i>,
value of entry in MappingPolicyIds. Add the entries in Result_policyEntries to
collection UserAccessPolicies.</p>

</li><li><p><span> </span>For each entry
UserAccessPolicy in the UserAccessPolicies, call procedure
GetAllOperationsForRoleById of <b>ADM_RoleOperationMapTable</b> by assigning
UserAccessPolicy.UserRoleId to <i>Param_RoleId</i>.</p>

</li><li><p><span> </span>If
Result_operations collection contains an entry of OperationId, do the
following:</p>

<ol><li><p><span> 
</span>If IsAccessScopeAgnosticOperation set to TRUE, the operation is allowed
for the user.</p>

</li><li><p><span> 
</span>If the UserAccessPolicy.AccessScopeId is same as ObjectAccessScopeId,
the operation is allowed for the user.</p>

</li></ol></li><li><p><span> </span>Operation is not allowed for
the user.</p>

</li></ol><p>The following table specifies the operations and the
corresponding OperationId mapping as mentioned in <b>ADM_AdminOperationsTable</b>.
For operations that operate on multiple objects of the same type (like
DeleteSuperscopes) or  have multiple suboperations, the validations for
operation being allowed is performed on each individual object and each
sub-operation.</p>

<table>
 <thead>
 <tr>
 <th>
 <p>Operation</p>
 </th>
 <th>
 <p>Operation steps</p>
 </th>
 <th>
 <p>Mapping OperationId</p>
 </th>
 <th>
 <p>Object for AccessScope Determination</p>
 </th>
 </tr>
 </thead>
 <tr>
 <td>
 <p>EditDhcpServer</p>
 </td>
 <td>
 <p>UpdateDhcpServerDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditServerProperties</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ApplyServerConfigurationTemplate</p>
 </td>
 <td>
 <p>ApplyDhcpServerConfigurationDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditServerProperties</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CreateDhcpScope</p>
 </td>
 <td>
 <p>CreateDhcpScopeDelegate</p>
 </td>
 <td>
 <p>MsmDhcpCreateScope</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>EditDhcpScope</p>
 </td>
 <td>
 <p>UpdateDhcpScopeDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditScope</p>
 </td>
 <td>
 <p>DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>DeleteDhcpScope</p>
 </td>
 <td>
 <p>DeleteDhcpScopeDelegate</p>
 </td>
 <td>
 <p>MsmDhcpDeleteScope</p>
 </td>
 <td>
 <p> DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ApplyScopeConfigurationTemplate</p>
 </td>
 <td>
 <p>ApplyDhcpScopeConfigurationDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditScope</p>
 </td>
 <td>
 <p> DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>AddScopesToSuperscope</p>
 </td>
 <td>
 <p>AddScopesToSuperscopeDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditSuperscope</p>
 </td>
 <td>
 <p>DhcpSuperscopeV4</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>RemoveScopesfromSuperscope</p>
 </td>
 <td>
 <p>RemoveScopesFromSuperscopeDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditSuperscope</p>
 </td>
 <td>
 <p>DhcpSuperscopeV4</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>RenameSuperscope</p>
 </td>
 <td>
 <p>RenameSuperscopeDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditSuperscope</p>
 </td>
 <td>
 <p>DhcpSuperscopeV4</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>DeleteSuperscopes</p>
 </td>
 <td>
 <p>DeleteSuperscopesDelegate</p>
 </td>
 <td>
 <p>MsmDhcpDeleteSuperscope</p>
 </td>
 <td>
 <p>DhcpSuperscopeV4</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>SetSuperscopeActivationStatus</p>
 </td>
 <td>
 <p>SetSuperscopeActivationStatusDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditSuperscope</p>
 </td>
 <td>
 <p>DhcpSuperscope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CreateDhcpServerPolicy</p>
 </td>
 <td>
 <p>CreateServerPolicyDelegate</p>
 </td>
 <td>
 <p>MsmDhcpCreateServerPolicy</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CreateDhcpScopePolicy</p>
 </td>
 <td>
 <p>CreateScopePolicyDelegate</p>
 </td>
 <td>
 <p>MsmDhcpCreateScopePolicy</p>
 </td>
 <td>
 <p>DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>UpdatePolicy</p>
 </td>
 <td>
 <p>UpdatePolicyDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditScopePolicy/ MsmDhcpEditServerPolicy</p>
 </td>
 <td>
 <p>DhcpScope/DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>DeletePolicy</p>
 </td>
 <td>
 <p>DeletePolicyDelegate</p>
 </td>
 <td>
 <p>MsmDhcpDeleteScopePolicy/ MsmDhcpDeleteServerPolicy</p>
 </td>
 <td>
 <p>DhcpScope/DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>UpdatePolicyProperty</p>
 </td>
 <td>
 <p>UpdatePolicyPropertiesDelegate</p>
 </td>
 <td>
 <p>MsmDhcpDeleteScopePolicy/ MsmDhcpDeleteServerPolicy</p>
 </td>
 <td>
 <p> DhcpScope/DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>MovePolicyProcessingOreder</p>
 </td>
 <td>
 <p>MovePolicyProcessingOrderDelegate</p>
 </td>
 <td>
 <p>MsmDhcpDeleteScopePolicy/ MsmDhcpDeleteServerPolicy</p>
 </td>
 <td>
 <p>DhcpScope/DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CreateDhcpReservation</p>
 </td>
 <td>
 <p>CreateDhcpReservationDelegate</p>
 </td>
 <td>
 <p>MsmDhcpScopeCreateOrEditAddressReservation</p>
 </td>
 <td>
 <p>DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>DeleteDhcpReservation</p>
 </td>
 <td>
 <p>DeleteDhcpReservationDelegate</p>
 </td>
 <td>
 <p>MsmDhcpScopeDeleteAddressReservation</p>
 </td>
 <td>
 <p>DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>DeleteDhcpReservationCollection</p>
 </td>
 <td>
 <p>DeleteDhcpReservationCollectionDelegate</p>
 </td>
 <td>
 <p>MsmDhcpScopeDeleteAddressReservation</p>
 </td>
 <td>
 <p>DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>SetDhcpreservation</p>
 </td>
 <td>
 <p>SetDhcpReservationDelegate</p>
 </td>
 <td>
 <p>MsmDhcpScopeCreateOrEditAddressReservation</p>
 </td>
 <td>
 <p>DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>SetDhcpReservationCollection</p>
 </td>
 <td>
 <p>SetDhcpReservationCollectionDelegate</p>
 </td>
 <td>
 <p>MsmDhcpScopeCreateOrEditAddressReservation</p>
 </td>
 <td>
 <p>DhcpScope</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CreateDhcpFailover</p>
 </td>
 <td>
 <p>CreateDhcpFailoverDelegate</p>
 </td>
 <td>
 <p>MsmDhcpCreateFailover</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>EditDhcpFailover</p>
 </td>
 <td>
 <p>UpdateDhcpFailoverDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditFailover</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>AddDhcpFailoverScopes</p>
 </td>
 <td>
 <p>DhcpFailoverAddScopesDelegate </p>
 </td>
 <td>
 <p>MsmDhcpEditFailover</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>RemoveDhcpFailoverScopes</p>
 </td>
 <td>
 <p>DhcpFailoverRemoveScopesDelegate</p>
 </td>
 <td>
 <p>MsmDhcpEditFailover</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>DeleteDhcpFailover</p>
 </td>
 <td>
 <p>DeleteDhcpFailoverDelegate</p>
 </td>
 <td>
 <p>MsmDhcpDeleteFailover</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ResetConfigSyncStatus</p>
 </td>
 <td>
 <p>ResetConfigSyncStatusDelegate</p>
 </td>
 <td>
 <p>MsmDhcpReplicateOperation</p>
 </td>
 <td>
 <p>AccessScopeAgnostic</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ReplicateScope</p>
 </td>
 <td>
 <p>ReplicateFailoverScopeDelegate</p>
 </td>
 <td>
 <p>MsmDhcpReplicateOperation</p>
 </td>
 <td>
 <p>AccessScopeAgnostic</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ReplicateRelation</p>
 </td>
 <td>
 <p>DoFailoverReplicationDelegate</p>
 </td>
 <td>
 <p>MsmDhcpReplicateOperation</p>
 </td>
 <td>
 <p>AccessScopeAgnostic</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ReplicateServer</p>
 </td>
 <td>
 <p>ReplicateFailoverServerDelegate</p>
 </td>
 <td>
 <p>MsmDhcpReplicateOperation</p>
 </td>
 <td>
 <p>AccessScopeAgnostic</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CreateDhcpFilters</p>
 </td>
 <td>
 <p>CreateDhcpFiltersDelegate</p>
 </td>
 <td>
 <p>MsmDhcpCreateEditFilter</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>UpdateDhcpFilter</p>
 </td>
 <td>
 <p>UpdateDhcpFilterDelegate</p>
 </td>
 <td>
 <p>MsmDhcpCreateEditFilter</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>UpdateDhcpFilters</p>
 </td>
 <td>
 <p>UpdateDhcpFiltersDelegate</p>
 </td>
 <td>
 <p>MsmDhcpCreateEditFilter</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>DeleteDhcpFilters</p>
 </td>
 <td>
 <p>DeleteDhcpFiltersDelegate</p>
 </td>
 <td>
 <p>MsmDhcpDeleteFilter</p>
 </td>
 <td>
 <p>DhcpServer</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CreateIpamIPAddress</p>
 </td>
 <td>
 <p>SaveIpamIPAddressDelegate</p>
 </td>
 <td>
 <p>CreateIPAddress</p>
 </td>
 <td>
 <p>IPRange</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>UpdateIpamIPAddress</p>
 </td>
 <td>
 <p>UpdateIpamIPAddressDelegate</p>
 </td>
 <td>
 <p>UpdateIPAddress</p>
 </td>
 <td>
 <p>IPRange</p>
 </td>
 </tr>
</table>

<p> </p>


 </div>
 </div>
 </div>
 </body>
</html>