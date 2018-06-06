<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.308 IPRangeByVirtualizationTypeParameters</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The IPRangeByVirtualizationTypeParameters complex type
specifies the criteria to be used for enumerating the IP range instances that
are of a given virtualization type.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;IPRangeByVirtualizationTypeParameters&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:EnumerationParametersBase&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;AddressFamily&quot; type=&quot;syssock:AddressFamily&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;VirtualizationType&quot; nillable=&quot;true&quot; type=&quot;ipam:IPVirtualizationType&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>AddressFamily</b>: This specifies the address
family of the IP range instances to be enumerated.</p>

<p><b>VirtualizationType</b>: This specifies the
virtualization type to be used to filter the list of IP range instances that
are enumerated.</p>


 </div>
 </div>
 </div>
 </body>
</html>