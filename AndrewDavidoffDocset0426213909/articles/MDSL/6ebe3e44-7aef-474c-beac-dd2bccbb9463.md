<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">

<body>
 <input type="hidden" id="userDataCache" class="userDataStyle">
 <input type="hidden" id="hiddenScrollOffset">
 <img id="dropDownImage" style="display:none; height:0; width:0;" src="../local/drpdown.gif">
 <img id="dropDownHoverImage" style="display:none; height:0; width:0;" src="../local/drpdown_orange.gif">
 <img id="collapseImage" style="display:none; height:0; width:0;" src="../local/collapse.gif">
 <img id="expandImage" style="display:none; height:0; width:0;" src="../local/exp.gif">
 <img id="collapseAllImage" style="display:none; height:0; width:0;" src="../local/collall.gif">
 <img id="expandAllImage" style="display:none; height:0; width:0;" src="../local/expall.gif">
 <img id="copyImage" style="display:none; height:0; width:0;" src="../local/copycode.gif">
 <img id="copyHoverImage" style="display:none; height:0; width:0;" src="../local/copycodeHighlight.gif">
 <div id="header"><h1 class="heading">6.68 FontFamilySyntax</h1></div>

 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory" onsave="saveAll()" onload="loadAll()"></div>
 <p xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
 </p>
 <div id="sectionSection0" class="section" name="collapseableSection">
 <content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
 </content>
 </div>
 <div id="sectionSection1" class="section" name="collapseableSection">
 <content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
 <table class="ProtocolAuthoredTable" xmlns="">
 <tr><td colspan="2">
 <b>FontFamilySyntax</b> </td>
 </tr>
 <tr><td><div class="indent0">[patterns]</div></td>
 <td></td>
 </tr>
 <tr><td><div class="indent2">.*</div></td>
 <td>A sequence of comma-separated font family names. Each name can optionally start with a string indicating the location of the font file. This optional location specifier is indicated by a # symbol – the part before the hash is the location and the part after the hash is the family name. The absence of a # indicates that only the family name is specified. (The regular expression does not reflect this, because there are no restrictions on what text appears as the font name other than that it must not contain a ‘#’ or a ‘,’ and since those are both allowed as delimiters, there are no syntactic limits on the string. Of course whether the string is meaningful in practice depends on whether the specified font is available.)</td>
 </tr>
 <tr><td><div class="indent4">[is case sensitive]</div></td>
 <td>true</td>
 </tr>
</table>
 </content>
 </div>
 <!--[if gte IE 5]>
 <tool:tip element="languageFilterToolTip" avoidmouse="false"/>
 <![endif]-->
 </div>
 <a name="feedback"></a><span></span>
 </div>
</body></html>
