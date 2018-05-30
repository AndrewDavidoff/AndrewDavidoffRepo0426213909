<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.4.3.1 Report Authoring, Management, and Viewing with Native Report Portal</title>
        <xml>
            <mshelp:toctitle title="2.4.3.1 Report Authoring, Management, and Viewing with Native Report Portal"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-SSSO]: Report Authoring, Management, and Viewing with Native Report Portal"></mshelp:rltitle>
            <mshelp:keyword index="A" term="30ee261d-fa18-42a0-bbdb-cbd10aa94b4a"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="30ee261d-fa18-42a0-bbdb-cbd10aa94b4a"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-SSSO]: Report Authoring, Management, and Viewing with Native Report Portal" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.4.3.1 Report Authoring, Management, and Viewing with Native Report Portal</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p><b>Actions</b></p>

<ol><li><p><span>    </span>Within a report
authoring tool, a report author designs a report and saves it in RDL file
format, as specified in <mshelp:link keywords="53287204-7cd0-4bc9-a5cd-d42a5925dca1" tabindex="0">[MS-RDL]</mshelp:link>. 
</p>

</li><li><p><span>    </span>The authoring
tool publishes the saved report to a <a href="20049766-3c6e-4f20-a20e-64785e88f6f2.htm#gt_cbdd3a12-e9ec-43e2-ac97-9c47f171f96a">report server</a> via methods
of the ReportService2010 API, as specified in <mshelp:link keywords="0c9864cf-afe9-4789-ae9e-a55df1ff9111" tabindex="0">[MS-RSWSRM2010]</mshelp:link>.</p>

</li><li><p><span>    </span>Within the
report server management tool, the report server administrator manages the
reports, resources, schedules, subscriptions, and users within the report
catalog.  </p>

</li><li><p><span>    </span>Each management
operation performed by the administrator is implemented as an API call from the
management tool to the ReportService2010 API.</p>

</li><li><p><span>    </span>Administrators
can publish reports in RDL format via these APIs.</p>

</li><li><p><span>    </span>Within a report
viewing tool, a report consumer specifies a report to execute from within the
report server catalog.</p>

</li><li><p><span>    </span>The report
viewer passes this instruction to the report server via the ReportExecution2005
API, as specified in <mshelp:link keywords="96c33524-52c1-4358-a23a-6921db74211c" tabindex="0">[MS-RSWSRE2005]</mshelp:link>.</p>

</li><li><p><span>    </span>The report
server returns the results of the report execution to the report viewer as
either Report Page Layout, as specified in <mshelp:link keywords="9c4ff7ba-f6da-4092-9670-aa0e54e73887" tabindex="0">[MS-RPL]</mshelp:link>
or a Remote GDI+, as specified in <mshelp:link keywords="b420a652-10eb-49b2-834c-ebc4d31e8ce5" tabindex="0">[MS-RGDI]</mshelp:link>,
depending on which was requested by the report viewer. Note that other standard
formats such as HTML, XML, and PDF can be requested and returned instead.</p>

</li></ol>
                </div>
            </div>
        </div>
    </body>
</html>