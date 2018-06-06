<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.1.1.1.8.2.1 GetDnsZoneFromTable</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This procedure can be used to retrieve the DnsZone for the
specified record identifier. The following is the input parameter to this
procedure.</p>

<p><b>Param_Id</b>: The <b>RecordId</b> of the DNS <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_e6a86700-c17d-4513-8f4f-5aacaff014df">zone</a> for which the DnsZone
data is being requested.</p>

<p>The following is the output parameter of this procedure:</p>

<p><b>Result_zone</b>: This is the DnsZone corresponding to the
specified record identifier.</p>

<p>The following processing steps are performed.</p>

<ol><li><p><span> </span>Look up the <b>ADM_DNSForwardLookupTable</b>
for the row with the <b>RecordId</b> value equal to <i>Param_Id</i>.</p>

</li><li><p><span> </span>Initialize
Result_zone to DnsZone and assign the following values.</p>

<ul><li><p><span><span> </span></span>Assign
<b>ParentId</b> to Result_zone.ParentId.</p>

</li><li><p><span><span> </span></span>Assign
<b>Name</b> to Result_zone.Name.</p>

</li><li><p><span><span> </span></span>Assign
<b>RecordId</b> to Result_zone.RecordId.</p>

</li><li><p><span><span> </span></span>Copy
the ForwardLookupZoneDetails to Result_zone.</p>

</li></ul></li><li><p><span> </span>Call
GetAccessScopeForObjectIdAndType of <b>ADM_AccessScopeAssociationTable</b>
passing the following parameters:</p>

<ul><li><p><span><span> </span></span><i>Param_objectId</i>
is set to <i>Param_Id</i>.</p>

</li><li><p><span><span> </span></span><i>Param_objectType</i>
is set to IpamObjectType.DNSForwardLookupZone.</p>

</li><li><p><span><span> </span></span><i>Param_accessScopeId</i>.</p>

</li><li><p><span><span> </span></span><i>Param_objectInheritanceStatus</i>.</p>

</li><li><p><span><span> </span></span><i>Param_inheritanceId</i>.</p>

</li></ul></li><li><p><span> </span>Assign <i>Param_accessScopeId</i>
to Result_zone.AccessScopeId.</p>

</li><li><p><span> </span>Assign <i>Param_objectInheritanceStatus</i>
to Result_zone.IsInheritedAccessScope.</p>

</li><li><p><span> </span>Return <i>Result_zone</i>
as the output parameter of this procedure.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>