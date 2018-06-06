<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.212 DnsServer</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The DnsServer complex type is used to specify the DNS server
instance properties.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;DnsServer&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:BaseIpamObject&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;AccessScopeId&quot; type=&quot;xsd:long&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;IsInheritedAccessScope&quot; type=&quot;xsd:boolean&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ServerRoleInfo&quot; nillable=&quot;true&quot; type=&quot;ipam:ServerRoleDns&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ZoneHealthSummary&quot; type=&quot;ipam:HealthStatus&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ZoneHealthSummaryLastUpdateTime&quot; nillable=&quot;true&quot; type=&quot;xsd:dateTime&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>AccessScopeId</b>: Indicates the ID in IPAM data
store, of the access scope to which this DNS server is associated.</p>

<p><b>IsInheritedAccessScope</b>: A Boolean that
indicates whether this DNS server has inherited its access scope from its
parent DNS server.</p>

<p><b>ServerRoleInfo</b>: This specifies the
role-specific information for the DNS server, which includes the various access
statuses.</p>

<p><b>ZoneHealthSummary</b>: This specifies the summary
health status for the DNS server.</p>

<p><b>ZoneHealthSummaryLastUpdateTime</b>: This
specifies the time at which the ZoneHealthSummary was last updated by the IPAM
server.</p>


 </div>
 </div>
 </div>
 </body>
</html>