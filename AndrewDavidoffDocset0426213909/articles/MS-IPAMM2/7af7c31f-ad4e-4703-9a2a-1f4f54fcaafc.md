<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.2 AccessScopeToUserRoleMapping</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>The AccessScopeToUserRoleMapping allows extended attributes
on a BaseIpamObject type (section <a href="1296bf34-5951-47ed-bbe0-a328f0630865.md">2.2.4.64</a>). It describes an
access policy that is an association between a <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_5d2ed62e-6d73-4b4c-a20b-45557fd84370">user role</a> and an <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_acc4994e-631f-4728-9779-af93054fc4b2">access scope</a>.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;AccessScopeToUserRoleMapping&quot;&gt;
  &lt;xs:complexContent mixed=&quot;false&quot;&gt;
  &lt;xs:extension base=&quot;ipam:BaseIpamObject&quot;&gt;
  &lt;xs:sequence&gt;
  &lt;xs:element minOccurs=&quot;0&quot; name=&quot;AccessScopeId&quot; nillable=&quot;true&quot; type=&quot;xsd:long&quot; /&gt;
  &lt;xs:element minOccurs=&quot;0&quot; name=&quot;AccessScopeName&quot; nillable=&quot;true&quot; type=&quot;xsd:string&quot; /&gt;
  &lt;xs:element minOccurs=&quot;0&quot; name=&quot;UserRoleId&quot; nillable=&quot;true&quot; type=&quot;xsd:long&quot; /&gt;
  &lt;xs:element minOccurs=&quot;0&quot; name=&quot;UserRoleName&quot; nillable=&quot;true&quot; type=&quot;xsd:string&quot; /&gt;
  &lt;/xs:sequence&gt;
  &lt;/xs:extension&gt;
  &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
  
</pre></div>
</dd></dl>

<p><b>AccessScopeId</b>:  Represents the <b>RecordId</b>
of the access scope object in the <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_1ebbf4e0-d234-4732-a83d-022081131cea">IPAM data store</a> .</p>

<p><b>AccessScopeName</b>:  A string that represents the
hierarchy of the access scope from the root level.</p>

<p><b>UserRoleId</b>:  An instance of the user role in
the IPAM data store.</p>

<p><b>UserRoleName</b>:  A string that corresponds to
the name of the user role.</p>


 </div>
 </div>
 </div>
 </body>
</html>