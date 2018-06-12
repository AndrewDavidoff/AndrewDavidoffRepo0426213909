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
 <div id="header"><h1 class="heading">4.182 DatePicker</h1></div>

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
<mshelp:link keywords="86913f34-aa06-4c94-9f09-83936a822fd8" tabindex="0">x:Object</mshelp:link> &gt; <mshelp:link keywords="22a604a1-b593-4464-91e4-488285506428" tabindex="0">DependencyObject</mshelp:link> &gt; <mshelp:link keywords="d3c6fb79-d082-4257-aa16-84c18cbf6051" tabindex="0">Visual</mshelp:link> &gt; <mshelp:link keywords="ce2d5941-a755-4517-b5ac-e99658cd1dd1" tabindex="0">UIElement</mshelp:link> &gt; <mshelp:link keywords="07f9afc2-9f13-4a2a-871b-ac7caef0660d" tabindex="0">FrameworkElement</mshelp:link> &gt; <mshelp:link keywords="f9528c9b-edc4-4e4e-8947-e16edb07c1d6" tabindex="0">Control</mshelp:link> &gt; <mshelp:link keywords="7ed3be31-33e5-49ca-9c29-cfcf7fbfbf5b" tabindex="0">DatePicker</mshelp:link>, <mshelp:link keywords="fb286ef6-72e1-445b-8b74-effc6b5e1777" tabindex="0">IInputElement</mshelp:link> </td>
 </tr>
 <tr><td colspan="2">
 <b>
DatePicker </b>
 </td>
 </tr>
 <tr><td><div class="indent0">(usage)</div></td>
 <td>&lt;DatePicker /&gt; </td>
 </tr>
 <tr><td><div class="indent0">(description)</div></td>
 <td>Represents a control that allows the user to select a date. </td>
 </tr>
 <tr><td><div class="indent0">[name property]</div></td>
 <td><mshelp:link keywords="07f9afc2-9f13-4a2a-871b-ac7caef0660d" tabindex="0">Name</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent0">[xml lang property]</div></td>
 <td><mshelp:link keywords="07f9afc2-9f13-4a2a-871b-ac7caef0660d" tabindex="0">Language</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent0">(properties)</div></td>
 <td> </td>
 </tr>
 <tr><td><div class="indent2">BlackoutDates</div></td>
 <td><mshelp:link keywords="a83f575d-2cf7-435d-935e-f64953d7846f" tabindex="0">CalendarBlackoutDatesCollection</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A collection of dates that are marked as not selectable. </td>
 </tr>
 <tr><td><div class="indent4">[read only]</div></td>
 <td>true </td>
 </tr>
 <tr><td><div class="indent2">CalendarStyle</div></td>
 <td><mshelp:link keywords="474ac96a-e49a-4316-9ea8-7c05ffc4bf9e" tabindex="0">Style</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The style that is used when rendering the calendar. </td>
 </tr>
 <tr><td><div class="indent2">DisplayDate</div></td>
 <td><mshelp:link keywords="04863bd7-3e7c-49ec-b48a-82a6f2be343e" tabindex="0">x:DateTime</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The date to display. </td>
 </tr>
 <tr><td><div class="indent2">DisplayDateEnd</div></td>
 <td><mshelp:link keywords="a70e74f7-3de9-4ac0-9b2d-5c177c9b0aa5" tabindex="0">x:Nullable</mshelp:link>(<mshelp:link keywords="04863bd7-3e7c-49ec-b48a-82a6f2be343e" tabindex="0">x:DateTime</mshelp:link>) </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The last date to be displayed. </td>
 </tr>
 <tr><td><div class="indent2">DisplayDateStart</div></td>
 <td><mshelp:link keywords="a70e74f7-3de9-4ac0-9b2d-5c177c9b0aa5" tabindex="0">x:Nullable</mshelp:link>(<mshelp:link keywords="04863bd7-3e7c-49ec-b48a-82a6f2be343e" tabindex="0">x:DateTime</mshelp:link>) </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The first date to be displayed. </td>
 </tr>
 <tr><td><div class="indent2">FirstDayOfWeek</div></td>
 <td><mshelp:link keywords="262515c1-b3b9-4453-8d16-f465422c5f9f" tabindex="0">DayOfWeek</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The day that is considered the beginning of the week. </td>
 </tr>
 <tr><td><div class="indent2">IsDropDownOpen</div></td>
 <td><mshelp:link keywords="c179f5e8-f1d2-4665-a360-ea494307b744" tabindex="0">x:Boolean</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A value that indicates whether the drop-down Calendar is open or closed. </td>
 </tr>
 <tr><td><div class="indent2">IsTodayHighlighted</div></td>
 <td><mshelp:link keywords="c179f5e8-f1d2-4665-a360-ea494307b744" tabindex="0">x:Boolean</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A value that indicates whether the current date will be highlighted. </td>
 </tr>
 <tr><td><div class="indent2">SelectedDate</div></td>
 <td><mshelp:link keywords="a70e74f7-3de9-4ac0-9b2d-5c177c9b0aa5" tabindex="0">x:Nullable</mshelp:link>(<mshelp:link keywords="04863bd7-3e7c-49ec-b48a-82a6f2be343e" tabindex="0">x:DateTime</mshelp:link>) </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The currently selected date. </td>
 </tr>
 <tr><td><div class="indent2">SelectedDateFormat</div></td>
 <td><mshelp:link keywords="82d6a1f6-090b-4d1d-8f1f-fa3f7f88c7ff" tabindex="0">DatePickerFormat</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The format that is used to display the selected date. </td>
 </tr>
 <tr><td><div class="indent2">Text</div></td>
 <td><mshelp:link keywords="9defda5a-685e-4b5a-9b63-e97e2b4184ee" tabindex="0">x:String</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The text that is displayed by the DatePicker, or sets the selected date. </td>
 </tr>
 <tr><td><div class="indent0">(events)</div></td>
 <td> </td>
 </tr>
 <tr><td><div class="indent2">CalendarClosed</div></td>
 <td>Occurs when the drop-down Calendar is closed. </td>
 </tr>
 <tr><td><div class="indent2">CalendarOpened</div></td>
 <td>Occurs when the drop-down Calendar is opened. </td>
 </tr>
 <tr><td><div class="indent2">DateValidationError</div></td>
 <td>Occurs when Text is set to a value that cannot be interpreted as a date or when the date cannot be selected. </td>
 </tr>
 <tr><td><div class="indent2">SelectedDateChanged</div></td>
 <td>Occurs when the SelectedDate property is changed. </td>
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
