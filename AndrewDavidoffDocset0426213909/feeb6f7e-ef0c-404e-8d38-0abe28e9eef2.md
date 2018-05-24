<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>3.1.4.3 Creating and Sending TableModified Event Notifications</title>
        <xml>
            <mshelp:toctitle title="3.1.4.3 Creating and Sending TableModified Event Notifications"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-OXCNOTIF]: Creating and Sending TableModified Event Notifications"></mshelp:rltitle>
            <mshelp:keyword index="A" term="feeb6f7e-ef0c-404e-8d38-0abe28e9eef2"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="feeb6f7e-ef0c-404e-8d38-0abe28e9eef2"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-OXCNOTIF]: Creating and Sending TableModified Event Notifications" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">3.1.4.3 Creating and Sending TableModified Event Notifications</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>If the client has subscribed to <b>TableModified</b> event
notifications, by using the <b>RopRegisterNotification</b> <a href="04fcfcd9-a11c-47cd-aa0c-c10a4085d0c8.htm#gt_3369fdd6-36f8-4a62-9cd7-2738ffb5048f">ROP</a> (section <a href="b7722064-1809-477b-8cba-f7b7d6c4046d.htm">2.2.1.2.1</a>), the server
SHOULD<a id="Appendix_A_Target_12"></a><a href="e58b7ae4-9c40-46e0-8844-3b9b2aba2d86.htm#Appendix_A_12" aria-label="Product behavior note 12">&lt;12&gt;</a> require that a table view is
created in order to send the <b>TableModified</b> event notifications, as
specified in section <a href="feaccb32-c2ff-4859-94b0-f1dff18f4853.htm">2.2.1.1.1</a>.
If a table view is required on the server, the server MUST receive a request from
one of the following ROPs, each of which cause a table view to be created on
the server: <b>RopCollapseRow</b> (<mshelp:link keywords="13af6911-27e5-4aa0-bb75-637b02d4f2ef" tabindex="0">[MS-OXCROPS]</mshelp:link>
section <mshelp:link keywords="93a993d2-39f6-4749-b742-5c76f08bddeb" tabindex="0">2.2.5.17</mshelp:link>),
<b>RopExpandRow</b> ([MS-OXCROPS] section <mshelp:link keywords="5b7c510b-20ae-4203-996a-000f477924fe" tabindex="0">2.2.5.16</mshelp:link>),
<b>RopFindRow</b> ([MS-OXCROPS] section <mshelp:link keywords="f109138e-cc0d-4d9f-9546-c9dd0086b5f9" tabindex="0">2.2.5.13</mshelp:link>),
<b>RopQueryColumnsAll</b> ([MS-OXCROPS] section <mshelp:link keywords="a38f25d9-16b8-4503-9fe7-9a62a0b165d9" tabindex="0">2.2.5.12</mshelp:link>),
<b>RopQueryPosition</b> ([MS-OXCROPS] section <mshelp:link keywords="869e9775-fae1-4463-8954-af8b9b172c44" tabindex="0">2.2.5.7</mshelp:link>),
<b>RopQueryRows</b> ([MS-OXCROPS] section <mshelp:link keywords="5b55f0d2-6304-4f8c-87dc-79786bbe5cd6" tabindex="0">2.2.5.4</mshelp:link>),
<b>RopSeekRow</b> ([MS-OXCROPS] section <mshelp:link keywords="b0becf9d-32e3-4c6f-82dd-3fd4fddb8b8a" tabindex="0">2.2.5.8</mshelp:link>),
<b>RopSeekRowFractional</b> ([MS-OXCROPS] section <mshelp:link keywords="369afabd-b570-4076-9b43-8d5ece6cae14" tabindex="0">2.2.5.10</mshelp:link>),
and <b>RopSeekRowBookmark</b> ([MS-OXCROPS] section <mshelp:link keywords="b87cf057-c0f2-427e-8eb8-faa54cb62276" tabindex="0">2.2.5.9</mshelp:link>).
The server SHOULD then create a subscription to <b>TableModified</b> event
notifications automatically for every table created on the server. The server
MUST NOT create a subscription to table notifications for the tables that were
created with a <b>NoNotifications</b> flag. For more details about the <b>NoNotifications</b>
flag, see <mshelp:link keywords="c0f31b95-c07f-486c-98d9-535ed9705fbf" tabindex="0">[MS-OXCFOLD]</mshelp:link>
section <mshelp:link keywords="09a42aeb-41cf-4cac-a232-c0645648bba6" tabindex="0">2.2.1.14.1</mshelp:link>
and [MS-OXCFOLD] section <mshelp:link keywords="c74fc153-06db-49f8-9ce8-5ee85284f78f" tabindex="0">2.2.1.13.1</mshelp:link>.</p>

<p>When a <b>TableModified</b> event occurs, the server
generates a notification using one of the following three methods, listed in
descending order of usefulness to the client.</p>

<ol><li><p><span>    </span>The server
generates an informative notification that specifies the nature of the change
(content or hierarchy), the value of the <b>Folder ID</b> structure, as
specified in <mshelp:link keywords="1afa0cd9-b1a0-4520-b623-bf15030af5d8" tabindex="0">[MS-OXCDATA]</mshelp:link>
section <mshelp:link keywords="1c934e18-441b-4c47-9de0-eb34ffea47e3" tabindex="0">2.2.1.1</mshelp:link>,
the value of the <b>Message ID</b> structure, as specified in [MS-OXCDATA]
section <mshelp:link keywords="f1004d6b-b314-41a8-83cb-c64c3dbeebc4" tabindex="0">2.2.1.2</mshelp:link>,
and new table values. The <b>TableRowAdded</b>, <b>TableRowDeleted</b>, and <b>TableRowModified</b>
events each produce informative notifications.</p>

</li><li><p><span>    </span>The server
generates a basic notification that does not include specifics about the change
made. The <b>TableChanged</b> and <b>TableRestrictionChanged</b> events produce
basic notifications.</p>

</li><li><p><span>    </span>The server does
not generate a notification at all.</p>

</li></ol><p>The notification level is server implementation-specific;
however, the server SHOULD generate informative notifications whenever possible
and only generate a basic notification when it is not feasible to generate an
informative notification.</p>

<p>The server SHOULD<a id="Appendix_A_Target_13"></a><a href="e58b7ae4-9c40-46e0-8844-3b9b2aba2d86.htm#Appendix_A_13" aria-label="Product behavior note 13">&lt;13&gt;</a> stop
sending notifications if the <b>RopResetTable</b> ROP ([MS-OXCROPS] section <mshelp:link keywords="96f1da05-5690-445b-a07d-6ad15f193297" tabindex="0">2.2.5.15</mshelp:link>)
is received, until a new table view is created using one of the following ROPs:
<b>RopCollapseRow</b>, <b>RopExpandRow</b>, <b>RopFindRow</b>, <b>RopQueryColumnsAll</b>,
<b>RopQueryPosition</b>, <b>RopQueryRows</b>, <b>RopSeekRow</b>, <b>RopSeekRowFractional</b>,
or <b>RopSeekRowBookmark</b>.</p>


                </div>
            </div>
        </div>
    </body>
</html>