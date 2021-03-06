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
 <div id="header"><h1 class="heading">4.128 ContentElement</h1></div>

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
<mshelp:link keywords="c0d383e4-fcdb-4546-a06b-81c262fe2a5e" tabindex="0">x:Object</mshelp:link> &gt; <mshelp:link keywords="44a6e58f-41e0-4602-b1d2-75a9b44a5acb" tabindex="0">DependencyObject</mshelp:link> &gt; <mshelp:link keywords="ecc4db98-a5ea-42ce-bca0-6f522aed9927" tabindex="0">ContentElement</mshelp:link>, <mshelp:link keywords="1ee43d58-7eb2-43cc-a23e-03101c2a1ef0" tabindex="0">IInputElement</mshelp:link> </td>
 </tr>
 <tr><td colspan="2">
 <b>ContentElement</b> </td>
 </tr>
 <tr><td colspan="2">
<mshelp:link keywords="14ba4981-b257-4962-8578-9a034636a1a6" tabindex="0">FrameworkContentElement</mshelp:link> </td>
 </tr>
 <tr><td><div class="indent0">(usage)</div></td>
 <td>&lt;ContentElement /&gt;</td>
 </tr>
 <tr><td><div class="indent0">(description)</div></td>
 <td>Provides a core-level base type for content elements. Content elements are designed for flow-style presentation, using an intuitive markup-oriented layout model and a deliberately simple object model.</td>
 </tr>
 <tr><td><div class="indent0">(properties)</div></td>
 <td></td>
 </tr>
 <tr><td><div class="indent2">AllowDrop</div></td>
 <td><mshelp:link keywords="c4ef5482-3a69-411e-bd77-93ce44c968a9" tabindex="0">x:Boolean</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A value that indicates whether this element can be used as the target of a drag-and-drop operation.</td>
 </tr>
 <tr><td><div class="indent2">CommandBindings</div></td>
 <td><mshelp:link keywords="5817ed49-f2a6-41ce-985c-0871848f58b9" tabindex="0">CommandBindingCollection</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A collection of CommandBinding objects that are associated with this element.</td>
 </tr>
 <tr><td><div class="indent4">[read only]</div></td>
 <td>true</td>
 </tr>
 <tr><td><div class="indent2">Focusable</div></td>
 <td><mshelp:link keywords="c4ef5482-3a69-411e-bd77-93ce44c968a9" tabindex="0">x:Boolean</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A value that indicates whether the element can receive focus.</td>
 </tr>
 <tr><td><div class="indent2">InputBindings</div></td>
 <td><mshelp:link keywords="381b602a-1409-4efc-9269-b86fe49dea96" tabindex="0">InputBindingCollection</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>The collection of input bindings that are associated with this element.</td>
 </tr>
 <tr><td><div class="indent4">[read only]</div></td>
 <td>true</td>
 </tr>
 <tr><td><div class="indent2">IsEnabled</div></td>
 <td><mshelp:link keywords="c4ef5482-3a69-411e-bd77-93ce44c968a9" tabindex="0">x:Boolean</mshelp:link></td>
 </tr>
 <tr><td><div class="indent4">(description)</div></td>
 <td>A value that indicates whether this element is enabled in the user interface (UI).</td>
 </tr>
 <tr><td><div class="indent0">(events)</div></td>
 <td></td>
 </tr>
 <tr><td><div class="indent2">DragEnter</div></td>
 <td>Occurs when the input system reports an underlying drag event with this element as the drag target.</td>
 </tr>
 <tr><td><div class="indent2">DragLeave</div></td>
 <td>Occurs when the input system reports an underlying drag event with this element as the drag origin.</td>
 </tr>
 <tr><td><div class="indent2">DragOver</div></td>
 <td>Occurs when the input system reports an underlying drag event with this element as the potential drop target.</td>
 </tr>
 <tr><td><div class="indent2">Drop</div></td>
 <td>Occurs when the input system reports an underlying drop event with this element as the drop target.</td>
 </tr>
 <tr><td><div class="indent2">FocusableChanged</div></td>
 <td>Occurs when the value of the Focusable property changes.</td>
 </tr>
 <tr><td><div class="indent2">GiveFeedback</div></td>
 <td>Occurs when the input system reports an underlying drag-and-drop event that involves this element.</td>
 </tr>
 <tr><td><div class="indent2">GotFocus</div></td>
 <td>Occurs when this element gets logical focus.</td>
 </tr>
 <tr><td><div class="indent2">GotKeyboardFocus</div></td>
 <td>Occurs when the keyboard is focused on this element.</td>
 </tr>
 <tr><td><div class="indent2">GotMouseCapture</div></td>
 <td>Occurs when this element captures the mouse.</td>
 </tr>
 <tr><td><div class="indent2">GotStylusCapture</div></td>
 <td>Occurs when this element captures the stylus.</td>
 </tr>
 <tr><td><div class="indent2">GotTouchCapture</div></td>
 <td>Occurs when a touch is captured to this element.</td>
 </tr>
 <tr><td><div class="indent2">IsEnabledChanged</div></td>
 <td>Occurs when the value of the IsEnabled property on this element changes.</td>
 </tr>
 <tr><td><div class="indent2">IsKeyboardFocusedChanged</div></td>
 <td>Occurs when the value of the IsKeyboardFocused property changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">IsKeyboardFocusWithinChanged</div></td>
 <td>Occurs when the value of the IsKeyboardFocusWithinChanged property changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">IsMouseCapturedChanged</div></td>
 <td>Occurs when the value of the IsMouseCaptured property changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">IsMouseCaptureWithinChanged</div></td>
 <td>Occurs when the value of the IsMouseCaptureWithinProperty changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">IsMouseDirectlyOverChanged</div></td>
 <td>Occurs when the value of the IsMouseDirectlyOver property changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">IsStylusCapturedChanged</div></td>
 <td>Occurs when the value of the IsStylusCaptured property changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">IsStylusCaptureWithinChanged</div></td>
 <td>Occurs when the value of the IsStylusCaptureWithin property changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">IsStylusDirectlyOverChanged</div></td>
 <td>Occurs when the value of the IsStylusDirectlyOver property changes on this element.</td>
 </tr>
 <tr><td><div class="indent2">KeyDown</div></td>
 <td>Occurs when a key is pressed while focus is on this element.</td>
 </tr>
 <tr><td><div class="indent2">KeyUp</div></td>
 <td>Occurs when a key is released while focus is on this element.</td>
 </tr>
 <tr><td><div class="indent2">LostFocus</div></td>
 <td>Occurs when this element loses logical focus.</td>
 </tr>
 <tr><td><div class="indent2">LostKeyboardFocus</div></td>
 <td>Occurs when the keyboard is no longer focused on this element.</td>
 </tr>
 <tr><td><div class="indent2">LostMouseCapture</div></td>
 <td>Occurs when this element loses mouse capture.</td>
 </tr>
 <tr><td><div class="indent2">LostStylusCapture</div></td>
 <td>Occurs when this element loses stylus capture.</td>
 </tr>
 <tr><td><div class="indent2">LostTouchCapture</div></td>
 <td>Occurs when this element loses a touch capture.</td>
 </tr>
 <tr><td><div class="indent2">MouseDown</div></td>
 <td>Occurs when any mouse button is pressed while the pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseEnter</div></td>
 <td>Occurs when the mouse pointer enters the bounds of this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseLeave</div></td>
 <td>Occurs when the mouse pointer leaves the bounds of this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseLeftButtonDown</div></td>
 <td>Occurs when the left mouse button is pressed while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseLeftButtonUp</div></td>
 <td>Occurs when the left mouse button is released while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseMove</div></td>
 <td>Occurs when the mouse pointer moves while over this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseRightButtonDown</div></td>
 <td>Occurs when the right mouse button is pressed while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseRightButtonUp</div></td>
 <td>Occurs when the right mouse button is released while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseUp</div></td>
 <td>Occurs when any mouse button is released over this element.</td>
 </tr>
 <tr><td><div class="indent2">MouseWheel</div></td>
 <td>Occurs when the user rotates the mouse wheel while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewDragEnter</div></td>
 <td>Occurs when the input system reports an underlying drag event with this element as the drag target.</td>
 </tr>
 <tr><td><div class="indent2">PreviewDragLeave</div></td>
 <td>Occurs when the input system reports an underlying drag event with this element as the drag origin.</td>
 </tr>
 <tr><td><div class="indent2">PreviewDragOver</div></td>
 <td>Occurs when the input system reports an underlying drag event with this element as the potential drop target.</td>
 </tr>
 <tr><td><div class="indent2">PreviewDrop</div></td>
 <td>Occurs when the input system reports an underlying drop event with this element as the drop target.</td>
 </tr>
 <tr><td><div class="indent2">PreviewGiveFeedback</div></td>
 <td>Occurs when a drag-and-drop operation is started.</td>
 </tr>
 <tr><td><div class="indent2">PreviewGotKeyboardFocus</div></td>
 <td>Occurs when the keyboard is focused on this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewKeyDown</div></td>
 <td>Occurs when a key is pressed while the keyboard is focused on this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewKeyUp</div></td>
 <td>Occurs when a key is released while the keyboard is focused on this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewLostKeyboardFocus</div></td>
 <td>Occurs when the keyboard is no longer focused on this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseDown</div></td>
 <td>Occurs when any mouse button is pressed while the pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseLeftButtonDown</div></td>
 <td>Occurs when the left mouse button is pressed while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseLeftButtonUp</div></td>
 <td>Occurs when the left mouse button is released while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseMove</div></td>
 <td>Occurs when the mouse pointer moves while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseRightButtonDown</div></td>
 <td>Occurs when the right mouse button is pressed while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseRightButtonUp</div></td>
 <td>Occurs when the right mouse button is released while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseUp</div></td>
 <td>Occurs when any mouse button is released while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewMouseWheel</div></td>
 <td>Occurs when the user rotates the mouse wheel while the mouse pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewQueryContinueDrag</div></td>
 <td>Occurs when there is a change in the keyboard or mouse button state during a drag-and-drop operation.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusButtonDown</div></td>
 <td>Occurs when the stylus button is pressed while the pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusButtonUp</div></td>
 <td>Occurs when the stylus button is released while the pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusDown</div></td>
 <td>Occurs when the stylus touches the digitizer while it is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusInAirMove</div></td>
 <td>Occurs when the stylus moves over an element without actually touching the digitizer.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusInRange</div></td>
 <td>Occurs when the stylus is close enough to the digitizer to be detected, while over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusMove</div></td>
 <td>Occurs when the stylus moves while over the element. The stylus must move while being detected by the digitizer to raise this event, otherwise, PreviewStylusInAirMove is raised instead.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusOutOfRange</div></td>
 <td>Occurs when the stylus is too far from the digitizer to be detected.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusSystemGesture</div></td>
 <td>Occurs when a user performs one of several stylus gestures.</td>
 </tr>
 <tr><td><div class="indent2">PreviewStylusUp</div></td>
 <td>Occurs when the user raises the stylus off the digitizer while the stylus is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewTextInput</div></td>
 <td>Occurs when this element gets text in a device-independent manner.</td>
 </tr>
 <tr><td><div class="indent2">PreviewTouchDown</div></td>
 <td>Occurs when a finger touches the screen while the finger is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewTouchMove</div></td>
 <td>Occurs when a finger moves on the screen while the finger is over this element.</td>
 </tr>
 <tr><td><div class="indent2">PreviewTouchUp</div></td>
 <td>Occurs when a finger is raised off of the screen while the finger is over this element.</td>
 </tr>
 <tr><td><div class="indent2">QueryContinueDrag</div></td>
 <td>Occurs when there is a change in the keyboard or mouse button state during a drag-and-drop operation.</td>
 </tr>
 <tr><td><div class="indent2">QueryCursor</div></td>
 <td>Occurs when the cursor is requested to display. This event is raised on an element each time that the mouse pointer moves to a new location, which means the cursor object might need to be changed based on its new position.</td>
 </tr>
 <tr><td><div class="indent2">StylusButtonDown</div></td>
 <td>Occurs when the stylus button is pressed while the pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">StylusButtonUp</div></td>
 <td>Occurs when the stylus button is released while the pointer is over this element.</td>
 </tr>
 <tr><td><div class="indent2">StylusDown</div></td>
 <td>Occurs when the stylus touches the digitizer while the stylus is over this element.</td>
 </tr>
 <tr><td><div class="indent2">StylusEnter</div></td>
 <td>Occurs when the stylus enters the bounds of this element.</td>
 </tr>
 <tr><td><div class="indent2">StylusInAirMove</div></td>
 <td>Occurs when the stylus moves over an element without actually touching the digitizer.</td>
 </tr>
 <tr><td><div class="indent2">StylusInRange</div></td>
 <td>Occurs when the stylus is close enough to the digitizer to be detected, while over this element.</td>
 </tr>
 <tr><td><div class="indent2">StylusLeave</div></td>
 <td>Occurs when the stylus leaves the bounds of the element.</td>
 </tr>
 <tr><td><div class="indent2">StylusMove</div></td>
 <td>Occurs when the stylus moves over this element. The stylus must move while on the digitizer to raise this event. Otherwise, StylusInAirMove is raised instead.</td>
 </tr>
 <tr><td><div class="indent2">StylusOutOfRange</div></td>
 <td>Occurs when the stylus is too far from the digitizer to be detected, while over this element.</td>
 </tr>
 <tr><td><div class="indent2">StylusSystemGesture</div></td>
 <td>Occurs when a user performs one of several stylus gestures.</td>
 </tr>
 <tr><td><div class="indent2">StylusUp</div></td>
 <td>Occurs when the user raises the stylus off the digitizer while it is over this element.</td>
 </tr>
 <tr><td><div class="indent2">TextInput</div></td>
 <td>Occurs when this element gets text in a device-independent manner.</td>
 </tr>
 <tr><td><div class="indent2">TouchDown</div></td>
 <td>Occurs when a finger touches the screen while the finger is over this element.</td>
 </tr>
 <tr><td><div class="indent2">TouchEnter</div></td>
 <td>Occurs when a touch moves from outside to inside the bounds of this element.</td>
 </tr>
 <tr><td><div class="indent2">TouchLeave</div></td>
 <td>Occurs when a touch moves from inside to outside the bounds of this element.</td>
 </tr>
 <tr><td><div class="indent2">TouchMove</div></td>
 <td>Occurs when a finger moves on the screen while the finger is over this element.</td>
 </tr>
 <tr><td><div class="indent2">TouchUp</div></td>
 <td>Occurs when a finger is raised off of the screen while the finger is over this element.</td>
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
