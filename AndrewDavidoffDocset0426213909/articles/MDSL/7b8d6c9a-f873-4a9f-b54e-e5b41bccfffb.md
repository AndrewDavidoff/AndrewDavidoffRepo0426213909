<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip"><body><input type="hidden" id="userDataCache" class="userDataStyle"><input type="hidden" id="hiddenScrollOffset"><img id="dropDownImage" style="display:none; height:0; width:0;" src="../local/drpdown.gif"><img id="dropDownHoverImage" style="display:none; height:0; width:0;" src="../local/drpdown_orange.gif"><img id="collapseImage" style="display:none; height:0; width:0;" src="../local/collapse.gif"><img id="expandImage" style="display:none; height:0; width:0;" src="../local/exp.gif"><img id="collapseAllImage" style="display:none; height:0; width:0;" src="../local/collall.gif"><img id="expandAllImage" style="display:none; height:0; width:0;" src="../local/expall.gif"><img id="copyImage" style="display:none; height:0; width:0;" src="../local/copycode.gif"><img id="copyHoverImage" style="display:none; height:0; width:0;" src="../local/copycodeHighlight.gif"><div id="header"><h1 class="heading">8.6.2.1 Notes (non-normative)</h1></div><div id="mainSection"><div id="mainBody"><div id="allHistory" class="saveHistory" onsave="saveAll()" onload="loadAll()"></div>




<p xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
<div id="sectionSection0" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
				</content></div><div id="sectionSection1" class="section" name="collapseableSection"><content xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:wsd="http://wsdev.schemas.microsoft.com/authoring/2008/2" xmlns:msxsl="urn:schemas-microsoft-com:xslt" xmlns:script="urn:script" xmlns:build="urn:build">
					<p xmlns="">The content wrapping process can end up producing more than one content member. For example, consider the following XML:</p>
					<div id="code" xmlns=""><pre>&lt;MyObject&gt;
 Some content
 &lt;MyObject.Prop&gt;BarValue&lt;/MyObject.Prop&gt;
 More content
&lt;/MyObject&gt;</pre></div>
					<p xmlns="">If &lt;MyObject&gt; represents an object node, its [member nodes] will contain two content nodes, one representing each piece of text. The well-formedness rules in section <mshelp:link keywords="777958b9-a118-4747-94cf-6f138abc56ef" tabindex="0">6</mshelp:link> require that Xaml processors identify this as an error--a <mshelp:link keywords="777958b9-a118-4747-94cf-6f138abc56ef" tabindex="0">Xaml Information Set</mshelp:link> is not well formed if an object node contains two member nodes with the same <mshelp:link keywords="5fe76f94-9868-41b2-a117-c1a62071e64d" tabindex="0">XamlMember Information Item</mshelp:link>. (See <mshelp:link keywords="a088ee7a-9a27-4569-9f44-99b5001e71d1" tabindex="0">6.2.1.3</mshelp:link>.) However, for some applications (e.g. Xaml editors) it may be useful to carry on document processing even when a document is known not to be valid. The example XML shown above is conceptually equivalent to this:</p>
					<div id="code" xmlns=""><pre>&lt;MyObject&gt;
 &lt;MyObject.Content&gt;
 Some content
 &lt;/MyObject.Content&gt;
 &lt;MyObject.Prop&gt;BarValue&lt;/MyObject.Prop&gt;
 &lt;MyObject.Content&gt;
 More content
 &lt;/MyObject.Content&gt;
&lt;/MyObject &gt;</pre></div>
					<p xmlns="">Where 'Content' is MyObject's content member. This makes it more obvious why this is not considered well-formed Xaml. The error is the same in both cases - the same member appearing twice in one element. The only difference in the first example is that the content member has not been spelled out as a member element.</p>
				</content></div><!--[if gte IE 5]>
			<tool:tip element="languageFilterToolTip" avoidmouse="false"/>
		<![endif]--></div><a name="feedback"></a><span></span></div></body></html>
