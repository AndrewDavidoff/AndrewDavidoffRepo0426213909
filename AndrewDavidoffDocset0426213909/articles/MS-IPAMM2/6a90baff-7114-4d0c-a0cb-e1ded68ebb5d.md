<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.220 DnsZone</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The DnsZone complex type specifies the information
pertaining to a <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_2993684a-cc67-43b9-9bb5-185df1582055">forward
lookup DNS zone</a>. The DnsZone complex type allows extension of attributes of
the <b>BaseDnsZone</b> complex type specified in section <a href="8fba2a4f-ae99-4aa4-857d-3647275c61c1.md">2.2.4.63</a>.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;DnsZone&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:BaseDnsZone&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ParentId&quot; type=&quot;xsd:long&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ParentZone&quot; nillable=&quot;true&quot; type=&quot;ipam:DnsZone&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ShortName&quot; nillable=&quot;true&quot; type=&quot;xsd:string&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ZoneOverallHealth&quot; type=&quot;ipam:HealthStatus&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ZoneOverallHealthLastUpdateTime&quot; nillable=&quot;true&quot;type=&quot;xsd:dateTime&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>ParentId: </b> The <b>RecordId</b> of the forward
lookup zone that is hosting the forward lookup DNS zone in a forward lookup DNS
zone hierarchy. </p>

<p><b>ParentZone: </b> This specifies the DnsZone
corresponding to the parent zone specified by <b>ParentId</b>.</p>

<p><b>ShortName: </b> This specifies the short name of
the forward lookup DNS zone. This MUST NOT be NULL and the length MUST be
lesser than 256 characters.</p>

<p><b>ZoneOverallHealth: </b> This specifies the overall
health of the zone.</p>

<p><b>ZoneOverallHealthLastUpdateTime: </b> This
specifies the time at which the <b>ZoneOverallHealth</b> was last updated.</p>


 </div>
 </div>
 </div>
 </body>
</html>