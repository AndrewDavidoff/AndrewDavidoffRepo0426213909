<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.6.1.1.8 Modifying a Page</title>
        <xml>
            <mshelp:toctitle title="2.6.1.1.8 Modifying a Page"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-PST]: Modifying a Page"></mshelp:rltitle>
            <mshelp:keyword index="A" term="e287bee3-dd1a-49aa-86cf-d0f5e4f49efe"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="e287bee3-dd1a-49aa-86cf-d0f5e4f49efe"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-PST]: Modifying a Page" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.6.1.1.8 Modifying a Page</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>Modifying the contents of a page.</p>

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
  <p>MUST check the <b>fAMapValid</b> value in the ROOT
  structure before proceeding (see section <a href="d9bcc1fd-c66a-41b3-b6d7-ed09d2a25ced.htm">2.6.1.3.7</a>).</p>
  <p>Create a new page for the modifications (section <a href="40703178-c913-468c-ad44-e50e61e6db94.htm">2.6.1.1.4</a>).</p>
  <p>Replace references to the old page BID with the new
  page BID.</p>
  <p>Free the old page (section <a href="7e1477b0-af44-41f8-b6d6-8ca31951333f.htm">2.6.1.1.6</a>).</p>
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
  <p>Free slot of required size not found.</p>
  </td>
  <td>
  <p>The PST File needs to grow. Refer to section <a href="cbea68b6-e93e-4477-a8ae-7e71c6b7908e.htm">2.6.1.1.2</a> for additional
  considerations.</p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Higher-level pages reference this page.</p>
  </td>
  <td>
  <p>Higher-level pages MUST be recursively modified using
  the same mechanism.</p>
  </td>
 </tr>
</table>

<p> </p>


                </div>
            </div>
        </div>
    </body>
</html>