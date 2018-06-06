<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.3.4.79 GetIPAddressesByIds</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This operation is used to retrieve the specified collection
of IP address objects from the IPAM data store.</p>

<dl>
<dd>
<div><pre> &lt;wsdl:operation name=&quot;GetIPAddressesByIds&quot;&gt;
   &lt;wsdl:input wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetIPAddressesByIds&quot; message=&quot;ipam:IIpamServer_GetIPAddressesByIds_InputMessage&quot; /&gt;
   &lt;wsdl:output wsaw:Action=&quot;http://Microsoft.Windows.Ipam/IIpamServer/GetIPAddressesByIdsResponse&quot; message=&quot;ipam:IIpamServer_GetIPAddressesByIds_OutputMessage&quot; /&gt;
 &lt;/wsdl:operation&gt;
</pre></div>
</dd></dl>

<p>Upon receiving the
IIpamServer_GetIPAddressesByIds_InputMessage request message, the server
performs the following processing steps. Upon successful completion of the
processing, the server MUST respond with an
IIpamServer_GetIPAddressesByIds_OutputMessage message. In the event of a
failure, an appropriate <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_ec8728a8-1a75-426f-8767-aa1932c7c19f">SOAP
fault</a> MUST be sent to the client as specified in section <a href="a90ad88d-2468-4ac1-bbb9-8f921d15bbc8.md">2.2.2.1</a>.</p>

<ol><li><p><span> </span>If <b>GetIPAddressesByIds.addressFamily</b>
is InterNetwork, the rest of the processing is done with the IPv4-specific
tables. <b>GetIPAddressesByIdsResponse.GetIPAddressesByIdsResult</b> will
consist of a collection of <b>IpamIPv4Address</b>. Otherwise IPv6-specific
tables are used for further processing. <b>GetIPAddressesByIdsResponse.GetIPAddressesByIdsResult</b>
will consist of a collection of <b>IpamIPv6Address</b>.</p>

</li><li><p><span> </span>If <b>GetIPAddressesByIds.Ids</b>
is NULL, an appropriate SOAP fault MUST be returned.</p>

</li><li><p><span> </span>If number of
entries in <b>GetIPAddressesByIds.Ids</b> is 0, then return NULL.</p>

</li><li><p><span> </span>Initialize <b>GetIPAddressesByIdsResponse.GetIPAddressesByIdsResult</b>
to an empty collection.</p>

</li><li><p><span> </span>For each record
identifier <b>RecordId</b> in the <b>GetIPAddressesByIds.ids</b>:</p>

<ol><li><p><span> 
</span>Get the IpamIPAddress corresponding to the <b>RecordId</b> by calling
the GetIPAddressFromTable procedure of <b>ADM_IPAddressTable</b> passing the <b>RecordId</b>
as <i>Param_id</i> input parameter and <b>GetIPAddressesByIds.addressFamily</b>
as the <i>Param_addressfamily</i> input parameter</p>

</li><li><p><span> 
</span>If the result address is obtained, add it to the <b>GetIPAddressesByIdsResponse.GetIPAddressesByIdsResult</b>
collection.</p>

</li></ol></li></ol>
 </div>
 </div>
 </div>
 </body>
</html>