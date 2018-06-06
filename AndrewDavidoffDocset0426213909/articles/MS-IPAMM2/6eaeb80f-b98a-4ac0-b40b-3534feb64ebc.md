<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.4 BulkUpdateRanges</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation provides the ability to modify multiple
ranges with a single operation.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;BulkUpdateRanges&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/BulkUpdateRanges&quot; message=&quot;ipam:IIpamServer_BulkUpdateRanges_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/BulkUpdateRangesResponse&quot; message=&quot;ipam:IIpamServer_BulkUpdateRanges_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the IIpamServer_BulkUpdateRanges_InputMessage,
the server performs the following processing steps. Upon successful completion
of these steps, the server MUST respond with the
IIpamServer_BulkUpdateRanges_OutputMessage.In the event of a failure, an
appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a>
MUST be sent to the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>If the
BulkUpdateRanges.rangesToUpdate is NULL or there are no elements in the
collection, set the BulkUpdateRangesResponse.BulkUpdateRangesResult to NULL and
return.</p>

</li><li><p><span> </span>Initialize
BulkUpdateRangesResponse.BulkUpdateRangesResult to a collection of key value
pairs. </p>

</li><li><p><span> </span>If
BulkUpdateRanges.addressFamily is InterNetwork, then IPv4-specific operations
are used in further processing. Otherwise, IPv6 based operations are used.</p>

</li><li><p><span> </span>For each IPRange
in the BulkUpdateRanges.rangesToUpdate:</p>

<ol><li><p><span> 
</span>Set the <b>updatedRange</b> to the range entry.</p>

</li><li><p><span> 
</span>Perform the range update as specified in section <a href="f6a5a510-69ff-4d25-bd7f-115435a37208.md">3.2.4.2</a>.</p>

</li><li><p><span> 
</span>If the above step generates any SOAP fault, add the failure information
of the SOAP fault to the BulkUpdateRangesResponse.BulkUpdateRangesResult with
the key having the updatedRange.RecordId and the value having the IpamException
having the fault information.</p>

</li></ol></li></ol>
 </div>
 </div>
 </div>
 </body>
</html>