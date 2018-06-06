<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.5.4.8.1.76 LogicalGroupNodeRootEnumerationParameters</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This is the processing done when the EnumInputParameters
contains data of type LogicalGroupNodeRootEnumerationParameters. The ObjectType
MUST be EnumerationObjectType.LogicalGroupNode. This is used to enumerate the
logical group nodes that will form the top-level children of a specified
logical group.</p>

<p>The following are the steps involved in identifying the rows
to be returned as a part of the enumeration.</p>

<ol><li><p><span> </span>Call the
procedure GetRootLogicalGroupNodesForLogicalGroup in ADM_LogicalGroupsTable
with the following parameters:</p>

<ul><li><p><span><span> </span></span>Param_logicalGroup
is assigned the value of
LogicalGroupNodeRootEnumerationParameters.LogicalGroup.</p>

</li></ul></li><li><p><span> </span>Copy the Result_logicalGroupNodes
to EnumOutputData.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>