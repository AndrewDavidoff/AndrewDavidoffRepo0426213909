<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.6.1.2.4 Duplicating the Contents of One Node to Another</title>
        <xml>
            <mshelp:toctitle title="2.6.1.2.4 Duplicating the Contents of One Node to Another"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-PST]: Duplicating the Contents of One Node to Another"></mshelp:rltitle>
            <mshelp:keyword index="A" term="9daacaf8-19b2-44ca-ba66-a6ce17cebbf4"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="9daacaf8-19b2-44ca-ba66-a6ce17cebbf4"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-PST]: Duplicating the Contents of One Node to Another" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.6.1.2.4 Duplicating the Contents of One Node to Another</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>Copying all the contents of an existing node to a new node,
where the new node can be a top-level node or a subnode (for example, when a <a href="08220cc9-69b1-4072-a2e7-2a0ff201d505.htm#gt_b6c15d0c-d992-421d-ba96-99d3b63894cf">Message object</a> is added to
another Message object as an <a href="08220cc9-69b1-4072-a2e7-2a0ff201d505.htm#gt_6ab4cacc-0e1a-4843-b9e5-4f1fee5a695a">Attachment
object</a>). Both nodes end up referencing the same instance of the data block,
and subnodes (that is, single-instancing). </p>

<table>
 <thead>
  <tr>
   <th>
   <p>Requirement level</p>
   </th>
   <th>
   <p><b><span>Actions</span></b></p>
   </th>
  </tr>
 </thead>
 <tr>
  <td>
  <p>Required</p>
  </td>
  <td>
  <p>The BBT Reference Count for <b>bidData</b> and <b>bidSub</b>
  of the existing node MUST be incremented.</p>
  <p>The NBT or SLBLOCK MUST be updated, depending on
  whether the target is a node or subnode,  to reflect the new node, using the
  same <b>bidData</b> and <b>bidSub</b> values as the existing node.</p>
  <p>The corresponding <b>rgnind</b>[<b>nidType</b>] field
  in the HEADER.ROOT structure MUST be incremented.</p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Recommended</p>
  </td>
  <td>
  <p>None.</p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Optional</p>
  </td>
  <td>
  <p>None.</p>
  </td>
 </tr>
</table>

<p>Possible side effects:</p>

<table>
 <thead>
  <tr>
   <th>
   <p>Scenario</p>
   </th>
   <th>
   <p>Impact</p>
   </th>
  </tr>
 </thead>
 <tr>
  <td>
  <p>NBT page too full.</p>
  </td>
  <td>
  <p>The NBT might need more levels or need to be balanced.</p>
  </td>
 </tr>
 <tr>
  <td>
  <p>The target is a subnode and the SLBLOCK is full.</p>
  </td>
  <td>
  <p>The subnode BTree needs to grow in depth to
  accommodate new subnode entry.</p>
  </td>
 </tr>
</table>

<p>If <b>bidData</b> points to a data tree, there is no need to
recursively increment the reference count of its child data blocks.</p>

<p>If the node contains a subnode, there is no need to
recursively increment the reference count of its child data blocks.</p>

<p>In many cases the existing node and new node have a
different <b>nidParent</b>. </p>


                </div>
            </div>
        </div>
    </body>
</html>