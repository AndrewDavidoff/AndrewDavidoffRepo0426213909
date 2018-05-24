<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.4.8.1 Search Update Descriptor (SUD)</title>
        <xml>
            <mshelp:toctitle title="2.4.8.1 Search Update Descriptor (SUD)"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-PST]: Search Update Descriptor (SUD)"></mshelp:rltitle>
            <mshelp:keyword index="A" term="feced5b5-714b-47e1-8ca0-a8aae53c2fe4"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="feced5b5-714b-47e1-8ca0-a8aae53c2fe4"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-PST]: Search Update Descriptor (SUD)" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.4.8.1 Search Update Descriptor (SUD)</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>The SUD represents a single unit of change that can have an
effect on any of the search objects. When a change is made to the contents of a
PST (add, modification, removal, and so on), the modifier is responsible to
create a SUD that describes the change and queue it into the Search Management
Queue (SMQ). In order to prevent wasted space in the PST, the following rules
are applied:</p>

<ol><li><p><span>    </span>If indexing is
enabled for a desktop search, the following types are queued: </p>

<ul><li><p><span><span>  </span></span>SUDT_MSG_ADD</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_MOD</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_DEL</p>

</li><li><p><span><span>  </span></span>SUDT_FLD_ADD</p>

</li><li><p><span><span>  </span></span>SUDT_FLD_MOD</p>

</li><li><p><span><span>  </span></span>SUDT_FLD_DEL</p>

</li><li><p><span><span>  </span></span>SUDT_IDX_MSG_DEL</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_MOV</p>

</li></ul></li><li><p><span>    </span>The following
types are queued: </p>

<ul><li><p><span><span>  </span></span>SUDT_SRCH_ADD</p>

</li><li><p><span><span>  </span></span>SUDT_SRCH_MOD</p>

</li><li><p><span><span>  </span></span>SUDT_SRCH_DEL</p>

</li></ul></li><li><p><span>    </span>If the NIDs of
either old or new parent folders are contained in the SDO, the following types
are queued: </p>

<ul><li><p><span><span>  </span></span>SUDT_MSG_MOV</p>

</li><li><p><span><span>  </span></span>SUDT_FLD_MOV</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_ADD</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_MOD</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_ROW_MOD</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_DEL</p>

</li><li><p><span><span>  </span></span>SUDT_MSG_SPAM</p>

</li><li><p><span><span>  </span></span>SUDT_IDX_MSG_DEL</p>

</li><li><p><span><span>  </span></span>SUDT_FLD_ADD</p>

</li><li><p><span><span>  </span></span>SUDT_FLD_MOD</p>

</li><li><p><span><span>  </span></span>SUDT_FLD_DEL</p>

</li></ul></li><li><p><span>    </span>If none of the
above conditions is satisfied, the SUD is not queued.</p>

</li></ol>
                </div>
            </div>
        </div>
    </body>
</html>