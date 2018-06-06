<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.415 sys:TupleOfGetAddressSpaceFilteranyType2zwQHvQz</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This complex type specifies a key value pair wherein <b>m_Item1</b>
specifies an ipam:GetAddressSpaceFilter type specifying the type of filter to
be applied with the value of the filter specified in the <b>m_Item2</b> portion
key value pair entry.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;TupleOfGetAddressSpaceFilteranyType2zwQHvQz&quot;&gt;
   &lt;xs:annotation&gt;
     &lt;xs:appinfo&gt;
       &lt;GenericType Name=&quot;TupleOf{0}{1}{#}&quot; Namespace=&quot;http://schemas.datacontract.org/2004/07/System&quot; xmlns=&quot;http://schemas.microsoft.com/2003/10/Serialization/&quot;&gt;
         &lt;GenericParameter Name=&quot;GetAddressSpaceFilter&quot; Namespace=&quot;http://Microsoft.Windows.Ipam&quot; /&gt;
         &lt;GenericParameter Name=&quot;anyType&quot; Namespace=&quot;http://www.w3.org/2001/XMLSchema&quot; /&gt;
       &lt;/GenericType&gt;
     &lt;/xs:appinfo&gt;
   &lt;/xs:annotation&gt;
   &lt;xs:sequence&gt;
     &lt;xs:element name=&quot;m_Item1&quot; type=&quot;ipam:GetAddressSpaceFilter&quot; /&gt;
     &lt;xs:element name=&quot;m_Item2&quot; nillable=&quot;true&quot; type=&quot;xsd:anyType&quot; /&gt;
   &lt;/xs:sequence&gt;
 &lt;/xs:complexType&gt; 
</pre></div>
</dd></dl>

<p><b>m_Item1</b>: Specifies a filter key criteria as
GetAddressSpaceFilter.</p>

<p><b>m_Item2</b>: Specifies an optional value that is
used to meet the filter criteria defined in <b>m_Item1</b>.</p>


 </div>
 </div>
 </div>
 </body>
</html>