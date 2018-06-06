<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.5.92 ServerInfoNewFlag</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This simple type is an enumeration that summarizes the
change of ServerInfo server instance data between two consecutive discovery
IPAM task executions. </p>

<dl>
<dd>
<div><pre> &lt;xs:simpleType name=&quot;ServerInfoNewFlag&quot;&gt;
   &lt;xs:restriction base=&quot;xsd:string&quot;&gt;
     &lt;xs:enumeration value=&quot;Old&quot; /&gt;
     &lt;xs:enumeration value=&quot;New&quot; /&gt;
     &lt;xs:enumeration value=&quot;Modified&quot; /&gt;
   &lt;/xs:restriction&gt;
 &lt;/xs:simpleType&gt;
</pre></div>
</dd></dl>

<p>The following table describes the various values of this
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
 <p>None</p>
 </td>
 <td>
 <p>Uninitialized or invalid value.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>Old</p>
 </td>
 <td>
 <p>There has been no change to the ServerInfo details.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>New</p>
 </td>
 <td>
 <p>The ServerInfo is a new instance since the last
 execution of the discovery task.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>Modified</p>
 </td>
 <td>
 <p>There has been some change to an existing instance of
 the ServerInfo.</p>
 </td>
 </tr>
</table>

<p> </p>


 </div>
 </div>
 </div>
 </body>
</html>