<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.204 DnsResourceRecordDataWks</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The DnsResourceRecordDataWks complex type SHOULD<a id="Appendix_A_Target_39"></a><a href="3b257e05-6300-4286-a090-0f9949d290bf.md#Appendix_A_39" aria-label="Product behavior note 39">&lt;39&gt;</a> extend the
DnsResourceRecordData. It specifies the details associated with a DNS resource
record of type WKS.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;DnsResourceRecordDataWks&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:DnsResourceRecordData&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Address&quot; nillable=&quot;true&quot; type=&quot;sysnet:IPAddress&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Protocol&quot; nillable=&quot;true&quot; type=&quot;xsd:string&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Services&quot; nillable=&quot;true&quot; type=&quot;serarr:ArrayOfstring&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>Address: </b> The IP address of the interface on
which the service is provided.</p>

<p><b>Protocol: </b> The protocol supported on the
interface.</p>

<p><b>Services: </b> The list of services provided by
the protocol on the interface.</p>


 </div>
 </div>
 </div>
 </body>
</html>