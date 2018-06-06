<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">3.1.1.1.29 ADM_Tasks</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This simple table models the persisted information related
to IPAM <a href="21b4a631-8f28-420f-822f-c5f879d5046e.md#gt_740b149e-e6b4-49f5-bc16-e03ff41def7f">tasks</a>. The
IpamTaskType specifies an identifier for each task supported by the IPAM
server. The way the tasks are implemented and controlled is
implementation-specific. However, the following information pertaining to tasks
is tracked. They are modeled on the same properties of TaskInfo, section <a href="94bc767a-ceda-44e7-88ca-7ce3db5565d7.md">2.2.4.442</a>.</p>

<ul><li><p><span><span> 
</span></span>LastRunTime</p>

</li><li><p><span><span> 
</span></span>NextRunTime</p>

</li><li><p><span><span> 
</span></span>State</p>

</li><li><p><span><span> 
</span></span>Status</p>

</li><li><p><span><span> 
</span></span>TaskType</p>

</li><li><p><span><span> 
</span></span>Triggers</p>

</li></ul><p>For each task, the RecurrenceDuration is maintained, which
specifies the recurrence at which the task executes.</p>


 </div>
 </div>
 </div>
 </body>
</html>