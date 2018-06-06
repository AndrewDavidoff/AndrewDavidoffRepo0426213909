<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.5.81 PolicyProcessingOrderDirection</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This simple type is an enumeration that specifies the
direction in which the DHCP policies are processed.</p>

<dl>
<dd>
<div><pre> &lt;xs:simpleType name=&quot;PolicyProcessingOrderDirection&quot;&gt;
   &lt;xs:restriction base=&quot;xsd:string&quot;&gt;
     &lt;xs:enumeration value=&quot;up&quot; /&gt;
     &lt;xs:enumeration value=&quot;down&quot; /&gt;
   &lt;/xs:restriction&gt;
 &lt;/xs:simpleType&gt;
</pre></div>
</dd></dl>

<p>The following table specifies the valid values for this
type.</p>

<table>
 <thead>
 <tr>
 <th>
 <p>Value</p>
 </th>
 <th>
 <p>Description</p>
 </th>
 </tr>
 </thead>
 <tr>
 <td>
 <p>up</p>
 </td>
 <td>
 <p>The direction in which the DHCP policies are processed
 is from last to first.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>down</p>
 </td>
 <td>
 <p>The direction in which the DHCP policies are processed
 is from first to last.</p>
 </td>
 </tr>
</table>

<p> </p>


 </div>
 </div>
 </div>
 </body>
</html>