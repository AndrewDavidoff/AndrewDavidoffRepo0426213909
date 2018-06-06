<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.153 DhcpScopeV6</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The DhcpScopeV6 complex type allows the extension of the
DhcpScope complex type. This specifies a scope for specifying IPv6 address
assignment with DHCP. As this depicts the IPv6 DHCP scope, the StartAddress and
EndAddress MUST be valid IPv6 address. The PrefixLength MUST be greater than or
equal to 1 and MUST be no greater than 127.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;DhcpScopeV6&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:DhcpScope&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;PreferredLeaseTime&quot; type=&quot;ser:duration&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;PurgeInterval&quot; type=&quot;ser:duration&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ScopePreference&quot; type=&quot;xsd:unsignedByte&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ScopeType&quot; type=&quot;ipam:AddressAssignment&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;StatelessClientInventoryLoggingStatus&quot; type=&quot;ipam:DhcpStatelessClientInventoryStatus&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ValidLeaseTime&quot; type=&quot;ser:duration&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>PreferredLeaseTime</b>: Specifies the Preferred
Lease Time duration of the DHCPv6 scope.</p>

<p><b>PurgeInterval</b>: Specifies the duration at which
the <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_e66a722d-aa47-4e20-b278-07d026c3d6cd">DHCPv6 stateless client
inventory</a> records are to be purged for the specified scope on the DHCP
server instance.</p>

<p><b>ScopePreference</b>: Specifies the scope
preference setting associated with the DHCPv6 scope.</p>

<p><b>ScopeType</b>: Specifies the address assignment
type of the scope – whether it is dynamic or stateless address assignment.</p>

<p><b>StatelessClientInventoryLoggingStatus</b>:
Specifies the DHCPv6 stateless client inventory logging is to be enabled for
the scope or not.</p>

<p><b>ValidLeaseTime</b>: Specifies the Valid Lease Time
duration of the DHCPv6 scope.</p>


 </div>
 </div>
 </div>
 </body>
</html>