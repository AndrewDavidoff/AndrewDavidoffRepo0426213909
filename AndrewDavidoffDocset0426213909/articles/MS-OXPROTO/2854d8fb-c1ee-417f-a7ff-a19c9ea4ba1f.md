<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.5.9.5 Protocol-Specific Details</title>
        <xml>
            <mshelp:toctitle title="2.5.9.5 Protocol-Specific Details"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-OXPROTO]: Protocol-Specific Details"></mshelp:rltitle>
            <mshelp:keyword index="A" term="2854d8fb-c1ee-417f-a7ff-a19c9ea4ba1f"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="2854d8fb-c1ee-417f-a7ff-a19c9ea4ba1f"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-OXPROTO]: Protocol-Specific Details" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.5.9.5 Protocol-Specific Details</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>Using <a href="f888c37a-d994-4b91-96a5-e88cfbd66bd6.htm#gt_3369fdd6-36f8-4a62-9cd7-2738ffb5048f">remote
operations (ROPs)</a></p>

<dl>
<dd>
<dl>
<dd>
<p><img id="MS-OXPROTO_pict5d437e73-f2f4-4aa2-826a-6661653d8375.png" src="MS-OXPROTO_files/image025.png" alt="Opening a folder by using ROPs" title="Opening a folder by using ROPs"></p>
</dd>
<dd>
<p><b>Figure 25: Opening a folder by
using ROPs</b></p>
</dd></dl></dd></dl>



<p><b>Note  </b>The ROPs are sent via <a href="f888c37a-d994-4b91-96a5-e88cfbd66bd6.htm#gt_8a7f6700-8311-45bc-af10-82e10accd331">RPC</a> or MAPI extensions for <a href="f888c37a-d994-4b91-96a5-e88cfbd66bd6.htm#gt_d72f1494-4917-4e9e-a9fd-b8f1b2758dcd">HTTP</a>. Several ROPs can be
batched into a single request, as described in <mshelp:link keywords="13af6911-27e5-4aa0-bb75-637b02d4f2ef" tabindex="0">[MS-OXCROPS]</mshelp:link>.</p>

<ol><li><p><span>    </span>The client logs
on to a <a href="f888c37a-d994-4b91-96a5-e88cfbd66bd6.htm#gt_d3ad0e15-adc9-4174-bacf-d929b57278b3">mailbox</a> per the
use case described in section <a href="073b1877-3b61-4cbe-bd4e-8e158a1a8795.htm">2.5.2</a>.</p>

</li><li><p><span>    </span>The messaging
client issues a <b>RopOpenFolder</b> request ([MS-OXCROPS] section <mshelp:link keywords="0ee0a1ff-bd4a-4a8c-aff7-4d029af0a43e" tabindex="0">2.2.4.1</mshelp:link>)
to the Exchange server to open the specified folder.</p>

</li><li><p><span>    </span>The server
responds with a handle to the folder.</p>

</li></ol>
                </div>
            </div>
        </div>
    </body>
</html>