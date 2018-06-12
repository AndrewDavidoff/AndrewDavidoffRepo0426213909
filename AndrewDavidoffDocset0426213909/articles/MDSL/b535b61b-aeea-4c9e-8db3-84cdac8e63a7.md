<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip"><body><input type="hidden" id="userDataCache" class="userDataStyle"><input type="hidden" id="hiddenScrollOffset"><img id="dropDownImage" style="display:none; height:0; width:0;" src="../local/drpdown.gif"><img id="dropDownHoverImage" style="display:none; height:0; width:0;" src="../local/drpdown_orange.gif"><img id="collapseImage" style="display:none; height:0; width:0;" src="../local/collapse.gif"><img id="expandImage" style="display:none; height:0; width:0;" src="../local/exp.gif"><img id="collapseAllImage" style="display:none; height:0; width:0;" src="../local/collall.gif"><img id="expandAllImage" style="display:none; height:0; width:0;" src="../local/expall.gif"><img id="copyImage" style="display:none; height:0; width:0;" src="../local/copycode.gif"><img id="copyHoverImage" style="display:none; height:0; width:0;" src="../local/copycodeHighlight.gif"><div id="header"><h1 class="heading">10.1.48.95.2.1.4.2.1 DocumentViewer</h1></div><div id="mainSection"><div id="mainBody"><div id="allHistory" class="saveHistory" onsave="saveAll()" onload="loadAll()"></div>
			<div id="sectionSection0" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
				</content></div><div id="sectionSection1" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td>
									<p>(usage)</p>
								</td>
								<td>
									<p>&lt;DocumentViewer&gt; IDocumentPaginatorSource &lt;/DocumentViewer&gt;</p>
								</td>
							</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>Represents a document viewing control that can host paginated FixedDocument content such as an XpsDocument.</p>
							</td>
						</tr><tr>
							<td>
								<p>[types assignable to]</p>
							</td>
							<td>
								<p>DocumentViewer DocumentViewerBase Control FrameworkElement UIElement Visual DependencyObject x:Object IInputElement</p>
							</td>
						</tr><tr>
							<td>
								<p>[content property]</p>
							</td>
							<td>
								<p>Document</p>
							</td>
						</tr><tr>
							<td>
								<p>[name property]</p>
							</td>
							<td>
								<p>Name</p>
							</td>
						</tr><tr>
							<td>
								<p>[xml lang property]</p>
							</td>
							<td>
								<p>Language</p>
							</td>
						</tr><tr>
							<td>
								<p>(properties)</p>
							</td>
							<td>
							</td>
						</tr><tr>
							<td>
								<p>HorizontalOffset</p>
							</td>
							<td>
								<p>x:Double</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The horizontal scroll position.</p>
							</td>
						</tr><tr>
							<td>
								<p>HorizontalPageSpacing</p>
							</td>
							<td>
								<p>x:Double</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The horizontal space between pages.</p>
							</td>
						</tr><tr>
							<td>
								<p>MaxPagesAcross</p>
							</td>
							<td>
								<p>x:Int32</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>A value defining the maximum number of page columns to display.</p>
							</td>
						</tr><tr>
							<td>
								<p>ShowPageBorders</p>
							</td>
							<td>
								<p>x:Boolean</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>A value that indicates whether drop-shadow page borders are displayed.</p>
							</td>
						</tr><tr>
							<td>
								<p>VerticalOffset</p>
							</td>
							<td>
								<p>x:Double</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The vertical scroll position.</p>
							</td>
						</tr><tr>
							<td>
								<p>VerticalPageSpacing</p>
							</td>
							<td>
								<p>x:Double</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The vertical spacing between displayed pages.</p>
							</td>
						</tr><tr>
							<td>
								<p>Zoom</p>
							</td>
							<td>
								<p>x:Double</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The document zoom percentage.</p>
							</td>
						</tr><tr>
							<td>
								<p>(static properties)</p>
							</td>
							<td>
							</td>
						</tr><tr>
							<td>
								<p>FitToHeightCommand</p>
							</td>
							<td>
								<p>RoutedUICommand</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The RoutedUICommand that performs the FitToHeight operation.</p>
							</td>
						</tr><tr>
							<td>
								<p>FitToMaxPagesAcrossCommand</p>
							</td>
							<td>
								<p>RoutedUICommand</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The RoutedUICommand that performs the MaxPagesAcross operation.</p>
							</td>
						</tr><tr>
							<td>
								<p>FitToWidthCommand</p>
							</td>
							<td>
								<p>RoutedUICommand</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The RoutedUICommand that performs the FitToWidth operation.</p>
							</td>
						</tr><tr>
							<td>
								<p>ViewThumbnailsCommand</p>
							</td>
							<td>
								<p>RoutedUICommand</p>
							</td>
						</tr><tr>
							<td>
								<p>(description)</p>
							</td>
							<td>
								<p>The RoutedUICommand that performs the ViewThumbnails operation.</p>
							</td>
						</tr></table>
				</content></div><!--[if gte IE 5]>
			<tool:tip element="languageFilterToolTip" avoidmouse="false"/>
		<![endif]--></div><a name="feedback"></a><span></span></div></body></html>