<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.6.2.4.1 Creating a TC</title>
        <xml>
            <mshelp:toctitle title="2.6.2.4.1 Creating a TC"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-PST]: Creating a TC"></mshelp:rltitle>
            <mshelp:keyword index="A" term="a3cafcd6-454a-46b4-a122-ebbda9ae56fb"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="a3cafcd6-454a-46b4-a122-ebbda9ae56fb"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-PST]: Creating a TC" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.6.2.4.1 Creating a TC</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>Creating a Table Context. This involves creating a heap node
with specialized contents (section <a href="a29ef0f7-1a42-4483-a14c-c245d066e23a.htm">2.6.2.1.1</a>), and an
embedded BTH within the HN (section <a href="bfb05b53-2091-49be-a9e1-1d2434f997ed.htm">2.6.2.2.1</a>).</p>

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
  <p>See section 2.6.2.1.1 and 2.6.2.2.1.</p>
  <p>The TCINFO (section <a href="45b3a0c5-d6d6-4e02-aebf-13766ff693f0.htm">2.3.4.1</a>) and <b>TCOLDESC</b>
  (section <a href="3a2f63cf-bb40-4559-910c-e55ec43d9cbb.htm">2.3.4.2</a>)
  structures MUST be properly initialized.</p>
  <p>The embedded BTH key and data fields MUST be set up
  according to the TCROWID structure (see section <a href="e20b5cf4-ea56-48b8-a8fa-e086c9b862ca.htm">2.3.4.3.1</a>).</p>
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

<p>Possible side effects: See section 2.6.2.1.1 and 2.6.2.2.1.</p>

<p>When setting up the <b>TCOLDESC</b> structures, special care
MUST be given when assigning the <b>iBit</b> fields to ensure the proper
ordering of the columns based on the column data size (section 2.3.4.2).</p>

<p>Also see section 2.3.4.2 for the rules regarding setting the
<b>cbData</b> field of <b>TCOLDESC</b>, noting the use of HNIDs for
variable-size data or fixed-size data that exceeds 8 bytes.</p>


                </div>
            </div>
        </div>
    </body>
</html>