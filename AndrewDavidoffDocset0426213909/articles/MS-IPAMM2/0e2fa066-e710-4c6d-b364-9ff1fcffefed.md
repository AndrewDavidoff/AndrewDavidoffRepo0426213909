<html dir="LTR" xmlns:mshelp="http://msdn.microsoft.com/mshelp" xmlns:ddue="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:tool="http://www.microsoft.com/tooltip">
 <body>
 <div id="header">
 <h1 class="heading">2.2.4.91 DeleteDhcpReservationCollectionParameters</h1>
 </div>
 <div id="mainSection">
 <div id="mainBody">
 <div id="allHistory" class="saveHistory"></div>
 <div id="sectionSection0" class="section" name="collapseableSection">
 

<p>This complex type allows extended attributes on an
IpamOperationWithProgressParameters type (section <a href="99fc6063-33f2-47ef-8db7-91d89369e3dc.md">2.2.4.286</a>). It creates
objects whose OperationId is DeleteDhcpReservationCollection. It identifies a
collection of DHCP reservations to be deleted and the post processing to be
done after deleting them, such as deleting associated DNS resource record.</p>

<dl>
<dd>
<div><pre> &lt;xs:complexType name=&quot;DeleteDhcpReservationCollectionParameters&quot;&gt;
   &lt;xs:complexContent mixed=&quot;false&quot;&gt;
     &lt;xs:extension base=&quot;ipam:IpamOperationWithProgressParameters&quot;&gt;
       &lt;xs:sequence&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Family&quot; type=&quot;syssock:AddressFamily&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;Flag&quot; type=&quot;ipam:DhcpReservationDeletionFlag&quot; /&gt;
         &lt;xs:element minOccurs=&quot;0&quot; name=&quot;ReservationRecordIds&quot; nillable=&quot;true&quot; type=&quot;serarr:ArrayOflong&quot; /&gt;
       &lt;/xs:sequence&gt;
     &lt;/xs:extension&gt;
   &lt;/xs:complexContent&gt;
 &lt;/xs:complexType&gt;
</pre></div>
</dd></dl>

<p><b>Family</b>: Specifies the address family of the
DHCP reservation instances to be deleted.</p>

<p><b>Flag:</b> A DhcpReservationDeletionFlag (section <a href="b75720f2-1afa-4f26-80f6-b471a55455ff.md">2.2.5.30</a>) that determines
the cleanup needed after the deletion of a reservation, such as the removal of
associated DNS resource records.</p>

<p><b>ReservationRecordIds:</b> A serarr:ArrayOflong
(section <a href="36dc2842-4920-4284-a94d-ab519731bb99.md">2.2.4.379</a>)
that represents the identifiers of DHCP reservations to be deleted.</p>


 </div>
 </div>
 </div>
 </body>
</html>