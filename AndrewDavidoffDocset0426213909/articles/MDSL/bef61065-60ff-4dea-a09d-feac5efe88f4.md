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
 <div id="header"><h1 class="heading">4.376 HierarchicalDataTemplate</h1></div>

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
<mshelp:link keywords="86913f34-aa06-4c94-9f09-83936a822fd8" tabindex="0">x:Object</mshelp:link> &gt; <mshelp:link keywords="083fab9c-f9de-44ca-ba32-1d07353f7eb4" tabindex="0">FrameworkTemplate</mshelp:link> &gt; <mshelp:link keywords="2ff20c66-01b1-4315-bbc2-f2c27c537e3b" tabindex="0">DataTemplate</mshelp:link> &gt; <mshelp:link keywords="bef61065-60ff-4dea-a09d-feac5efe88f4" tabindex="0">HierarchicalDataTemplate</mshelp:link> </td>
 </tr>
 <tr><td colspan="2">
 <b>
HierarchicalDataTemplate </b>
 </td>
 </tr>
 <tr><td><div class="indent0">(usage)</div></td>
 <td>&lt;HierarchicalDataTemplate&gt; <mshelp:link keywords="07f9afc2-9f13-4a2a-871b-ac7caef0660d" tabindex="0">FrameworkElement</mshelp:link> &lt;/HierarchicalDataTemplate&gt; </td>
 </tr>
 <tr><td><div class="indent0">(description)</div></td>
 <td>Represents a DataTemplate that supports HeaderedItemsControl, such as TreeViewItem or MenuItem. </td>
 </tr>
 <tr><td><div class="indent0">[content property]</div></td>
 <td><mshelp:link keywords="083fab9c-f9de-44ca-ba32-1d07353f7eb4" tabindex="0">Template</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent0">[dictionary key property]</div></td>
 <td><mshelp:link keywords="2ff20c66-01b1-4315-bbc2-f2c27c537e3b" tabindex="0">DataTemplateKey</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent0">[is name scope]</div></td>
 <td>true </td>
 </tr>
 <tr><td><div class="indent0">(properties)</div></td>
 <td> </td>
 </tr>
 <tr><td><div class="indent2">AlternationCount</div></td>
 <td><mshelp:link keywords="5bcc11cc-8a6e-48f4-b938-0b20495e99df" tabindex="0">x:Int32</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The number of alternating item containers for the child items. </td>
 </tr>
 <tr><td><div class="indent2">ItemBindingGroup</div></td>
 <td><mshelp:link keywords="675febc2-8709-4e5b-98bf-f8f9354c0caf" tabindex="0">BindingGroup</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The BindingGroup that is copied to each child item. </td>
 </tr>
 <tr><td><div class="indent2">ItemContainerStyle</div></td>
 <td><mshelp:link keywords="474ac96a-e49a-4316-9ea8-7c05ffc4bf9e" tabindex="0">Style</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The Style that is applied to the item container for each child item. </td>
 </tr>
 <tr><td><div class="indent2">ItemContainerStyleSelector</div></td>
 <td><mshelp:link keywords="7fdb73cc-7fb1-4dc7-bcfe-98387ef27b26" tabindex="0">StyleSelector</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>Custom style-selection logic for a style that can be applied to each item container. </td>
 </tr>
 <tr><td><div class="indent2">ItemsSource</div></td>
 <td><mshelp:link keywords="50a319aa-ed3a-4331-a03b-64dd09648349" tabindex="0">BindingBase</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The binding for this data template, which indicates where to find the collection that represents the next level in the data hierarchy. </td>
 </tr>
 <tr><td><div class="indent2">ItemStringFormat</div></td>
 <td><mshelp:link keywords="9defda5a-685e-4b5a-9b63-e97e2b4184ee" tabindex="0">x:String</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A composite string that specifies how to format the items in the next level in the data hierarchy if they are displayed as strings. </td>
 </tr>
 <tr><td><div class="indent2">ItemTemplate</div></td>
 <td><mshelp:link keywords="2ff20c66-01b1-4315-bbc2-f2c27c537e3b" tabindex="0">DataTemplate</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The DataTemplate to apply to the ItemTemplate property on a generated HeaderedItemsControl (such as a MenuItem or a TreeViewItem), to indicate how to display items from the next level in the data hierarchy. </td>
 </tr>
 <tr><td><div class="indent2">ItemTemplateSelector</div></td>
 <td><mshelp:link keywords="0e26fec0-45aa-4551-a552-94bfa5fe3299" tabindex="0">DataTemplateSelector</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The DataTemplateSelector to apply to the ItemTemplateSelector property on a generated HeaderedItemsControl (such as a MenuItem or a TreeViewItem), to indicate how to select a template to display items from the next level in the data hierarchy. </td>
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
