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
 <div id="header"><h1 class="heading">6.8 BindingModeSyntax</h1></div>

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
 <b>
BindingModeSyntax </b>
 </td>
 </tr>
 <tr><td><div class="indent0">[values]</div></td>
 <td> </td>
 </tr>
 <tr><td><div class="indent2">Default</div></td>
 <td>Uses the default Mode value of the binding target. The default value varies for each property. In general, user-editable control properties, such as those of text boxes and check boxes, default to two-way bindings, whereas most other properties default to one-way bindings. </td>
 </tr>
 <tr><td><div class="indent2">OneTime</div></td>
 <td>Updates the binding target when the application starts or when the data context changes. This type of binding is appropriate if you are using data where either a snapshot of the current state is appropriate to use or the data is truly static. This type of binding is also useful if you want to initialize your target property with some value from a source property and the data context is not known in advance. </td>
 </tr>
 <tr><td><div class="indent2">OneWay</div></td>
 <td>Updates the binding target property when the binding source changes. This type of binding is appropriate if the control being bound is implicitly read-only, such as a stock ticker. Or perhaps the target property has no control interface for making changes, such as a data-bound background color of a table. If there is no need to monitor the changes of the target property, the OneWay binding mode can be used instead of the TwoWay binding mode. </td>
 </tr>
 <tr><td><div class="indent2">OneWayToSource</div></td>
 <td>Updates the source property when the target property changes. </td>
 </tr>
 <tr><td><div class="indent2">TwoWay</div></td>
 <td>Causes changes to either the source property or the target property to automatically update the other. This type of binding is appropriate for editable forms or other fully-interactive UI scenarios. </td>
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
