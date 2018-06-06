<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.358 ResetConfigSyncStatusDataFormatter</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The ResetConfigSyncStatusDataFormatter complex type allows
extended attributes on an IpamObject type (section <a href="8db9f5bb-a614-4490-8fad-d5a89c448fe8.md">2.2.4.285</a>). It creates
formatted strings with data about the list of DhcpScope objects’ scope IDs for
which this reset is applied.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;ResetConfigSyncStatusDataFormatter&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:IpamObject&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Scopes&quot; nillable=&quot;true&quot; type=&quot;ipam:ArrayOfDhcpScope&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>Scopes</b>: An ArrayOfDhcpScope type (section <a href="03239b00-3ec0-4014-9ca0-45cdb329e877.md">2.2.4.28</a>) that represents
the DHCP scopes whose config sync status has been cleared.</p>


 </div>
 </div>
 </div>
 </body>
</html>