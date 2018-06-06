<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.63 GetBlockHierarchyForRangeId</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation retrieves the address block hierarchy for an
address block to which a specified range maps.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetBlockHierarchyForRangeId&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetBlockHierarchyForRangeId&quot; message=&quot;ipam:IIpamServer_GetBlockHierarchyForRangeId_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetBlockHierarchyForRangeIdResponse&quot; message=&quot;ipam:IIpamServer_GetBlockHierarchyForRangeId_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetBlockHierarchyForRangeId_InputMessage request message, the
server performs the following processing steps. Upon successful completion of
these steps, the server MUST respond with the
IIpamServer_GetBlockHierarchyForRangeId_OutputMessage message. In the event of
a failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP
fault</a> MUST be sent to the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>Get the address
range corresponding to the GetBlockHierarchyForRangeId.rangeId by calling the
procedure GetIPRangeFromTable passing the following parameters:</p>

<ol><li><p><span> 
</span>Set <i>Param_id</i> to GetBlockHierarchyForRangeId.rangeId.</p>

</li><li><p><span> 
</span>Set <i>Param_addressfamily</i> to
GetBlockHierarchyForRangeId.addressFamily.</p>

</li></ol></li><li><p><span> </span>Initialize
GetBlockHierarchyForRangeIdResponse.GetBlockHierarchyForRangeIdResult to NULL.</p>

</li><li><p><span> </span>If
result.ParentIPBlockId is not 0, call the procedure GetIPBlockFromTable by
passing the following values as input parameters:</p>

<ol><li><p><span> 
</span><i>Param_blockId</i> is set to result.ParentIPBlockId.</p>

</li><li><p><span> 
</span><i>Param_addressfamily</i> is set to
GetBlockHierarchyForRangeId.addressFamily.</p>

</li></ol></li><li><p><span> </span>If the result is
not NULL, it represents the subnet that the range
GetBlockHierarchyForRangeId.rangeId maps to. If result.ParentIPBlockRecordId is
not 0, call GetIPBlockFromTable with following parameters:</p>

<ol><li><p><span> 
</span><i>Param_blockId</i> is set to result. ParentIPBlockRecordId.</p>

</li><li><p><span> 
</span>Param_addressfamily is set to GetBlockHierarchyForRangeId.addressFamily.</p>

</li></ol></li><li><p><span> </span>If <b>result</b>
is not null, perform the following steps:</p>

<ol><li><p><span> 
</span>Enumerate the rows in <b>ADM_IPBlocksTable</b> which meet all the
following condition:</p>

<ol><li><p><span> </span>StartIPAddress
&lt;= result.StartIPAddress.</p>

</li><li><p><span> </span>EndIPAddress
&gt;= result.EndIPAddress.</p>

</li><li><p><span> </span>refixLength
&lt;= result.PrefixLength.</p>

</li></ol></li><li><p><span> 
</span>Arrange the resulting rows in ascending order of StartIPAddress,
EndIPAddress and PrefixLength.</p>

</li><li><p><span> 
</span>Retrieve the IPBlock data for all the rows using their <b>RecordId</b>
and using the GetIPBlockFromTable procedure of <b>ADM_IPBlocksTable</b>.</p>

</li><li><p><span> 
</span>The collection of IPBlock data obtained becomes the block hierarchy for
the address block to which the specified address range maps to. Assign this
collection of IPBlock data to
GetBlockHierarchyForRangeIdResponse.GetBlockHierarchyForRangeIdResult.</p>

</li></ol></li></ol>
 </div>
 </div>
 </div>
 </body>
</html>