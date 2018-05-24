<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.2.2.8.3.1 Data Blocks</title>
        <xml>
            <mshelp:toctitle title="2.2.2.8.3.1 Data Blocks"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-PST]: Data Blocks"></mshelp:rltitle>
            <mshelp:keyword index="A" term="d0e6fbaf-00e3-4d4d-bea8-8ab3cdb4fde6"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="d0e6fbaf-00e3-4d4d-bea8-8ab3cdb4fde6"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-PST]: Data Blocks" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.2.2.8.3.1 Data Blocks</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>A data block is a block that is &quot;External&quot; (that
is, not marked &quot;Internal&quot;) and contains data streamed from higher
layer structures. The data contained in data blocks have no meaning to the
structures defined at the NDB Layer.</p>

<p>Unicode:</p>

<table>
 <tr>
  <th><p><br>0</p></th>
  <th><p><br>1</p></th>
  <th><p><br>2</p></th>
  <th><p><br>3</p></th>
  <th><p><br>4</p></th>
  <th><p><br>5</p></th>
  <th><p><br>6</p></th>
  <th><p><br>7</p></th>
  <th><p><br>8</p></th>
  <th><p><br>9</p></th>
  <th><p>1<br>0</p></th>
  <th><p><br>1</p></th>
  <th><p><br>2</p></th>
  <th><p><br>3</p></th>
  <th><p><br>4</p></th>
  <th><p><br>5</p></th>
  <th><p><br>6</p></th>
  <th><p><br>7</p></th>
  <th><p><br>8</p></th>
  <th><p><br>9</p></th>
  <th><p>2<br>0</p></th>
  <th><p><br>1</p></th>
  <th><p><br>2</p></th>
  <th><p><br>3</p></th>
  <th><p><br>4</p></th>
  <th><p><br>5</p></th>
  <th><p><br>6</p></th>
  <th><p><br>7</p></th>
  <th><p><br>8</p></th>
  <th><p><br>9</p></th>
  <th><p>3<br>0</p></th>
  <th><p><br>1</p></th>
 </tr>
 <tr>
  <td colspan="32">
  <p>data
  (variable)</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>padding
  (variable, optional)</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>blockTrailer
  (16 bytes)</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
</table>

<p>ANSI:</p>

<table>
 <tr>
  <th><p><br>0</p></th>
  <th><p><br>1</p></th>
  <th><p><br>2</p></th>
  <th><p><br>3</p></th>
  <th><p><br>4</p></th>
  <th><p><br>5</p></th>
  <th><p><br>6</p></th>
  <th><p><br>7</p></th>
  <th><p><br>8</p></th>
  <th><p><br>9</p></th>
  <th><p>1<br>0</p></th>
  <th><p><br>1</p></th>
  <th><p><br>2</p></th>
  <th><p><br>3</p></th>
  <th><p><br>4</p></th>
  <th><p><br>5</p></th>
  <th><p><br>6</p></th>
  <th><p><br>7</p></th>
  <th><p><br>8</p></th>
  <th><p><br>9</p></th>
  <th><p>2<br>0</p></th>
  <th><p><br>1</p></th>
  <th><p><br>2</p></th>
  <th><p><br>3</p></th>
  <th><p><br>4</p></th>
  <th><p><br>5</p></th>
  <th><p><br>6</p></th>
  <th><p><br>7</p></th>
  <th><p><br>8</p></th>
  <th><p><br>9</p></th>
  <th><p>3<br>0</p></th>
  <th><p><br>1</p></th>
 </tr>
 <tr>
  <td colspan="32">
  <p>data
  (variable)</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>padding
  (variable, optional)</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>blockTrailer</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
 <tr>
  <td colspan="32">
  <p>...</p>
  </td>
 </tr>
</table>

<p><b>data (variable):</b> The value of this field
SHOULD be treated as an opaque <a href="08220cc9-69b1-4072-a2e7-2a0ff201d505.htm#gt_ad861812-8cb0-497a-80bb-13c95aa4e425">binary large object (BLOB)</a>
by the NDB Layer. The size of this field is indicated by the <b>cb</b> subfield
of the <b>blockTrailer </b>field.</p>

<p><b>padding (variable, optional):</b> This field is
present if the size of the <b>data </b>field plus the size of the <b>blockTrailer</b>
field is not a multiple of 64. The size of this field is the smallest number of
bytes required to make the size of the data block a multiple of 64.
Implementations MUST ignore this field.</p>

<p><b>blockTrailer (Unicode: 16 bytes; ANSI: 12 bytes):</b>
A BLOCKTRAILER structure (section <a href="a14943ef-70c2-403f-898c-5bc3747117e1.htm">2.2.2.8.1</a>).</p>


                </div>
            </div>
        </div>
    </body>
</html>