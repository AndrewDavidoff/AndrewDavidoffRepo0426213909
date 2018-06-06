<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.1.1.1.1.2.9 GetUtilizationTrendForLogicalGroupNode</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This procedure can be used to retrieve the address range
utilization trend for the logical group node specified. The following are the
input parameters to this procedure:</p>

<p><b>Param_logicalGroupNode: </b> The LogicalGroupNode
for which the address range utilization is being requested.</p>

<p><b>Param_addressfamily: </b> The AddressFamily of the
address range for which the utilization information for the logical group node
is being requested.</p>

<p><b>Param_utilizationType: </b> This is of type
IPUtilizationType, specifying the type of utilization data that is being
requested.</p>

<p><b>Param_startDate: </b> This is the start date of
the duration for which the utilization trend is being requested.</p>

<p><b>Param_endDate: </b> This is the end date of the
duration for which the utilization trend is being requested.</p>

<p>The following is the output parameter of this procedure.</p>

<p><b>Result_utilization: </b> This will be of type
IPCumulativeUtilization having IpUtilization to be a collection of
IPUtilization. If <i>Param_addressfamily</i> is InterNetwork, the
IPv4Utilization is returned and IPv6Utilization if <i>Param_addressfamily</i>
is InterNetworkV6.</p>

<p>The following are the processing steps involved.</p>

<ol><li><p><span> </span>Call the
procedure GetObjectIdsForLogicalGroupNode passing the following parameters:</p>

<ul><li><p><span><span> </span></span><i>Param_logicalGroupNode</i></p>

</li><li><p><span><span> </span></span><i>Param_objectType</i>
is assigned the value of EnumerationObjectType.IPRange.</p>

</li><li><p><span><span> </span></span><i>Param_addressfamily</i>.</p>

</li></ul></li><li><p><span> </span>If <i>Param_addressfamily</i>
is InterNetwork, initialize Result_utilization to IPv4Utilization, otherwise
initialize Result_utilization to IPv6Utilization.</p>

</li><li><p><span> </span>For each id in
Result_ObjectIds:</p>

<ol><li><p><span> 
</span>Call the procedure GetIPRangeFromTable passing id as <i>Param_Id</i> and
<i>Param_addressfamily</i>.</p>

</li><li><p><span> 
</span>If <i>Param_utilizationType</i> is Current:</p>

<ol><li><p><span> </span>Add
result.UtilizationStatistics to Result_utilization.</p>

</li></ol></li><li><p><span> 
</span>Otherwise, if <i>Param_addressFamily</i> is InterNetworkV6 or <i>Param_utilizationType</i>
is not Current:</p>

<ol><li><p><span> </span>Call the
procedure GetRangeUtilization passing the following parameters:</p>

<ul><li><p><span><span> 
</span></span><i>Param_id</i> is set to id.</p>

</li><li><p><span><span> 
</span></span><i>Param_addressfamily</i></p>

</li><li><p><span><span> 
</span></span><i>Param_utilizationType</i></p>

</li><li><p><span><span> 
</span></span><i>Param_startDate</i></p>

</li><li><p><span><span> 
</span></span><i>Param_endDate</i></p>

</li></ul></li><li><p><span> </span>Add the
corresponding members of IPCumulativeUtilization with Result_utilization.</p>

</li></ol></li></ol></li><li><p><span> </span>Return <i>Result_utilization</i>
as the output parameter of this procedure. </p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>