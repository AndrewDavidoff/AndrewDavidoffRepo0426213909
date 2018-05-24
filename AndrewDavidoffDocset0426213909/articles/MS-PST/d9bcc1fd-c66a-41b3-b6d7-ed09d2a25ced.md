<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.6.1.3.7 Crash Recovery and AMap Rebuilding</title>
        <xml>
            <mshelp:toctitle title="2.6.1.3.7 Crash Recovery and AMap Rebuilding"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-PST]: Crash Recovery and AMap Rebuilding"></mshelp:rltitle>
            <mshelp:keyword index="A" term="d9bcc1fd-c66a-41b3-b6d7-ed09d2a25ced"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="d9bcc1fd-c66a-41b3-b6d7-ed09d2a25ced"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-PST]: Crash Recovery and AMap Rebuilding" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.6.1.3.7 Crash Recovery and AMap Rebuilding</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>The <b>fAMapValid</b> flag in the ROOT structure is used to
indicate whether the AMaps in the PST file are in a known-valid state. In
general, this flag is set to one of the two valid states described in section <a href="32ce8c94-4757-46c8-a169-3fd21abee584.htm">2.2.2.5</a>.</p>

<p>At the beginning of any operation that either allocates or
frees space in the PST file, implementations set the <b>fAMapValid</b> value to
INVALID_AMAP, which signifies that the AMaps (and also PMaps, FMaps, and
FPMaps, for that matter) cannot be trusted. When the operation is complete,
this value is set back to the valid state. In the event where the PST file is
abnormally closed before the operation is finished, it is likely that <b>fAMapValid</b>
was never restored back to the valid state. In that case, the PST file MUST go
through a very expensive recovery operation the next time an attempt to
allocate file space is made.</p>

<p>This recovery operation uses a process called an &quot;AMap
rebuild&quot;, which involves first marking all the AMaps as &quot;free&quot;
and then walking the NBT and BBT to mark pages and blocks as
&quot;allocated&quot; in the map pages as they appear.<a id="Appendix_A_Target_23"></a><a href="f040f8b2-f023-4ed9-94fd-de487da83ed5.htm#Appendix_A_23" aria-label="Product behavior note 23">&lt;23&gt;</a> The rebuild process also
ensures that all space occupied by the AMaps, PMaps, FMaps and FPMaps are
properly marked as allocated.</p>

<p>Implementations are NOT required to implement AMap Rebuild
algorithms, but MUST first check the <b>fAMapValid</b> value before
manipulating the AMaps in any way. If the <b>fAMapValid</b> value is set to
invalid, implementations that do not implement AMap Rebuild algorithms MUST NOT
modify the PST file in any way. Read-only implementations, however, MAY ignore
the <b>fAMapValid</b> value.</p>


                </div>
            </div>
        </div>
    </body>
</html>