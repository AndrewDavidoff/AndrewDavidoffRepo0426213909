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
 <div id="header"><h1 class="heading">4.27 BindingGroup</h1></div>

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
<mshelp:link keywords="c0d383e4-fcdb-4546-a06b-81c262fe2a5e" tabindex="0">x:Object</mshelp:link> &gt; <mshelp:link keywords="44a6e58f-41e0-4602-b1d2-75a9b44a5acb" tabindex="0">DependencyObject</mshelp:link> &gt; <mshelp:link keywords="5ef2a58e-b1fe-48ae-9aed-cad06b82643d" tabindex="0">BindingGroup</mshelp:link> </td>
 </tr>
 <tr><td colspan="2">
 <b>BindingGroup</b> </td>
 </tr>
 <tr><td><div class="indent0">(usage)</div></td>
 <td>&lt;BindingGroup /&gt;</td>
 </tr>
 <tr><td><div class="indent0">(description)</div></td>
 <td>Contains a collection of bindings and ValidationRule objects that are used to validate an object.</td>
 </tr>
 <tr><td><div class="indent0">(used by)</div></td>
 <td><mshelp:link keywords="14ba4981-b257-4962-8578-9a034636a1a6" tabindex="0">FrameworkContentElement</mshelp:link> <mshelp:link keywords="f80d4df2-08f5-4cbb-9a5e-f99fab120062" tabindex="0">FrameworkElement</mshelp:link> <mshelp:link keywords="d437b7c0-e457-4c9d-ac97-3a37fa4dc79e" tabindex="0">HierarchicalDataTemplate</mshelp:link> <mshelp:link keywords="06423658-82ef-457d-8339-78b2b66582d5" tabindex="0">ItemsControl</mshelp:link></td>
 </tr>
 <tr><td><div class="indent0">(properties)</div></td>
 <td></td>
 </tr>
 <tr><td><div class="indent2">Items</div></td>
 <td><mshelp:link keywords="7a233194-66e5-4f96-9d64-3f9efa0be8a9" tabindex="0">IList</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The sources that are used by the Binding objects in the BindingGroup.</td>
 </tr>
 <tr><td><div class="indent4">[read only]</div></td>
 <td>true</td>
 </tr>
 <tr><td><div class="indent2">Name</div></td>
 <td><mshelp:link keywords="34869e25-9e8d-49b4-b204-87bf0cf447ae" tabindex="0">x:String</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The name that identifies the BindingGroup, which can be used to include and exclude Binding objects in the BindingGroup.</td>
 </tr>
 <tr><td><div class="indent2">NotifyOnValidationError</div></td>
 <td><mshelp:link keywords="c4ef5482-3a69-411e-bd77-93ce44c968a9" tabindex="0">x:Boolean</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>Whether the Error event occurs when the state of a ValidationRule changes.</td>
 </tr>
 <tr><td><div class="indent2">SharesProposedValues</div></td>
 <td><mshelp:link keywords="c4ef5482-3a69-411e-bd77-93ce44c968a9" tabindex="0">x:Boolean</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A value that indicates whether the BindingGroup reuses target values that have not been committed to the source.</td>
 </tr>
 <tr><td><div class="indent2">ValidatesOnNotifyDataError (4.5)</div></td>
 <td><mshelp:link keywords="c4ef5482-3a69-411e-bd77-93ce44c968a9" tabindex="0">x:Boolean</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A value that indicates whether to include the NotifyDataErrorValidationRule.</td>
 </tr>
 <tr><td><div class="indent2">ValidationRules</div></td>
 <td><mshelp:link keywords="eed85a21-7e81-4907-91cc-7d5b8c4fee2e" tabindex="0">Collection</mshelp:link>(<mshelp:link keywords="32679a18-549c-41d8-bbc1-bf16cbea25d6" tabindex="0">ValidationRule</mshelp:link>)</td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A collection of ValidationRule objects that validate the source objects in the BindingGroup.</td>
 </tr>
 <tr><td><div class="indent4">[read only]</div></td>
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
