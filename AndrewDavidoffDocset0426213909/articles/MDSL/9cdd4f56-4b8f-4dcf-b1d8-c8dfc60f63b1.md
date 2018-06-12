<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip"><body><input type="hidden" id="userDataCache" class="userDataStyle"><input type="hidden" id="hiddenScrollOffset"><img id="dropDownImage" style="display:none; height:0; width:0;" src="../local/drpdown.gif"><img id="dropDownHoverImage" style="display:none; height:0; width:0;" src="../local/drpdown_orange.gif"><img id="collapseImage" style="display:none; height:0; width:0;" src="../local/collapse.gif"><img id="expandImage" style="display:none; height:0; width:0;" src="../local/exp.gif"><img id="collapseAllImage" style="display:none; height:0; width:0;" src="../local/collall.gif"><img id="expandAllImage" style="display:none; height:0; width:0;" src="../local/expall.gif"><img id="copyImage" style="display:none; height:0; width:0;" src="../local/copycode.gif"><img id="copyHoverImage" style="display:none; height:0; width:0;" src="../local/copycodeHighlight.gif"><div id="header"><h1 class="heading">2.2 Xaml Type Order</h1></div><div id="mainSection"><div id="mainBody"><div id="allHistory" class="saveHistory" onsave="saveAll()" onload="loadAll()"></div>
				<p xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
				</p>
			<div id="sectionSection0" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
				</content></div><div id="sectionSection1" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
					<p xmlns="">Xaml types in this specification are ordered in an alphabetical way. The WPF Xaml Vocabulary uses the [types assignable to] property in a way that corresponds to inheritance in object-oriented programming. On the row above each type name is a list of 'Base' types. On the row below each type name are types which directly 'inherit' from that type.</p>
					<p xmlns="">The following example shows the XamlType Information Items for the Fruit, Apple, and Banana types. </p>
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td colspan="2">
									<p> <b>Fruit</b></p>
								</td>
							</tr><tr>
							<td colspan="2">
								<p>
									<b>Fruit</b>
								</p>
							</td>
						</tr><tr>
							<td>
								<p> <b>Apple Banana</b></p>
							</td>
							<td>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(usage)</b>
								</p>
							</td>
							<td>
								<p>Value</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>...</b>
								</p>
							</td>
							<td>
								<p>...</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>property N</b>
								</p>
							</td>
							<td>
								<p>Value</p>
							</td>
						</tr></table>
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td colspan="2">
									<p> <b>Fruit</b><b>&gt; </b><b>Apple</b></p>
								</td>
							</tr><tr>
							<td colspan="2">
								<p>
									<b>Apple</b>
								</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(usage)</b>
								</p>
							</td>
							<td>
								<p>Value</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>...</b>
								</p>
							</td>
							<td>
								<p>...</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>property N</b>
								</p>
							</td>
							<td>
								<p>Value</p>
							</td>
						</tr></table>
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td colspan="2">
									<p> <b>Fruit</b><b>&gt; </b><b></b>Banana</p>
								</td>
							</tr><tr>
							<td colspan="2">
								<p>
									<b>Banana (4.5)</b>
								</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(usage)</b>
								</p>
							</td>
							<td>
								<p>Value</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>...</b>
								</p>
							</td>
							<td>
								<p>...</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>property N</b>
								</p>
							</td>
							<td>
								<p>Value</p>
							</td>
						</tr></table>
					<p xmlns="">Since this specification models typical object-oriented inheritance, a 'derived' type inherits all members from a 'base' type. This is not made explicit. For each type, only additional members are listed. The <a href="https://go.microsoft.com/fwlink/?linkid=845196" alt="" target="_blank"><linktext xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5">[MS-XAML]</linktext></a> specification does not require this inheritance-like style. In the Xaml Schema Information Set data model, each type lists its members exhaustively. Therefore, the correct interpretation of a type definition in this specification is that the corresponding XamlType Information Item's [members] property should include not just the listed members, but also all of the [members] of each type listed in its [types assignable to] property.</p>
					<p xmlns="">The "Banana" type, in the example above, has "(4.5)" listed after it to indicate that this type was introduced in this XAML Vocabulary's version 4.5 release. All types or members without a version number after it were released in versions previous to that.</p>
					<p xmlns="">XamlMember Information Items have numerous properties, and in this specification, members are more similar than they are different. So a notation is used to minimize redundancy. Some XamlMember Information Item properties may be omitted. Unless specified otherwise, the default values described in the following table apply.</p>
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td>
									<p>
										<b>Property</b>
									</p>
								</td>
								<td>
									<p>
										<b>Default Value</b>
									</p>
								</td>
							</tr><tr>
							<td>
								<p>
									<b>[text syntax]</b>
								</p>
							</td>
							<td>
								<p>Null</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is read only]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is static]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is attachable]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[target type]</b>
								</p>
							</td>
							<td>
								<p>Null </p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[allowed location]</b>
								</p>
							</td>
							<td>
								<p>Any</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is event]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is directive]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr></table>
					<p xmlns="">Members are not defined in distinct sections of this specification - they are listed inside their defining type following a row named (properties). This means that the [owner type] member defined by <a href="https://go.microsoft.com/fwlink/?linkid=845196" alt="" target="_blank"><linktext xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5">[MS-XAML]</linktext></a> is never specified explicitly in this specification. The [owner type] is always the type in which the member definition appears. Likewise, the [members] property of the defining type is never explicitly defined - it always contains all of the members listed for that type. The [name] and [value type] are specified on the first line of the property description. This line may be followed by non-default values for other properties. The following example shows the XamlType Information Item for the Satsuma type, which defines a member named SegmentCount of type Int32.</p>
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td colspan="2">
									<p> <b>Fruit &gt; Satsuma</b></p>
								</td>
							</tr><tr>
							<td colspan="2">
								<p>
									<b>Satsuma</b>
								</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(usage)</b>
								</p>
							</td>
							<td>
								<p>&lt;Satsuma /&gt;</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(description)</b>
								</p>
							</td>
							<td>
								<p>Specifies a small, orange citrus fruit.</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(properties)</b>
								</p>
							</td>
							<td>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>SegmentCount</b>
								</p>
							</td>
							<td>
								<p>Int32</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(description)</b>
								</p>
							</td>
							<td>
								<p>The number of segments in this satsuma.</p>
							</td>
						</tr></table>
					<p xmlns="">If all of the XamlMember Information Item properties had been listed in full for this property, it would look like the following table.</p>
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td>
									<p>
										<b>Property</b>
									</p>
								</td>
								<td>
									<p>
										<b>Value</b>
									</p>
								</td>
							</tr><tr>
							<td>
								<p>
									<b>[name]</b>
								</p>
							</td>
							<td>
								<p>SegmentCount</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[owner type]</b>
								</p>
							</td>
							<td>
								<p>Satsuma</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[value type]</b>
								</p>
							</td>
							<td>
								<p>Int32</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[text syntax]</b>
								</p>
							</td>
							<td>
								<p>Null</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is read only]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is static]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is attachable]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[target type]</b>
								</p>
							</td>
							<td>
								<p>Null</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[allowed location]</b>
								</p>
							</td>
							<td>
								<p>Any</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[is event]</b>
								</p>
							</td>
							<td>
								<p>False</p>
							</td>
						</tr></table>
					<p xmlns="">As with the type-level (description), the per-member (description) entries in this specification are non-normative.</p>
					<p xmlns="">XamlType Information Item descriptions in this document may contain up to three additional member categories: attachable members, event members, and static members. These three member categories have slightly different defaults, and are grouped separately in the type definitions for clarity. The conventions for these member categories are defined in the following sections.</p>
				</content></div><!--[if gte IE 5]>
			<tool:tip element="languageFilterToolTip" avoidmouse="false"/>
		<![endif]--></div><a name="feedback"></a><span></span></div></body></html>
