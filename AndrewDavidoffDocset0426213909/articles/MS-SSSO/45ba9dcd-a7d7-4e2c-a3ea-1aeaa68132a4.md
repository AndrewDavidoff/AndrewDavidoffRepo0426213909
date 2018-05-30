<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
    <head>
        <meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8"></meta>
        <meta name="save" content="history"></meta>
        <title>2.2.3 Reporting Services</title>
        <xml>
            <mshelp:toctitle title="2.2.3 Reporting Services"></mshelp:toctitle>
            <mshelp:rltitle title="[MS-SSSO]: Reporting Services"></mshelp:rltitle>
            <mshelp:keyword index="A" term="45ba9dcd-a7d7-4e2c-a3ea-1aeaa68132a4"></mshelp:keyword>
            <mshelp:attr name="DCSext.ContentType" value="open specification"></mshelp:attr>
            <mshelp:attr name="AssetID" value="45ba9dcd-a7d7-4e2c-a3ea-1aeaa68132a4"></mshelp:attr>
            <mshelp:attr name="TopicType" value="kbRef"></mshelp:attr>
            <mshelp:attr name="DCSext.Title" value="[MS-SSSO]: Reporting Services" />
        </xml>
    </head>
    <body>
        <div id="header">
            <h1 class="heading">2.2.3 Reporting Services</h1>
        </div>
        <div id="mainSection">
            <div id="mainBody">
                <div id="allHistory" class="saveHistory"></div>
                <div id="sectionSection0" class="section" name="collapseableSection">
                    

<p>The following protocols and formats are used by the
Reporting Services <a href="https://go.microsoft.com/fwlink/?LinkId=152499">[MSDN-SSRS]</a>.</p>

<table>
 <thead>
  <tr>
   <th>
   <p>Format</p>
   </th>
   <th>
   <p>Description</p>
   </th>
   <th>
   <p>Reference</p>
   </th>
  </tr>
 </thead>
 <tr>
  <td>
  <p>Report Definition Language file format</p>
  </td>
  <td>
  <p>SQL Server Report Definition Language (RDL) is a
  file type that is used to represent the metadata for defining a report.</p>
  </td>
  <td>
  <p><mshelp:link keywords="53287204-7cd0-4bc9-a5cd-d42a5925dca1" tabindex="0">[MS-RDL]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Report Page Layout (RPL) binary stream format</p>
  </td>
  <td>
  <p>RPL is a binary format that is used by SQL Server
  Reporting Services when it communicates with viewer controls to offload some
  of the rendering work from the server to the client viewer control. </p>
  <p>By using RPL, implementers can create custom report
  designers that will create RPL, as well as custom report renderers that
  process and display RPL to display reports.</p>
  </td>
  <td>
  <p><mshelp:link keywords="9c4ff7ba-f6da-4092-9670-aa0e54e73887" tabindex="0">[MS-RPL]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Remote GDI+ (RGDI) binary stream format</p>
  </td>
  <td>
  <p>RGDI is a binary format that is produced by SQL Server
  Reporting Services when it communicates with viewer controls to offload some
  of the rendering work from the server to the client viewer control.</p>
  <p>By using RGDI, the implementer can create custom
  report designers that will generate RGDI, and can create custom report
  renderers that process and display RGDI to display reports. A client control
  that consumes RGDI is required to translate RGDI content to GDI+ objects and
  calls. RGDI works with only one page of report data at a time; each page is
  represented by an RGDI stream.</p>
  </td>
  <td>
  <p><mshelp:link keywords="b420a652-10eb-49b2-834c-ebc4d31e8ce5" tabindex="0">[MS-RGDI]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Report Server Web Service for Report Management:
  ReportService2010</p>
  </td>
  <td>
  <p>This protocol is used for managing objects and
  settings on all <a href="20049766-3c6e-4f20-a20e-64785e88f6f2.htm#gt_cbdd3a12-e9ec-43e2-ac97-9c47f171f96a">report
  servers</a>, starting with Microsoft SQL Server 2008 R2.</p>
  </td>
  <td>
  <p><mshelp:link keywords="0c9864cf-afe9-4789-ae9e-a55df1ff9111" tabindex="0">[MS-RSWSRM2010]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Report Server Web Service for Report Management for
  SharePoint Mode: ReportService2006</p>
  </td>
  <td>
  <p>This protocol is used for managing objects and
  settings on a report server that is configured for SharePoint integrated
  mode.</p>
  </td>
  <td>
  <p><mshelp:link keywords="eea1faab-ab5f-4fac-aecd-5c7543a8977c" tabindex="0">[MS-RSWSRMSM2006]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Report Server Web Service for Report Execution:
  ReportExecution2005</p>
  </td>
  <td>
  <p>This API protocol is provided by the ReportService2005
  web service for managing objects and settings on a report server that is
  configured for SharePoint integrated mode.</p>
  </td>
  <td>
  <p><mshelp:link keywords="96c33524-52c1-4358-a23a-6921db74211c" tabindex="0">[MS-RSWSRE2005]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Report Server Web Service for Report Management Native
  Mode: ReportService2005</p>
  </td>
  <td>
  <p>This protocol is provided by the ReportService2005 web
  service for managing objects and settings on a report server that is
  configured for native integrated mode.</p>
  </td>
  <td>
  <p><mshelp:link keywords="a30e6fc4-36ad-423a-b578-ba50523f5a77" tabindex="0">[MS-RSWSRMNM2005]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Report Server Web Service for SharePoint Forms
  Authentication ReportServiceAuthentication</p>
  </td>
  <td>
  <p>This API protocol is provided by the ReportService2006
  web service for managing objects and settings on a report server that is
  configured for SharePoint integrated mode.</p>
  </td>
  <td>
  <p><mshelp:link keywords="ee081425-607f-4742-8d61-5bf61f0d2a26" tabindex="0">[MS-RSWSSFA]</mshelp:link></p>
  </td>
 </tr>
 <tr>
  <td>
  <p>Reporting Services REST API protocol</p>
  </td>
  <td>
  <p>This RESTful API specifies an HTTP-based web service
  API to manage objects and settings on a report server that is configured for
  native integrated mode.</p>
  </td>
  <td>
  <p><mshelp:link keywords="a7752484-e24a-41f8-8ea2-c0e6568768fd" tabindex="0">[MS-RSREST]</mshelp:link></p>
  </td>
 </tr>
</table>

<p> </p>


                </div>
            </div>
        </div>
    </body>
</html>