<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.4.3 Message Store</title>
        <xml>
            <mshelp:toctitle title="2.4.3 Message Store"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-PST]: Message Store"></mshelp:rltitle>
            <mshelp:keyword index="A" term="aa0539bd-e7bf-4cec-8bde-0b87c2a86baf"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="aa0539bd-e7bf-4cec-8bde-0b87c2a86baf"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-PST]: Message Store" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.4.3 Message Store</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>At the PST level, the <a href="08220cc9-69b1-4072-a2e7-2a0ff201d505.htm#gt_fda94a53-448d-48d5-9991-176c530ff597">message store</a> is the root
of the PST, which is the rough equivalent of the top of a Mailbox. The message
store contains the top-level PST settings and metadata that are required to
access and manage the PST contents.</p>

<p>At the LTP Level, the message store is implemented as a
regular PC. At the NDB Layer, the message store is identified with a special
internal NID value of NID_MESSAGE_STORE (0x21) (see section <a href="0510ece4-6853-4bef-8cc8-8df3468e3ff1.htm">2.4.1</a>). Any valid PST MUST
have exactly one message store node.</p>


                </div>
            </div>
        </div>
    </body>
</html>