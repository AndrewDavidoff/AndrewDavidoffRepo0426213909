<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.78 CreateIpamIPAddressParameters</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The CreateIpamIPAddressParameters complex type specifies the
information pertaining to the operation CreateIpamIpAddress. This is used as a
callback.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;CreateIpamIPAddressParameters&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:IpamOperationWithProgressParameters&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Address&quot; nillable=&quot;true&quot; type=&quot;ipam:IpamIPAddress&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;CreateDhcpReservation&quot; type=&quot;xsd:boolean&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;CreateDnsRecord&quot; type=&quot;xsd:boolean&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;OverrideMBEAndSI&quot; type=&quot;xsd:boolean&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>Address: </b> The IpamIPAddress (section <a href="364a63ef-be28-498d-a67d-ed3df88b545a.md">2.2.4.257</a>) that represents
the IP address to be created.</p>

<p><b>CreateDhcpReservation: </b> Specifies whether a
DHCP reservation needs to be created for this address.</p>

<p><b>CreateDnsRecord: </b> Specifies whether a DNS
records need to be created for this address.</p>

<p><b>OverrideMBEAndSI: </b> Specifies whether the <b>ManagedByEntity</b>
and <b>ManagedByEntityValue</b> custom fields associated with this
IpamIPAddress need to be overridden.</p>


 </div>
 </div>
 </div>
 </body>
</html>