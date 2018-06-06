<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.5.31 DhcpReservationStatus</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This simple type is an enumeration that specifies when a
reservation on a DHCP server is active or inactive.</p>

<dl>
<dd>
<div><pre> &lt;xs:simpleType name=&quot;DhcpReservationStatus&quot;&gt;
   &lt;xs:restriction base=&quot;xsd:string&quot;&gt;
     &lt;xs:enumeration value=&quot;Inactive&quot; /&gt;
     &lt;xs:enumeration value=&quot;Active&quot; /&gt;
   &lt;/xs:restriction&gt;
 &lt;/xs:simpleType&gt;
</pre></div>
</dd></dl>

<p>The following table specifies the valid values for this type.</p>

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
 <p>Inactive</p>
 </td>
 <td>
 <p>The DHCP reservation is inactive.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>Active</p>
 </td>
 <td>
 <p>The DHCP reservation is active.</p>
 </td>
 </tr>
</table>

<p> </p>


 </div>
 </div>
 </div>
 </body>
</html>