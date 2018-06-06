<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.236 InvalidSQLDBConfigInvalidPortIpamExceptionData</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This complex type allows extended attributes on an
IpamExceptionData type. It creates objects whose IpamExceptionId is
IpamApiErrorInvalidSQLDBConfigInvalidPort.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;InvalidSQLDBConfigInvalidPortIpamExceptionData&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:IpamExceptionData&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;InputPort&quot; type=&quot;xsd:unsignedInt&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;MaxAllowedPort&quot; type=&quot;xsd:unsignedInt&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;MinAllowedPort&quot; type=&quot;xsd:unsignedInt&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>InputPort: </b>An unsigned int that represents the
port configured for the SQL DB.</p>

<p><b>MaxAllowedPort: </b>An unsigned int that
represents the maximum port number allowed for database configuration. </p>

<p><b>MinAllowedPort: </b>An unsigned int that
represents the minimum port number allowed for database configuration.</p>


 </div>
 </div>
 </div>
 </body>
</html>