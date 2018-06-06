<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.106 GetSubnetByNetworkIdAndAddressSpace</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation is used to retrieve the IP subnet data having
the specified record identifier.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetSubnetByNetworkIdAndAddressSpace&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetSubnetByNetworkIdAndAddressSpace&quot; message=&quot;ipam:IIpamServer_GetSubnetByNetworkIdAndAddressSpace_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetSubnetByNetworkIdAndAddressSpaceResponse&quot; message=&quot;ipam:IIpamServer_GetSubnetByNetworkIdAndAddressSpace_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt; 
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetSubnetByNetworkIdAndAddressSpace_InputMessage request message,
the server performs the following processing steps. Upon successful completion
of these steps, the server MUST respond with the IIpamServer_GetSubnetByNetworkIdAndAddressSpace_OutputMessage
message. In the event of a failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP fault</a> MUST be sent to
the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>A SOAP fault is
sent if GetSubnetByNetworkIdAndAddressSpace.networkId.addressFamily is NULL or
is neither InterNetwork nor InterNetworkV6. If
GetSubnetByNetworkIdAndAddressSpace.networkId.addressFamily is InterNetwork,
then IPv4-specific tables will be used for further processing. Else
IPv6-specific tables will be used for processing.</p>

</li><li><p><span> </span>Get the IP
subnet by calling the GetSubnetByNetworkIdAndAddressSpace procedure of the <b>ADM_IPSubnetTable</b>
passing the GetSubnetByNetworkIdAndAddressSpace.networkId as <i>Param_NetworkId</i>,
GetSubnetByNetworkIdAndAddressSpace.prefixLength as Param_PrefixLength and
GetSubnetByNetworkIdAndAddressSpace.addressSpaceRecordId as <i>Param_AddressSpaceRecordId</i>.</p>

</li><li><p><span> </span>Assign the Result_Subnet
returned by the previous procedure call to
GetSubnetByNetworkIdAndAddressSpaceResponse.GetSubnetByNetworkIdAndAddressSpaceResult.</p>

</li></ol>
 </div>
 </div>
 </div>
 </body>
</html>