<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.154 DhcpScopeV6TemplateConfiguration</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The DhcpScopeV6TemplateConfiguration complex type is used
for edit operation on a collection of DHCP IPv6 Scopes. It specifies the
properties of the scope that need to be changed for the collection in a
multi-select edit operation.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;DhcpScopeV6TemplateConfiguration&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:DhcpScopeTemplateConfiguration&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;PreferredLeaseTime&quot; type=&quot;ser:duration&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;PurgeInterval&quot; type=&quot;ser:duration&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ScopePreference&quot; type=&quot;xsd:unsignedByte&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;StatelessClientInventoryStatus&quot; type=&quot;ipam:DhcpStatelessClientInventoryStatus&quot; /&gt;
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
the DHCPv6 stateless client inventory records are to be purged for the
specified scope on the DHCP server instance.</p>

<p><b>ScopePreference</b>: Specifies the scope
preference setting associated with the DHCPv6 scope.</p>

<p><b>StatelessClientInventoryStatus</b>: Specifies
whether the DHCPv6 stateless client inventory logging is to be enabled for the
scope.</p>

<p><b>ValidLeaseTime</b>: Specifies the Valid Lease Time
duration of the DHCPv6 scope.</p>


 </div>
 </div>
 </div>
 </body>
</html>