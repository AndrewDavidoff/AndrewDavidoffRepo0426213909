<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.452 UpdatePolicyPropertiesParameters</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The UpdatePolicyPropertiesParameters allows extended
attributes on an IpamOperationWithProgressParameters type (section <a href="99fc6063-33f2-47ef-8db7-91d89369e3dc.md">2.2.4.286</a>). It creates
objects whose OperationId is UpdatePolicyProperty and associates them to a
collection of DhcpPolicyV4 complex types (section <a href="d159e433-4820-4d34-92d9-7f3afb1014fa.md">2.2.4.132</a>) and an
ipam:DhcpPolicyPropertyUpdate object.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;UpdatePolicyPropertiesParameters&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:IpamOperationWithProgressParameters&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Policies&quot; nillable=&quot;true&quot; type=&quot;ipam:ArrayOfDhcpPolicyV4&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Update&quot; type=&quot;ipam:DhcpPolicyPropertyUpdate&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>Policies: </b> An ArrayOfDhcpPolicyV4 and
represents the policies to be updated.</p>

<p><b>Update: </b> This is of type
ipam:DhcpPolicyPropertyUpdate and represents whether the set of policies are
activated or deactivated.</p>


 </div>
 </div>
 </div>
 </body>
</html>