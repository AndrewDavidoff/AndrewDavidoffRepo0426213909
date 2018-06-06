<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.211 DnsReverseLookupZoneEnumerationParameters</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The DnsReverseLookupZoneEnumerationParameters complex type
is used to specify the criteria to be used for enumerating the reverse lookup
DNS zones.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;DnsReverseLookupZoneEnumerationParameters&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:EnumerationParametersBase&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Filter&quot; nillable=&quot;true&quot; type=&quot;serarr:ArrayOfKeyValueOfDnsReverseLookupZoneFilterCriteriaanyType2zwQHvQz&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>Filter: </b> This specifies a key value pair of
filter conditions. The key specifies the DnsReverseLookupZoneFilterCriteria and
the value specifies the value to be used for filtering for the filter criteria
specified in the key.</p>


 </div>
 </div>
 </div>
 </body>
</html>