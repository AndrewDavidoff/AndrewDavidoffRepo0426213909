<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip"><body><input type="hidden" id="userDataCache" class="userDataStyle"><input type="hidden" id="hiddenScrollOffset"><img id="dropDownImage" style="display:none; height:0; width:0;" src="../local/drpdown.gif"><img id="dropDownHoverImage" style="display:none; height:0; width:0;" src="../local/drpdown_orange.gif"><img id="collapseImage" style="display:none; height:0; width:0;" src="../local/collapse.gif"><img id="expandImage" style="display:none; height:0; width:0;" src="../local/exp.gif"><img id="collapseAllImage" style="display:none; height:0; width:0;" src="../local/collall.gif"><img id="expandAllImage" style="display:none; height:0; width:0;" src="../local/expall.gif"><img id="copyImage" style="display:none; height:0; width:0;" src="../local/copycode.gif"><img id="copyHoverImage" style="display:none; height:0; width:0;" src="../local/copycodeHighlight.gif"><div id="header"><h1 class="heading">2.3 Xaml Members where [is attachable] is True</h1></div><div id="mainSection"><div id="mainBody"><div id="allHistory" class="saveHistory" onsave="saveAll()" onload="loadAll()"></div>




<p xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
<div id="sectionSection0" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
				</content></div><div id="sectionSection1" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
					<p xmlns="">A type that defines members whose [is attachable] property is True will list them in a section that begins with "(attachable properties)". The following FruitBowl type example defines a Children member for which the normal defaults apply. This FruitBowl type also defines an attachable member named ZIndex for which [is attachable] is True. (The other member defaults still apply for ZIndex.)</p>
					<p xmlns=""><b></b></p><table class="ProtocolAuthoredTable" xmlns=""><tr>
								<td colspan="2">
									<p>
										<b>Object &gt; Bowl(T) &gt; FruitBowl</b>
									</p>
								</td>
							</tr><tr>
							<td colspan="2">
								<p>
									<b>FruitBowl</b>
								</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(usage)</b>
								</p>
							</td>
							<td>
								<p>&lt;FruitBowl&gt;Fruit*&lt;/FruitBowl&gt;</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(description)</b>
								</p>
							</td>
							<td>
								<p>A container of fruit.</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[content property]</b>
								</p>
							</td>
							<td>
								<p>Children</p>
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
									<b>Children</b>
								</p>
							</td>
							<td>
								<p>FruitCollection</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(description)</b>
								</p>
							</td>
							<td>
								<p>The items of fruit</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>(attachable properties)</b>
								</p>
							</td>
							<td>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>FruitBowl.ZIndex</b>
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
								<p>Indicates how deeply buried within the fruit bowl a piece of fruit is.</p>
							</td>
						</tr><tr>
							<td>
								<p>
									<b>[target type]</b>
								</p>
							</td>
							<td>
								<p>Fruit</p>
							</td>
						</tr></table>
					<p xmlns="">The name for an attachable member is specified as <i>TypeName</i>.<i>MemberName</i>. This is a syntactical convention to make it clear that this is an attachable property, and to illustrate how the property will look in a Xaml document. The [name] property of the XamlMember Information Item will only contain the <i>MemberName</i> part (the part after the period).</p>
				</content></div><!--[if gte IE 5]>
			<tool:tip element="languageFilterToolTip" avoidmouse="false"/>
		<![endif]--></div><a name="feedback"></a><span></span></div></body></html>
