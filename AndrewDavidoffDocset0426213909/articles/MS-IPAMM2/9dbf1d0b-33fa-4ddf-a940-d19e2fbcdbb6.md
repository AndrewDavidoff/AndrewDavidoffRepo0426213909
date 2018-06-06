<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.19.4.4.1.34 UpdateDhcpFiltersDelegate</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This processing is done when the
IpamOperationWithProgressParameter.OperationId is
AdminOperationId.UpdateDhcpFilters. The IpamOperationWithProgressParameter
instance in this case MUST be of type UpdateDhcpFiltersParameters. </p>

<p>This operation updates the filter properties of a collection
of DHCP filters. In the following steps, any time a fault is generated, the
SetOverallStatus SHOULD be called with the fault details.</p>

<ol><li><p><span> </span>If
IpamOperationWithProgressParameter is NULL or not of type
UpdateDhcpFiltersParameters, generate an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a> (as specified in
section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>).
Project IpamOperationWithProgressParameter in a local variable as
UpdateDhcpFiltersParameters.</p>

</li><li><p><span> </span>If
UpdateDhcpFiltersParameters.Filters is NULL or
UpdateDhcpFiltersParameters.Filters.count is 0, generate an appropriate SOAP
fault (as specified in section 2.2.2.1).</p>

</li><li><p><span> </span>For each Filter
entry in the collection UpdateDhcpFiltersParameters.Filters, copy the filter
instance in a local variable localFilter and the do the following steps:</p>

<ol><li><p><span> 
</span>Check if a row exists in <b>ADM_DhcpFiltersTable</b> in which <b>ADM_DhcpFiltersTable.FilterId</b>
is localFilter.FilterId and ADM_DhcpFiltersTable.ServerId is
localFilter.ServerId.</p>

</li><li><p><span> 
</span>If the row exists, update the row of <b>ADM_DhcpFiltersTable</b> with
the properties of the filter specified in the localFilter. </p>

</li><li><p><span> 
</span>If the row does not exist, create a new row in <b>ADM_DhcpFiltersTable</b>
and initialize it with the FilterId and ServerId and the filter properties from
localFilter.</p>

</li><li><p><span> 
</span>Call SetOverallStatus with Success and 100% completion.</p>

</li></ol></li></ol>
 </div>
 </div>
 </div>
 </body>
</html>