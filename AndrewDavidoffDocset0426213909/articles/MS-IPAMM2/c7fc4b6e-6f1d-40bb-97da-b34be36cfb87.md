<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.388 ServerPolicyOptionDataFormatter</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The ServerPolicyOptionDataFormatter complex type allows extended
attributes on an IpamObject type (section <a href="8db9f5bb-a614-4490-8fad-d5a89c448fe8.md">2.2.4.285</a>). It creates
formatted strings with data about the server name, vendor class name, policy
name, and the associated option ID.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;ServerPolicyOptionDataFormatter&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:IpamObject&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;OptionId&quot; type=&quot;xsd:int&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;PolicyName&quot; nillable=&quot;true&quot; type=&quot;xsd:string&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ServerName&quot; nillable=&quot;true&quot; type=&quot;xsd:string&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;VendorClassName&quot; nillable=&quot;true&quot; type=&quot;xsd:string&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>OptionId: </b> An INT that uniquely identifies the
DHCP option.</p>

<p><b>PolicyName: </b> A string that represents the name
of the policy.</p>

<p><b>ServerName: </b> A string that represents the name
of the DHCP server on which the option is configured.</p>

<p><b>VendorClassName: </b> A string that represents the
name of the vendor class associated with the DHCP option.</p>


 </div>
 </div>
 </div>
 </body>
</html>