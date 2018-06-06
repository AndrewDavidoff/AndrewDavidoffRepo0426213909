<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.5.20 DhcpFailoverState</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This simple type is an enumeration that specifies the state
of the failover relationship between two DHCP servers.</p>

<dl>
<dd>
<div><pre> &lt;xs:simpleType name=&quot;DhcpFailoverState&quot;&gt;
   &lt;xs:restriction base=&quot;xsd:string&quot;&gt;
     &lt;xs:enumeration value=&quot;Unknown&quot; /&gt;
     &lt;xs:enumeration value=&quot;NoState&quot; /&gt;
     &lt;xs:enumeration value=&quot;Init&quot; /&gt;
     &lt;xs:enumeration value=&quot;Startup&quot; /&gt;
     &lt;xs:enumeration value=&quot;Normal&quot; /&gt;
     &lt;xs:enumeration value=&quot;CommunicationsInterrupted&quot; /&gt;
     &lt;xs:enumeration value=&quot;PartnerDown&quot; /&gt;
     &lt;xs:enumeration value=&quot;PotentialConflict&quot; /&gt;
     &lt;xs:enumeration value=&quot;ConflictDone&quot; /&gt;
     &lt;xs:enumeration value=&quot;ResolutionInterrupted&quot; /&gt;
     &lt;xs:enumeration value=&quot;Recover&quot; /&gt;
     &lt;xs:enumeration value=&quot;RecoverWait&quot; /&gt;
     &lt;xs:enumeration value=&quot;RecoverDone&quot; /&gt;
   &lt;/xs:restriction&gt;
 &lt;/xs:simpleType&gt;
</pre></div>
</dd></dl>

<p>The following table specifies the valid values for this
type. For more details on each state, see <a href="https://go.microsoft.com/fwlink/?LinkId=217377">[IETF-DHCPFOP-12]</a>.</p>

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
 <p>Unknown</p>
 </td>
 <td>
 <p>The state of the failover relationship is unknown.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>NoState</p>
 </td>
 <td>
 <p>No state has been set for the failover relationship.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>Init</p>
 </td>
 <td>
 <p>The failover relationship is in an Init state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>Startup</p>
 </td>
 <td>
 <p>The failover relationship is in the startup state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>Normal</p>
 </td>
 <td>
 <p>The failover relationship is in the Normal state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>CommunicationsInterrupted</p>
 </td>
 <td>
 <p>The failover relationship is in
 CommunicationsInterrupted state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>PartnerDown</p>
 </td>
 <td>
 <p>The failover relationship is in PartnerDown state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>PotentialConflict</p>
 </td>
 <td>
 <p>The failover relationship is in PotentialConflict
 state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ConflictDone</p>
 </td>
 <td>
 <p>The failover relationship is in ConflictDone state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>ResolutionInterrupted</p>
 </td>
 <td>
 <p>The failover relationship is in ResolutionInterrupted
 state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>Recover</p>
 </td>
 <td>
 <p>The failover relationship is in Recover state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>RecoverWait</p>
 </td>
 <td>
 <p>The failover relationship is in RecoverWait state.</p>
 </td>
 </tr>
 <tr>
 <td>
 <p>RecoverDone</p>
 </td>
 <td>
 <p>The failover relationship is in RecoverDone state.</p>
 </td>
 </tr>
</table>

<p> </p>


 </div>
 </div>
 </div>
 </body>
</html>