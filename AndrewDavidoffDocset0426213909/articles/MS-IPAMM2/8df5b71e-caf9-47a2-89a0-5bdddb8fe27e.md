<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.237 InvalidWIDDBConfigAuthNotSupportedIpamExceptionData</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This complex type allows extended attributes on an
IpamExceptionData type. It creates objects whose IpamExceptionId is
IpamApiErrorInvalidWIDDBConfigAuthNotSupported.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;InvalidWIDDBConfigAuthNotSupportedIpamExceptionData&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:IpamExceptionData&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;DatabaseAuthenticationType&quot; type=&quot;xsd:int&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>DatabaseAuthenticationType: </b> An integer that
represents the database authentication type.</p>


 </div>
 </div>
 </div>
 </body>
</html>