<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.87 GetLogicalGroupUtilizationByType</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation retrieves the logical group utilization based
on the trend type requested.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetLogicalGroupUtilizationByType&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetLogicalGroupUtilizationByType&quot; message=&quot;ipam:IIpamServer_GetLogicalGroupUtilizationByType_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetLogicalGroupUtilizationByTypeResponse&quot; message=&quot;ipam:IIpamServer_GetLogicalGroupUtilizationByType_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetLogicalGroupUtilizationByType_InputMessage request message, the
server performs the following processing steps. Upon successful completion of
the steps specified below, the server MUST respond with the
IIpamServer_GetLogicalGroupUtilizationByType_OutputMessage message. In the
event of a failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a> MUST be sent to
the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>If
GetLogicalGroupUtilizationByType.groupNode is NULL or
GetLogicalGroupUtilizationByType.groupType is not LogicalGroupType.Range, an
appropriate SOAP fault MUST be generated.</p>

</li><li><p><span> </span>Call the
procedure GetUtilizationTrendForLogicalGroupNode in <b>ADM_IPRangeTable</b>
passing the following parameters:</p>

<ul><li><p><span><span> </span></span><i>Param_logicalGroupNode</i>
is assigned the value of GetLogicalGroupUtilizationByType.groupNode.</p>

</li><li><p><span><span> </span></span><i>Param_addressfamily</i>
is assigned the value of GetLogicalGroupUtilizationByType.addressFamily.</p>

</li><li><p><span><span> </span></span><i>Param_utilizationType</i>
is set to GetLogicalGroupUtilizationByType.ipUtilizationType.</p>

</li><li><p><span><span> </span></span><i>Param_startDate</i>
is assigned the value of NULL.</p>

</li><li><p><span><span> </span></span><i>Param_endDate</i>
is assigned the value of NULL.</p>

</li></ul></li><li><p><span> </span>Assign
Result_utilization to GetLogicalGroupUtilizationByPeriodResponse.GetLogicalGroupUtilizationByPeriodResult.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>