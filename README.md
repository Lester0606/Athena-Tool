<!DOCTYPE html>
<html>
<head>
<title>NYNE Athena Tool</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/js/bootstrap.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.19/js/jquery.dataTables.js"></script>

<style>

body {
padding: 5px 30px;
background-image: linear-gradient(to bottom right, #3492eb, #a2ccf5, #3492eb);
background-size:auto;
background-position:cover;
}

.col-sm-6 {
min-width: 50%;
}

.col-sm-4 {
min-width: 33.3%;
}

#nextcall:hover {
  background-color: #db589e;
  color: white;
  border-color: #db589e;
}

#supernotes {
padding: 30px 50px  10px 50px;
}


.main-header {
color:#000;
font-family: "Times New Roman", Times, serif;
}

.navtab {
display: flex;
list-style: none;
justify-content: left;
padding-top: .5em;
background-image: linear-gradient(to right, #3d3d3d, #6b6b6b, #999999, #cfcfcf, #adadad, #6b6b6b, #3d3d3d );
border-top: 1px solid black;
border-right: 1px solid black;
border-top-right-radius:10px;
border-top-left-radius:10px;
}

.navtab ul {
margin-bottom: 0;
padding-left: 14px;
}


.navtab li {
float: left;
margin-left:-16px;
list-style-type: none;
}

.navtab li a {
 
  color:#fff;
  background:#404042;
  position:relative;
  display:inline-block;
  margin:0 22px;
  padding:6px 10px;
  border-radius:4px 4px 0 0;
  text-decoration: none;
  font-size: 1.2rem;
}

nav a:before,
nav a:after{
  content:" ";
  position: absolute;
  top:0;
  width: 23px;
  height: 100%;
  background-color: #404042;
}
nav a:before{
  border-radius: 16px 0 0 0;
  transform: skew(-16deg);
  left: -16px;
  border-left: 1px solid #000;
}
nav a:after{
  border-radius: 0 16px 0 0;
  transform: skew(16deg);
  right: -16px;
  border-right: 1px solid #000;
  z-index: 1;
}
nav li.active a{
  color:#777;
  background:#ededed;
  font-weight: bold;
}
nav li.active a:before,
nav li.active a:after{
  z-index: 1;
  background: #ededed;
}

center.phonedc {
  font-weight: bold;
  color: #ed5a5a;
}

h5 {
  font-weight: bold;
}

#menu3 h3 {
margin:0;
padding-bottom: 20px;
}

div#menu3.tab-pane.fade.active.in {
padding:30px;
}

#aim {
padding:0 50px 20px 50px;
}

.tab-content {
background-color: #ededed;
border-radius: 0 0 10px 10px;
border-left: solid 1px black;
border-right: solid 1px black;
border-bottom: solid 1px black;
padding: 5px 20px;
}


input {
width: 60%;
height: 7%;
font-size: 20px;
}

textarea {
width: 100%;
height: 180px;
font-size: 15px;
border-radius: 3px;
resize: vertical;
}

textarea#casetemp {
width: 100%;
height: 100px;
font-size: 15px;
border-radius: 8px;
resize: none;
margin:0;
}



b {
font-size: solid 16px;
}

.btntog {
width: auto;
height: 5%;
white-space: normal;
}
.form-group {
width:95%;
padding:1px;
margin-left: 10px;
font-size: 13px;
}
.form-control{
border:1px solid #cce0ed;
padding:1px;
margin-bottom:1px;
}

.tbody {
    display:block;
    height:450px;
    overflow:auto;
}
#tableWrap tr:nth-child(even) {
background-color: #f2dce0;
}
.error {
    border-color: red;
    position: relative;
    animation: shake .1s linear;
    animation-iteration-count: 3;
}

@keyframes shake {
    0% { left: -5px; }
    100% { right: -5px; }
}
.thead, .tbody .tr {
    display:table;
    width:100%;
    table-layout:fixed;/* even columns width , fix width of table too*/
}


.thead {
    width: calc( 100% - 1em )/* scrollbar is average 1em/16px width, remove it from thead width */
}
.btn-toolbar {
     margin-left: 0px;
}
.popup {
  position: relative;
  display: inline-block;
  cursor: pointer;
}

/* The actual popup (appears on center) */
.popup .popuptext {
  visibility: hidden;
  width: 160px;
  background-color: #555;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 8px 0;
  position: absolute;
  z-index: 1;
  bottom: 125%;
  left: 50%;
  margin-left: -80px;
}

/* Popup arrow */
.popup .popuptext::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: #555 transparent transparent transparent;
}

/* Toggle this class when clicking on the popup container (hide and show the popup) */
.popup .show {
  visibility: visible;
  -webkit-animation: fadeIn 0.5s;
  animation: fadeIn 0.5s
}

/* Add animation (fade in the popup) */
@-webkit-keyframes fadeIn {
  from {opacity: 0;}
  to {opacity: 1;}
}

@keyframes fadeIn {
  from {opacity: 0;}
  to {opacity:1 ;}
}


.main-header {
padding: 5px 5px;
margin-top: 7px;
color: #f4f4f4;
}


</style>

<header class="main-header">
<h1><center>NYNE Athena Tool</center></h1>
</header>
</head>


<body>

<nav class="navtab">
<ul>
<li class="active" id="tab1"><a data-toggle="tab" href="#menu1">NY Tools</a></li>
  <li id="tab2"><a data-toggle="tab" href="#menu2">NE Tools</a></li>
  <li id="tab3"><a data-toggle="tab" href="#menu3">PhoneBook</a></li>
  <li id="tab4"><a data-toggle="tab" href="#aim">AIM Guidelines</a></li>
  <li id="tab5"><a data-toggle="tab" href="#referral">Referral Guide</a></li>
  <li id="tab6"><a data-toggle="tab" href="#supernotes">Super Notes</a></li>
</ul>

</nav>

<!----------- New York Tab ----------------->
<div class="tab-content">
<div id="menu1" class="tab-pane fade in active row"  style="text-align:center; border-radius:5px;">
        <div class="col-sm-6" style="border:1px solid rgba(150, 150, 150, 1);  margin: 5px 30px 15px 30px; padding:5px; border-radius:5px;">
            <center><h5><b>Systems and Tools</b></h5></center>

<div class="col-sm-6">
    <center><h5><b>PreCertification</b></h5></center>
            <ul class="list-group">


<li  class="list-group-item list-group-item-action">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="CS90" data-target="#cs90" style="cursor:hand">CS90</a>
<!----Modal ----->
<div class="modal fade" id="cs90" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>CS90</b></h5>
      </div>
      <div class="modal-body">
      <b>Description:</b><br>
        Open in Computer. Type 'NY' in Searchbox in Main Menu.
      </div>
     <div class="modal-footer"></div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin: 7px 0px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="WCF" data-target="#wcfny" style="cursor:hand">WCF</a>
<!----Modal ----->
<div class="modal fade" id="wcfny" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>WCF</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a system where you view the fax sent by providers.
      <br><br>
      <b>Link:</b><br>
https://fnp8bpmprod.wellpoint.com/ENTBPM/
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://fnp8bpmprod.wellpoint.com/ENTBPM/','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="NY Hospital List" data-target="#nyhosp" style="cursor:hand">NY Hospital List</a>
<!----Modal ----->
<div class="modal fade" id="nyhosp" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>NY Hospital List</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a system where you view Hospital Name, Address and EPINs.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=45545648-4847-4766-a50a-3e922a41c06c&returnLabel=ACES Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Dny%2Bhospital%2Blist%26qType%3Dall%26objectStoreID%3D699f4118%2Df22e%2D41b2%2Dbab2%2Db06f7cf13249%26searchCollectionID%3D1c32a2de%2Daa58%2D43b3%2Dba11%2D543e35c541c5%26selectedCategories%3D%26sort%3Drelevance%26pagesize%3D15
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=45545648-4847-4766-a50a-3e922a41c06c&returnLabel=ACES Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Dny%2Bhospital%2Blist%26qType%3Dall%26objectStoreID%3D699f4118%2Df22e%2D41b2%2Dbab2%2Db06f7cf13249%26searchCollectionID%3D1c32a2de%2Daa58%2D43b3%2Dba11%2D543e35c541c5%26selectedCategories%3D%26sort%3Drelevance%26pagesize%3D15','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
   </ul>
</div>
<div class="col-sm-6">
   <center><h5><b>PreDetermination</b></h5></center>
   <ul class="list-group">

    <li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="ACMS UM - Intake" data-target="#ompta" style="cursor:hand">OMPTA</a>
<!----Modal ----->
<div class="modal fade" id="ompta" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>OMPTA</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is the for researching MPs and CGs for CPT codes for PreD.
      <br><br>
      <b>Link:</b><br>
https://pulse.antheminc.com/webcenter/portal/medpolicy/pages_searchresults?medPolFilter=guideline%2Cpolicy%2C&query=
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://pulse.antheminc.com/webcenter/portal/medpolicy/pages_searchresults?medPolFilter=guideline%2Cpolicy%2C&query=','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>

<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="ACMS UM - Intake" data-target="#cg" style="cursor:hand">Clinical Guideline</a>
<!----Modal ----->
<div class="modal fade" id="cg" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Clinical Guideline</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is the for researching CGs if it is for PreD.
      <br><br>
      <b>Link:</b><br>
https://www.empireblue.com/medicalpolicies/noapplication/f3/s0/t0/pw_ad089438.pdf?refer=ehpproviderhttps://www.empireblue.com/medicalpolicies/noapplication/f3/s0/t0/pw_ad089438.pdf?refer=ehpprovider
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://www.empireblue.com/medicalpolicies/noapplication/f3/s0/t0/pw_ad089438.pdf?refer=ehpproviderhttps://www.empireblue.com/medicalpolicies/noapplication/f3/s0/t0/pw_ad089438.pdf?refer=ehpprovider','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="Clinical Criteria" data-target="#cc" style="cursor:hand">Clinical Criteria</a>
<!----Modal ----->
<div class="modal fade" id="cc" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Clinical Criteria</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is the for researching PreD for injectibles.
      <br><br>
      <b>Link:</b><br>
https://www11.empireblue.com/pharmacyinformation/clinicalcriteria.html
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://www11.empireblue.com/pharmacyinformation/clinicalcriteria.html','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="OBIS" data-target="#obis" style="cursor:hand">OBIS</a>
<!----Modal ----->
<div class="modal fade" id="obis" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>OBIS</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This tool helps in researching for NY member's Medical Management benefits.
      <br><br>
      <b>Link:</b><br>
https://intranet.empireblue.com/obis/Logon.do
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://intranet.empireblue.com/obis/Logon.do','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
   </ul>
</div>
</div>
<div class="col-sm-5" style="border:1px solid rgba(150, 150, 150, 1);  margin: 5px 0 15px 5px; padding:5px; border-radius:10px;">
            <center><h5><b>Documents and Guides</b></h5></center>
<div class="col-sm-6">
   <ul class="list-group">
    <li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="ACMS UM - Intake" data-target="#nycase" style="cursor:hand">Case Set Up Keys</a>
<!----Modal ----->
<div class="modal fade" id="nycase" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Case Set Up Keys</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        Helps you in creating case for New York Region.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=202adb5f-5e4b-441c-b149-ecb2256ae7fb&returnLabel=ACES Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Dcase%2Bset%2Bup%2Bkeys%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=202adb5f-5e4b-441c-b149-ecb2256ae7fb&returnLabel=ACES Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Dcase%2Bset%2Bup%2Bkeys%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="AIM Groupers List 2020" data-target="#nasco" style="cursor:hand">AIM Groupers List 2020</a>
<!----Modal ----->
<div class="modal fade" id="nasco" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>AIM Groupers List 2020</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a list of codes handled by AIM.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/FileDetail.cfm?objectid=67d84eb1-79a4-46c6-9fcf-27a8daa5cb13&returnLabel=Knowledge%20Library%20Search&returnUrl=%2Fhome%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Daim%2Bgroupers%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/FileDetail.cfm?objectid=67d84eb1-79a4-46c6-9fcf-27a8daa5cb13&returnLabel=Knowledge%20Library%20Search&returnUrl=%2Fhome%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Daim%2Bgroupers%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="Srx/CPT Groupers List" data-target="#srx" style="cursor:hand">Srx/CPT Groupers List</a>
<!----Modal ----->
<div class="modal fade" id="srx" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Srx/CPT Groupers List</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        An excel file listing all Srx Codes and what to do with them.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/FileDetail.cfm?objectid=26216b28-7a74-4c0c-bb77-8632b5e79387&returnLabel=Operations%20Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3DcO0217312%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/FileDetail.cfm?objectid=26216b28-7a74-4c0c-bb77-8632b5e79387&returnLabel=Operations%20Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3DcO0217312%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
</ul></div>
<div class="col-sm-6">
<ul class="list-group">
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="What Do I Do NY Local" data-target="#nydocode" style="cursor:hand">What Do I Do NY Local</a>
<!----Modal ----->
<div class="modal fade" id="nydocode" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>What Do I Do NY Local</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        A guide to dealing with NY codes.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=53a10bf0-037a-45c9-8410-a132b02a0897&returnLabel=Training&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255F
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=53a10bf0-037a-45c9-8410-a132b02a0897&returnLabel=Training&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255F','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="Determining Predetermination Reviews" data-target="#DET" style="cursor:hand">Determining Predetermination Reviews</a>
<!----Modal ----->
<div class="modal fade" id="DET" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Determining Predetermination Reviews</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        A guide for determining PreD for NY.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=caa05ee9-46e7-4f44-bae4-f1e97a57cd11&returnLabel=Pre-D&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255FCom
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=caa05ee9-46e7-4f44-bae4-f1e97a57cd11&returnLabel=Pre-D&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255FCom','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
   </ul>
</div>
</div>
  </div>
<!----------- North East Tab ----------------->
  <div id="menu2" class="tab-pane fade row" style="text-align:center; border-radius:5px;">
  <div class="col-sm-6" style="border:1px solid rgba(150, 150, 150, 1);  margin: 5px 30px 15px 30px; padding:5px; border-radius:5px;">
            <center><h5><b>Systems</b></h5></center>
<div class="col-sm-6">
            <ul class="list-group">

<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="ACES" data-target="#acES" style="cursor:hand">ACES</a>
<!----Modal ----->
<div class="modal fade" id="acES" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>ACES</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is the tool for researching PreC in NE Region.
      <br><br>
      <b>Link:</b>
https://eshare.antheminc.com/home/sites/operations/search.cfm?qCollection=aces&q=&advancedSearch=false&sort=relevance&pagesize=15&qTitle=NO&qType=all
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/operations/search.cfm?qCollection=aces&q=&advancedSearch=false&sort=relevance&pagesize=15&qTitle=NO&qType=all','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="mcw" data-target="#CCB" style="cursor:hand">Call Care Browser(CCB)</a>
<!----Modal ----->
<div class="modal fade" id="CCB" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Call Care Browser(CCB) - WGS</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a system for checking benefits, eligibility, and coverage.
      <br><br>
      <b>Link:</b><br>
https://callcare.wellpoint.com/ccb-wgs/login.asp
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://callcare.wellpoint.com/ccb-wgs/login.asp','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="mcw" data-target="#finddoc" style="cursor:hand">Find a Doctor/Facility(NE)</a>
<!----Modal ----->
<div class="modal fade" id="finddoc" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Find a Doctor/Facility(NE)</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a website for checking participation of providers and facilities. Works well with cross-border referral.
      <br><br>
      <b>Link:</b><br>https://www.anthem.com/find-doctor/?cnslocale=en_US_nh&dplid=sso.dpl.providerdirectory.search-criteria
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://www.anthem.com/find-doctor/?cnslocale=en_US_nh&dplid=sso.dpl.providerdirectory.search-criteria','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="mcw" data-target="#finddocma" style="cursor:hand">BCBS MA Provider Lookup(NEHP ONLY)</a>
<!----Modal ----->
<div class="modal fade" id="finddocma" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>BCBS MA Provider Lookup (NEHP ONLY)</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a website for checking participation of providers and facilities. Works well with cross-border referral.
      <br><br>
      <b>Link:</b><br>https://myfindadoctor.bluecrossma.com/
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://myfindadoctor.bluecrossma.com/','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
</ul></div>
<div class="col-sm-6">
<ul class="list-group">
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="mcw" data-target="#mcw" style="cursor:hand">MCW</a>
<!----Modal ----->
<div class="modal fade" id="mcw" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>MCW</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a system where you can check the benefits of the member and the par provider.
      <br><br>
      <b>Link:</b><br>
https://mcwprod.corp.anthem.com/jsp/McwLogin.jsp
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://mcwprod.corp.anthem.com/jsp/McwLogin.jsp','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="mcw" data-target="#nic" style="cursor:hand">NIC</a>
<!----Modal ----->
<div class="modal fade" id="nic" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>NIC</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a system where you can check the plan of the members under employer.
      <br><br>
      <b>Link:</b><br>
https://collaborate.wellpoint.com/sites/nic/Benefit%20Plan%20Designs/Forms/AC1.aspx
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://collaborate.wellpoint.com/sites/nic/Benefit%20Plan%20Designs/Forms/AC1.aspx','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="acesid" data-target="#acesid" style="cursor:hand">ACES ID</a>
<!----Modal ----->
<div class="modal fade" id="acesid" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>ACES ID</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is where you check the specific Hospital ID for NE local accounts.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=63b5495d-68f9-47d7-a80d-44fd2ff49c5b&returnLabel=ACES%20Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3D1SV0
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=63b5495d-68f9-47d7-a80d-44fd2ff49c5b&returnLabel=ACES%20Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3D1SV0','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="mcw" data-target="#wcf" style="cursor:hand">WCF</a>
<!----Modal ----->
<div class="modal fade" id="wcf" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>WCF</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a system where you view the fax sent by providers.
      <br><br>
      <b>Link:</b><br>
https://fnp8aeprod.wellpoint.com/CONTENTONLY/
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://fnp8aeprod.wellpoint.com/CONTENTONLY/','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
</ul>
</div>
</div>
<div class="col-sm-5" style="border:1px solid rgba(150, 150, 150, 1);  margin: 5px 0 15px 5px; padding:20px; border-radius:10px;">
            <center><h5><b>Documents and Guides</b></h5></center>
<div class="col-sm-6">
            <ul class="list-group">

   <li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="ACase Set Up Keys" data-target="#casene" style="cursor:hand">Case Set Up Keys</a>
<!----Modal ----->
<div class="modal fade" id="casene" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Case Set Up Keys</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is the tool to help you set up a case.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=a4caaccf-566c-4db2-b9d0-cbd6b613723e&returnLabel=ACES Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Dcase%2Bset%2Bup%2Bkeys%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/operations/sites/aces/FileDetail.cfm?objectid=a4caaccf-566c-4db2-b9d0-cbd6b613723e&returnLabel=ACES Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsites%2Faces%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Dcase%2Bset%2Bup%2Bkeys%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="Srx/CPT Groupers List" data-target="#nesrx" style="cursor:hand">Srx/CPT Groupers List</a>
<!----Modal ----->
<div class="modal fade" id="nesrx" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Srx/CPT Groupers List</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        An excel file listing all Srx Codes and what to do with them.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/FileDetail.cfm?objectid=26216b28-7a74-4c0c-bb77-8632b5e79387&returnLabel=Operations%20Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3DcO0217312%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/FileDetail.cfm?objectid=26216b28-7a74-4c0c-bb77-8632b5e79387&returnLabel=Operations%20Search&returnUrl=%2Fhome%2Fsites%2Foperations%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3DcO0217312%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="AIM Groupers List 2020" data-target="#aimg" style="cursor:hand">AIM Groupers List 2020</a>
<!----Modal ----->
<div class="modal fade" id="aimg" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>AIM Groupers List 2020</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a list of codes handled by AIM.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/FileDetail.cfm?objectid=67d84eb1-79a4-46c6-9fcf-27a8daa5cb13&returnLabel=Knowledge%20Library%20Search&returnUrl=%2Fhome%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Daim%2Bgroupers%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/FileDetail.cfm?objectid=67d84eb1-79a4-46c6-9fcf-27a8daa5cb13&returnLabel=Knowledge%20Library%20Search&returnUrl=%2Fhome%2Fsearch%2Ecfm%3FqCollection%3Desharehome%26q%3Daim%2Bgroupers%26advancedSearch%3Dfalse%26sort%3Drelevance%26pagesize%3D15%26qTitle%3DNO%26qType%3Dall','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="Case Note Template" data-target="#cnt" style="cursor:hand">Case Note Template</a>
<!----Modal ----->
<div class="modal fade" id="cnt" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>Case Note Template</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        A word document for note template.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=af6998a4-d8db-47af-9081-818f9f5f345f&returnLabel=C-D&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255FComme
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=af6998a4-d8db-47af-9081-818f9f5f345f&returnLabel=C-D&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255FComme','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
 <li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="PhoneBook" data-target="#phonebook" style="cursor:hand">PhoneBook</a>
<!----Modal ----->
<div class="modal fade" id="phonebook" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>PhoneBook</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is the tool to help you set up a case.
      <br><br>
      <b>Link:</b><br>
http://doc2share.wellpoint.com/Home/getObject.cfm?ObjectID=eaa30f22-587e-4757-b91d-9f82a153ca51
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('http://doc2share.wellpoint.com/Home/getObject.cfm?ObjectID=eaa30f22-587e-4757-b91d-9f82a153ca51','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
</ul>
</div>
<div class="col-sm-6">
            <ul class="list-group">
 <li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="NASCO" data-target="#nenasco" style="cursor:hand">NE Accounts on NASCO</a>
<!----Modal ----->
<div class="modal fade" id="nenasco" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>NE Accounts on NASCO</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is a list of account handled by NASCO.
      <br><br>
      <b>Link:</b><br>
Link is too long.
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=955561c5-5c4e-4f7c-8be5-92a14acb939d&returnLabel=M-N&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255FCommercial%255FUM%255FIntake%252FEnterprise%255FCommercial%255FUM%255FIntake%255FBookcase%252Ecfm%3Fobjectid%253Ddc253563%252D403f%252D479e%252D8809%252D264f9045428c%2526qtype%253Dall%2526titleonly%253Dfalse%2526sortdirection%253Dasc%2526rtnpagesize%253D10%2526ishtml%253Dfalse%2526advancedsearch%253Dfalse%2526sortcolumn%253DTitle%2526searchtype%253Dall%2526startfolderid%253Df2b767fe%252D0759%252D456a%252Dae0d%252D238acc39d167%2526rtnpage%253D1%2526pagesize%253D15%2526qtitle%253DNO%2526sort%253Drelevance%2526page%253D1%2526returnUrl%253D%25252Fhome%25252Fsites%25252Fchs%25252FPages%25252FAnthem%25255FCare%25255FManagement%25252FUtilization%25255FManagement%25252FEnterprise%25255FCommercial%25255FUM%25255FIntake%25252Findex%25252Ecfm','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="NEHP Referral Fact Sheet" data-target="#nehp" style="cursor:hand">NEHP Referral Fact Sheet</a>
<!----Modal ----->
<div class="modal fade" id="nehp" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>NEHP Referral Fact Sheet</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is fact document about NEHP Referral.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/FileDetail.cfm?objectid=e2f8bd4e-7d6d-4873-a3b0-7863f5b772a4&returnLabel=CHS/CHP
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/FileDetail.cfm?objectid=e2f8bd4e-7d6d-4873-a3b0-7863f5b772a4&returnLabel=CHS/CHP','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
<li class="list-group-item" style="margin-bottom: 7px;">
<!-----Link ---->
   <a data-toggle="modal" data-toggle="tooltip" title="NEHP Referral Fact Sheet" data-target="#docode" style="cursor:hand">What Do I Do with this Code</a>
<!----Modal ----->
<div class="modal fade" id="docode" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
       <h5><b>What Do I Do with this Code</b></h5>
      </div>
      <div class="modal-body" style="word-wrap: break-word;">
      <b>Description:</b><br>
        This is the document guide on what you can do about the codes for NE.
      <br><br>
      <b>Link:</b><br>
https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=70fdbf3e-5ce2-4008-8691-e84103253402&returnLabel=Training&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255F
      </div>
      <div class="modal-footer">
      <button type="button" class="btn btn-primary" onclick=" window.open('https://eshare.antheminc.com/home/sites/chs/filedetail.cfm?objectid=70fdbf3e-5ce2-4008-8691-e84103253402&returnLabel=Training&returnUrl=%252Fhome%252Fsites%252Fchs%252FPages%252FAnthem%255FCare%255FManagement%252FUtilization%255FManagement%252FEnterprise%255F','_blank')">Open Link</button>
     
       
      </div>
    </div>
  </div>
</div>
<!-------------------->
  </li>
</ul>
</div>
</div>
</div>

<!----------- AIM Tab ----------------->
  <div id="aim" class="tab-pane fade row" style ="border-radius:5px;">
        <center><h3>AIM Guidelines</h3></centeR> <hr>
<div class="col-sm-6" >
        <center><h4><u><strong>NE Region (Out-Patient)</strong></u></h4></centeR>  
<div class="row">
    <div class="col-sm-6">
      <h5>What Type of Services?</h5>
      <select class="form-control" onchange="selectAim();" style="width: 200px;" id="aimelem">
<option value=" "> </option>
        <option value="msk">MSK</option>
        <option value="gen">Genetic Testing</option>
        <option value="radcar">Radiology</option>
        <option value="upgi">Upper GI</option>
        <option value="drug">Injectable drugs</option>
      </select>
    </div>
    <div class="col-sm-6" id="sourcediv" style="display:none;">
      <h5>What can you see on the Source System?</h5>
      <h6 style="font-size:10px; color:blue">*Check on ACMS->Mem Info Tab the Source System.</h6>
      <select class="form-control" style="width: 200px;" id="source" onchange="selectSource()">
<option></option>
        <option value="star">STAR</option>
        <option value="wgs">WGS</option>
        <option value="nasco">NASCO</option>
<option value="aces">ACES</option>
      </select>
    </div>
<div class="col-sm-6" style="display:none;" id="excelgrp">
      <h5>Is it on AIM Groupers List/SRx List</h5>
      <select class="form-control" style="width: 200px;" id="excelgrp" onchange="selectExcelGrp()">
<option></option>
        <option value="yes">Yes</option>
        <option value="no">No</option>
      </select>
    </div>
   <div class="col-sm-6" style="display:none;" id="ftdiv">
      <h5>What is the Fund Type?</h5>
       <h6 style="font-size:10px; color:blue">*Check on ACMS->Mem Info Tab the Fund Type.</h6>
      <select class="form-control" style="width: 200px;" id="ft" onchange="selectft()">
<option></option>
        <option value="aso">ASO</option>
        <option value="fi">FI</option>
      </select>
    </div>
<div class="col-sm-6" style="display:none;" id="aimdiv">
      <h5>What can you see on AIM List?</h5>
       <h6 style="font-size:10px; color:blue">*Check on MCW->Click on the Subscriber's plan and search on AIM. Check on AIM Coverage</h6>
      <select class="form-control" style="width: 200px;" id="aimcov" onchange="selectAimCov()">
<option></option>
        <option value="umcm">UM / CM</option>
        <option value="na">NA</option>
      </select>
    </div>
<div class="col-sm-6" style="display:none;" id="groupdiv">
      <h5>Is it on AIM Groupers List / Anthem SRx List</h5>
       <h6 style="font-size:10px; color:blue">*Check on AIM Grouper's List / SRx List ->Search for the code. Is it on the list?</h6>
      <select class="form-control" style="width: 200px;" id="grouplist" onchange="selectgroup()">
<option></option>
        <option value="yes">Yes</option>
        <option value="no">No</option>
      </select>
    </div>
   </div><hr>

<div class="col-sm-12">
<center><button class="btn btn-secondary" onclick="clearalldiv()" id="btn">Reset</button></center>
<br><br>
<div clas="row container" style="border: 1px #4085b9 dashed; border-radius:5px; padding: 20px; margin-top: 50px">
<small>- Note: If caller confirms that AIM denied the initial request, we check the code and follow MP/CG guideline. If we need to load a case, document on the clinical and non-clinical summary that “Per caller, AIM denied the initial request.</small>
<br><br>
<small>- Please Pull up the AIM workflow excel file for complete workflow process (NY/NE).</small>
</div>

</div>
</div>
<div class="col-sm-6" style="padding:0 30px; border-left:1px solid rgba(220,220,220,1)">
<center><h4><u><strong>NY Region</u></strong></h4></centeR><br>  
<div class="row">
<p><b>1.</b> Check for the Codes on CS90.</p>
<p><b>2.</b> Check on MAD TAB for special instructions.</p>
<p><b>3.</b> If there is a special instruction in MAD TAB to refer to AIM, Check in AIM's Grouper's List</p>
<p><b>4.</b> If it is in AIM Grouper's List, Transfer to AIM. IF NOT, then do the usual research for PreC/PreD </p>
</div><br>
<div clas="row container" style="border: 1px #4085b9 dashed; border-radius:5px">
<center><h5><b><u><strong>Fully Insured</u></strong></b></h5><br>
<p><strong>Upper GI</strong> and <strong>MSK</strong> codes, automatically <strong>Transfer to AIM</strong><BR>
<small>How to check if it's Upper GI or MSK?</small>
<p>Check the codes in <i>CS90</i> for MSK and <i>Offshore List</i> for Upper GI.</p><br>
<center><h5><b><u><strong>ASO Plans</u></strong></b></h5>
<p>We manage: <u><strong>Out-Patient</strong></u> - Check<strong> CS90/Ompta</strong> | <u><strong>In-Patient</strong></u> - <strong>Create case and pend for review</strong>
</center>
</div>
</div>

  </div>
<!----------- NEHP Tab ----------------->
<div id="referral" class="tab-pane fade row"  style="margin: 1px -15px 1px -15px; padding: 10px; border-radius:5px;">
        <center><h3><u><strong>Referral Work Flow</u></strong></h3></centeR> <hr>
	<div class="col-sm-6" >
        <center><h4><u><strong>NE & NEHP Local</u></strong></h4></centeR>  
	<div class="row">
    <div class="col-sm-6">
      <h5>Are they calling from the PCP's Office?</h5>
      <select class="form-control" onchange="selectPcpoffices();" style="width: 200px;" id="pcpelem">
	<option></option>
        <option value="yes">Yes, calling from PCPs Office</option>
        <option value="no">No, Not from PCPs Office</option>
      </select>
    </div>
    <div class="col-sm-6" id="pcpsourcediv" style="display:none;">
      <h5>Is it the same as we have on acms or source system?</h5>
      <select class="form-control" style="width: 200px;" id="pcpsource" onchange="selectPcpsources();">
	<option></option>
        <option value="yes">Yes</option>
        <option value="no">No</option>
      </select>
    </div>
   <div class="col-sm-6" style="display:none;" id="umregiondiv">
      <h5>Is it a NE local or NEHP Account?</h5>
      <select class="form-control" style="width: 200px;" id="umregion" onchange="selectUmregion();">
	<option></option>
        <option value="nelocal">NE Local</option>
        <option value="nehplocal">NEHP Local</option>
      </select>
    </div>

   <div class="col-sm-6" style="display:none;" id="contractdiv">
      <h5>Does the PCPs contracting state was CT/NH/ME?</h5>
      <select class="form-control" style="width: 200px;" id="contract" onchange="selectContractstate()">
<option></option>
        <option value="yes">Yes</option>
        <option value="no">No</option>
      </select>
    </div>

<div class="col-sm-6" style="display:none;" id="mddiv">
      <h5>Where is the specialist location?</h5>
      <select class="form-control" style="width: 200px;" id="md" onchange="selectMdloc()">
<option></option>
        <option value="home">CT | NH | ME</option>
        <option value="host">MA | VT | RI | OTHER</option>
      </select>
    </div>

<div class="col-sm-6" style="display:none;" id="groupdiv">
      <h5>Is it on AIM Groupers List / Anthem SRx List</h5>
       <h6 style="font-size:10px; color:blue">*Check on AIM Grouper's List / SRx List ->Search for the code. Is it on the list?</h6>
      <select class="form-control" style="width: 200px;" id="grouplist" onchange="selectgroup()">
<option></option>
        <option value="yes">Yes</option>
        <option value="no">No</option>
      </select>
    </div>
   </div><hr>
<div class="col-sm-12">
<center><button class="btn btn-secondary" onclick="clearalldiv()" id="btn">Reset</button></center>
<br><br>
<div clas="row container" style="border: 1px #4085b9 dashed; border-radius:5px; padding: 20px">
<small> >> <strong> State of New Hampshire – Blue New England POS </strong> - If POS and Provider is INN therefore Cross Border Referral  is not required.</small>
<br><br>
<small> >> <strong> HealthTrust </strong>  -  If PCP is referring an OON provider, you may APPROVE it, DON’T PEND IT!.</small>
<br><br>
<small> >> <strong> Open Access /Access Blue Plan </strong>  -  If the Provider is INN, Cross Border Referral is not required.</small>
<br><br>
<small> >> <strong> YGE Prefix </strong>  -  If the Provider is INN, Cross Border Referral is not required same as Open Access.</small>
</div>
</div>
</div>

<div class="col-sm-6">
<div style="border: 1px #4085b9 dashed; border-radius:5px; padding: 20px">
<center><h5><b><u><strong>Terms to know</u></strong></b></h5></center>
<small> >> <strong> In-network: </strong> - When a specialist is located in the member’s contract state and is part of the member’s network..</small>
<br><br>
<small> >> <strong> Participating:  </strong>  -  When a specialist is located outside the member’s contract state and is part of the member’s network.</small>
<br><br>
<small> >> <strong> Out of network:  </strong>  -  When a specialist is located inside or outside the member’s contract state, but is not part of their network.</small>
<br><br>
<small> >> <strong> IFO Referral:  </strong>  -  When a member is being referred to an out of network specialist and we review to determine if member can have in-network benefits with said provider</small>
<br><br>
<small> >> <strong> Cross Border Referral: </strong>  -  When a member is being referred to a participating provider outside of their contract state where the case can be approved without a review of medical necessity. ONLY used for NEHP policies.</small>
<br><br>
<center><h5>*** <u><strong>Important</u></strong> ***</h5></center>
<br>
<small> >> <strong> Reto auth: </strong> INN (upto 1 Year) ONN (2 Business days)</small>
<br><br>
<small> >> They need to have an  <strong> "Approved Referral" </strong>1st before we can create an Auth wheather medical or Surgical.</small>
</div>
</div>

  </div>
<!----------- Phonebook Tab ----------------->
<div id="menu3" class="tab-pane fade" style="padding:15px; margin-left:-15px; margin-right:-15px; border-radius:5px";>
<center><h3>Phonebook</h3></center>
<center><h4 style="font-size:12px; color:red"><strong>***NOTE:</strong> <i> Other phone numbers that are not listed on this phone list, please check you email and/or offshore list.</i></h4></center>

<div class="row">
<div class="col-sm-6">
<div class="form-group">
<center><h5>Onshore and Clinical Fax#</h5></center>
<table class="table table-bordered table-responsive" style="font-size:12px; border:2px solid #2b85c2;">
    <thead style="background-color: #2b85c2; color: white">
      <tr>
        <th>Department</th>
        <th>UM Intake Phone# </th>
        <th>Fax # Oupatient</th>
<th>Fax # Inpatient</th>
      </tr>
    </thead>
<tbody>
      <tr>
        <td>NY Local ph# (Onshore)</td>
        <td>866-604-0936</td>
        <td>877-606-3803</td>
	<td>ASO - 888-892-0990  <br> FI - 888-309-9672 </td>
      </tr>
      <tr>
        <td>NY Local ph# (Offshore)</td>
        <td>800-982-8089</td>
        <td>877-606-3803</td>
	<td>ASO - 888-892-0990  <br> FI - 888-309-9672 </td>
      </tr>
<tr>
        <td>CT Local phone#</td>
        <td>800-238-2227</td>
	<td>877-539-3851</td>
	<td>Concurrent- 877-549-3987 <br> Future - 877-539-3851
</td>
      </tr>
<tr>
        <td>ME Local phone# </td>
        <td>800-392-1016</td>
<td>877-539-3855
</td>
<td>Concurrent - 877-539-9589 <br> Future - 877-539-3855
</td>
      </tr>
      <tr>
        <td>NH Local phone# </td>
        <td>800-531-4450</td>
	<td>877-539-3860 or 877-539-9588
	</td>
	<td>Concurrent - 800-281-1049  <br> Future - 877-539-3860 or 877-539-9588 </td>
      </tr>
</tbody>
</table>
</div>

<div "form-group">
<table class="table table-bordered table-responsive" style="font-size:12px; border:2px solid #2b85c2;">
<center><h5>Other Dept</h5></center>
    <thead style="background-color: #2b85c2; color: white">
      <tr>
        <th>Department</th>
        <th>Phone #</th>
        <th>Fax #</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>AIM</td>
        <td>877-430-2288</td>
<td>na</td>
      </tr>
      <tr>
        <td>FEP</td>
        <td>800-860-2156</td>
<td>na</td>
      </tr>
<tr>
        <td>Blue Card</td>
        <td>800-810-2583</td>
	<td>na</td>
</tr>
<tr>
        <td>Behavioral Health</td>
        <td>800-626-3643</td>
	<td>na</td>
</tr>
      <tr>
        <td>House Account</td>
        <td>877-875-1223</td>
	<td>na</td>
      </tr>
      <tr>
        <td>MediBlue</td>
        <td>855-690-7796</td>
	<td>na</td>
      </tr>
      <tr>
        <td>32BJ</td>
        <td>866-316-3394</td>
<td>na</td>
      </tr>
      <tr>
        <td>Suffolk County</td>
        <td>800-939-7515 </td>
<td>na</td>
      </tr>
<tr>
        <td>Spanish Hotline</td>
        <td>866-533-4997 | ext: 5001 </td>
<td>na</td>
      </tr>
<tr>
        <td>Specialty Drug</td>
        <td>833-293-0659</td>
<td>888-223-0550 </td>
      </tr>
<tr>
        <td>NY National (National IHM)</td>
        <td>855-342-7592 </td>
<td>na</td>
      </tr>
<tr>
        <td>NYC Indemnity (YLA Prefix)</td>
        <td>844-285-8209</td>
<td>na</td>
      </tr>
<tr>
        <td>NYC Indemnity (NYC Prefix)</td>
        <td>844-285-8210</td>
<td>na</td>
      </tr>
      <tr>
        <td>State of Connecticut</td>
        <td>800-238-2227</td>
	<td>na</td>
      </tr>
 <tr>
        <td>New York Appeals</td>
        <td>800-634-5605</td>
	<td>888-694-1545</td>
      </tr>
    </tbody>
</table>
</div>
</div>

<div class="row">
<div class="col-sm-6">
<div class="form-group">
<table class="table table-bordered table-responsive" style="font-size:12px; border:2px solid #2b85c2;">
<center><h5>West Local Phone Directory</h5></center>
    <thead style="background-color: #2b85c2; color: white">
      <tr>
        <th>State</th>
        <th>Department</th>
        <th>Phone #</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>CA</td>
        <td>UM Intake Ph#</td>
        <td>800-274-7767</td>
      </tr>
      <tr>
        <td>CA</td>
        <td>CalPERS Ph#</td>
        <td>800-451-6780</td>
      </tr>
      <tr>
        <td>CA</td>
        <td>National Ph#</td>
        <td>866-470-6244</td>
      </tr>
      <tr>
        <td>CO</td>
        <td>UM Intake Ph#</td>
        <td>800-832-7850</td>
      </tr>
      <tr>
        <td>NV</td>
        <td>UM Intake Ph#</td>
        <td>800-336-7797</td>
      </tr>
      <tr>
        <td>CA Local</td>
        <td>UM Backdoor Ph#</td>
        <td>877-672-0641</td>
      </tr>
      <tr>
        <td>CA National</td>
        <td>UM Backdoor Ph#</td>
        <td>877-672-0643</td>
      </tr>
      <tr>
        <td>CalPERS</td>
        <td>UM Backdoor Ph#</td>
        <td>855-255-3995</td>
      </tr>
      <tr>
        <td>CO / NV</td>
        <td>UM Backdoor Ph#</td>
        <td>877-672-0646</td>
      </tr>
    </tbody>
</table>
</div>

<div class="form-group">
<center><h5>Provider Services</h5></center>  
<table class="table table-bordered table-responsive" style="font-size:12px; border:2px solid #2b85c2;">
    <thead style="background-color: #2b85c2; color: white">
      <tr>
        <th>Department</th>
        <th>Phone #</th>
      </tr>
    </thead>
    <tbody>
       <tr>
        <td>All PS</td>
        <td>800-552-6630</td>
      </tr>
      <tr>
        <td>NY Prov. Serv#</td>
        <td>800-992-2583</td>
      </tr>
      <tr>
        <td>CT Prov. Serv#</td>
        <td>800-922-3242</td>
      </tr>
      <tr>
        <td>ME Prov. Serv# </td>
        <td>800-832-6011</td>
      </tr>
      <tr>
        <td>NH Prov. Serv#</td>
        <td>800-332-6558</td>
      </tr>
    </tbody>
  </table>
</div>

<div class="form-group">
<center><h5>Central Phone Number</h5></center>
<table class="table table-bordered table-responsive" style="font-size:12px; border:2px solid #2b85c2;">
    <thead style="background-color: #2b85c2; color: white">
      <tr>
        <th>Department</th>
        <th>Phone #</th>
      </tr>
    </thead>
    <tbody>
<tr>
        <td>IN UM Intake</td>
        <td>800-345-4348</td>
      </tr>
<tr>
        <td>KY UM Intake</td>
        <td>800-568-0075</td>
      </tr>
<tr>
        <td>OH UM Intake</td>
	<td>800-752-1182</td>
      </tr>
<tr>
        <td>MO UM Intake</td>
        <td>866-398-1922</td>
      </tr>
<tr>
        <td>WI UM Intake</td>
        <td>800-4726909</td>
      </tr>
    </tbody>
</table>
</div>
</div>
</div>

</div> <!-- end of row -->
</div> <!-- end of end of phonebook tab -->

<!----------- Super Notes TAB ----------------->


<div id="supernotes" class="tab-pane fade row">

<div style="float:right; margin-bottom: 10px;">
		<select class="form-control" id="theme" onchange="selectcolor()" style="width:100%;">
	 <option value="theme">Theme</option>
	<option value="Thistle">Thistle</option>
	<option value="LightSalmon">LightSalmon</option>
	<option value="PaleTurquoise">PaleTurquoise</option>
	<option value="Coral">Coral</option>
	<option value="DarkSeaGreen">DarkSeaGreen</option>
	<option value="LemonChiffon">LemonChiffon</option>
	<option value="Plum">Plum</option>
	<option value="PapayaWhip">PapayaWhip</option>
	<option value="LightSteelBlue">LightSteelBlue</option>
	<option value="PeachPuff">PeachPuff</option>
		</select>
</div>

<div class="row">
<div class="col-sm-4">
<div class="form-group">
         <label for="aname">Agent's Name</label>
         <select class="form-control" id="aname" onchange="nameperm()">
		<option>Choose your Name</option>
        	<option value="Agnes Detorres">Agnes Detorres</option>
        	<option value="Alnajir Lani">Alnajir Lani</option>
        	<option value="April Lyn Rocha">April Lyn Rocha</option>
        	<option value="Christian Garcia">Christian Garcia</option>
        	<option value="Cyr Patrick Pulmano ">Cyr Patrick Pulmano</option>
                <option value="Dennison Feliciano">Dennison Feliciano</option>
        	<option value="Eliud Espanola">Eliud Espanola</option>
        	<option value="Evanger Nolasco">Evanger Nolasco</option>
                <option value="Hercy Calpito">Hercy Calpito</option>
                <option value="Genevie Descalsota">Genevie Descalsota</option>
                <option value="Jeannice Partos">Jeannice Partos</option>
                <option value="Jessica Mae Velasquez">Jessica Mae Velasquez</option>
                <option value="Jeneva Bugayong">Jeneva Bugayong</option>
                <option value="Jessie Alexander Morete ">Jessie Alexander Morete</option>
                <option value="Jho Marie Elizondo">Jho Marie Elizondo</option>
                <option value="Jhulia Star Pascua">Jhulia Star Pascua</option>
                <option value="Jilbert Balaguer">Jilbert Balaguer</option>
                <option value="Joanna Marie Bermudez">Joanna Marie Bermudez</option>
                <option value="John Anthony Aquino">John Anthony Aquino</option>
                <option value="John Lester Matnog">John Lester Matnog</option>
                <option value="Maria Violeta Sangria">Maria Violeta Sangria</option>
                <option value="Maribeth Garcia">Maribeth Garcia</option>
                <option value="Michael Ramirez ">Michael Ramirez</option>
                <option value="Nirvana Ramos ">Nirvana Ramos</option>
                <option value="Prime Arat III">Prime Arat III</option>
                <option value="Remon Villamel Joyner">Remon Joyner</option>
                <option value="Shaun Michael Castronuevo">Shaun Michael Castronuevo</option>
                <option value="Sheila Mae Debuton">Sheila Debuton</option>
      </select>
  </div>
</div>
<div class="col-sm-4">
 <div class="form-group">
    <label for="cbn">Call Time:</label>
    <input type="text" id="min" style="width:20%; height: 30px; font-size: 14px; text-align: center; border-radius:5px" value="0">:
   <input type="text" id="sec" style="width:20%; height: 30px; font-size: 14px; text-align: center;border-radius:5px" value="0">
</div>
</div>
<div class="col-sm-4">
 <label for="rowcount"># of Calls:</label>
    <input type="text" id="rowcount" style="width:11%; height: 30px; border-radius:5px; font-size: 14px; text-align:center" value="0" disabled>

<label for="aht">AHT</label>
    <input type="text" id="aht" style="width:18%; height: 30px; border-radius:5px; font-size: 14px; text-align:center" value="000" disabled>

         <button type="button" id="nextcall" class="btn btn-primary" onclick="addRow()" style="float:right">Next Call</button>
</div>
</div>
<hr>      
<form style="font-size:11px">
  <div class="col-sm-4">
  <div class="form-group">
    <label for="cname">Caller Name</label>
    <input type="text" class="form-control" id="cname" placeholder="Enter Caller Name" onchange="casetempval()">
  </div>

  <div class="form-group">
    <label for="cbn">Phone No.</label>
    <input type="text" class="form-control" id="cbn" placeholder="Enter Call Back Number" onchange="casetempval()">
  </div>
 <div class="form-group">
         <label for="typeofcall">Type of Call</label>
<select class="form-control" id="typeofcall" onchange="casetempval()">
<option>Enter Type of Call</option>

        <option value="Authorization Status Check">Authorization Status Check</option>
        <option value="Authorization Update">Authorization Update</option>
        <option value="Initial Authorization/Case Created">Initial Authorization/Case Created</option>
<option value="Precertification Check">Precertification Check</option>
<option value="Misroute">Misroute</option>
<option value="Initiate Appeals">Initiate Appeals</option>
<option value="Initiate Peer To Peer">Initiate Peer To Peer</option>
<option value="General Inquiry">General Inquiry</option>
<option value="Disconnected Call/Dropped Call">Disconnected Call/Dropped Call</option>
<option value="Expedite Request">Expedite Request
</option>
      </select>
 </div>
   <hr>

  <div class="form-group">
    <label for="cbn">Provider NPI</label>
    <input type="text" class="form-control" id="provnpi" placeholder="Enter Provider NPI" onchange="casetempval()">
   </div>

   <div class="form-group">
    <label for="cbn">Facility NPI #</label>
    <input type="text" class="form-control" id="facinpi" placeholder="Enter Facility NPI " onchange="casetempval()">
  </div>
<hr>

<div class="form-group" id="memdiv">


    <label for="cbn">Member ID #</label>
<select class="form-control" id="multiplemem" onchange="casetempval()" style="width:21%; float:right; margin-right:15px">
<option value="no">no</option>
        <option value="yes">yes</option>
       

</select>
<span style="float:right; margin-right:15px">Multiple Members</span>

   <input type="text" class="form-control" id="memid" placeholder="Enter Member ID No." onchange="casetempval()">
  </div>

  <div class="form-group">
         <label for="region">Contracting Region</label>
<select class="form-control" id="region" onchange="casetempval()">
<option value="None">Region</option>
        <option value="NE Local">NE Local</option>
<option value="NY Local">NY Local</option>
<option value="Other Regions">Other Regions</option>
<option value="N/A">N/A</option>
      </select>
  </div>


</div>
 <div class="col-sm-4">


<div class="form-group">
         <label for="placeofservice">Place of Service</label>
<select class="form-control" id="placeofservice" onchange="casetempval()">
<option>Enter Place of Service</option>

        <option value="Office">OFFICE</option>
        <option value="Ambulatory">AMBULATORY </option>
        <option value="Outpatient Hospital">OP HOSP</option>
<option value="Inpatient Hospital">IP HOSP</option>
<option value="HOME">HOME</option>
      </select>
  </div>

<div class="form-group">
         <label for="typeofservice">Type of Service</label>
<select class="form-control" id="typeofservice" onchange="casetempval()">
<option>Enter Type of Service</option>

        <option value="Elective">Elective</option>
        <option value="Emergency">Emergency</option>
        <option value="Urgent">Urgent</option>
<option value="Maternity">Maternity</option>
<option value="NICU">NICU</option>
      </select>
  </div>
<hr>
<div class="form-group">
    <label for="cpt">CPT</label><select class="form-control" id="multiplecode" onchange="casetempval()" style="width:21%; float:right; margin-right:15px">
<option value="no">no</option>
        <option value="yes">yes</option>
       

</select>
<span style="float:right; margin-right:15px">Multiple Codes</span>
    <input type="text" class="form-control" id="cpt" placeholder="Enter CPT Codes" onchange="casetempval()">
  </div>
<div class="form-group">
    <label for="icd">ICD 10</label>
    <input type="text" class="form-control" id="ICD" placeholder="Enter Dx Codes" onchange="casetempval()">
  </div>
<hr>

<div class="form-group" id="tempnotedivne" style="display:none">
         <label for="tempnotene">Template Note NE</label>
<select class="form-control" id="tempnotene" onchange="casetempval()">
<option>Enter Template Note</option>

        <option value="Precert Created">Precert Created</option>
        <option value="Case Status Check – No Changes to Case">Case Status Check – No Changes to Case</option>
        <option value="Case Update / Extension Request">Case Update / Extension Request </option>
<option value="No Review Required">No Review Required</option>
<option value="Inpatient Surgery/Outpatient Surgery/DME">Inpatient Surgery/Outpatient Surgery/DME</option>
<option value="ER Cases">ER Cases</option>
<option value="Genetic Testing">Genetic Testing</option>
      </select>
 </div>
<div class="form-group" id="tempnotedivny" style="display:none">
         <label for="tempnoteny">Template Note NY</label>
<select class="form-control" id="tempnoteny" onchange="casetempval()">
<option>Enter Template Note NY</option>

        <option value="ER Cases">ER Cases</option>
        <option value="All Other Inpatient (IP) and Outpatient (OP) Cases">All Other Inpatient (IP) and Outpatient (OP) Cases</option>
<option value="Case Status Check – No Changes to Case">Case Status Check – No Changes to Case</option>
<option value="No Review Required">No Review Required</option>
<option value="No Benefit">No Benefit</option>
<option value="Coverage Terminated">Coverage Terminated</option>
<option value="Pre-D Suggested and Caller Declines">Pre-D Suggested and Caller Declines</option>
<option value="Pre-Note and Auto Approval">Pre-Note and Auto Approval</option>
<option value="Changes to a Case">Changes to a Case</option>
<option value="Non-Urgent to Urgent">Non-Urgent to Urgent</option>
      </select>
 </div>
<div class="form-group">
         <label for="transfer">Transfer</label>
<select class="form-control" id="transfer" onchange="selectXfer()">
<option>Enter Transfer</option>
<option value="AIM">AIM</option>
<option value="Appeals">Appeals</option>
<option value="Behavioral">Behavioral</option>
<option value="Blue Card">Blue Card</option>
<option value="Federal Employee Program">Federal Employee Program</option>
<option value="Member Services">Member Services</option>
<option value="National Account">National Account</option>
<option value="NE Onshore">NE Onshore</option>
<option value="Nurse">Nurse</option>
<option value="NY Onshore - Abroad Excluded">NY Onshore - Abroad Excluded</option>
<option value="NY Onshore - Denied Cases">NY Onshore - Denied Cases</option>
<option value="NY Onshore - FI HMO/HPOS">NY Onshore - FI HMO/HPOS</option>
<option value="Peer to Peer">Peer to Peer</option>
<option value="Provider Services">Provider Services</option>
<option value="Specialty Drug">Specialty Drug</option>
<option value="State of CT">State of CT</option>
<option value="Sup Call">Sup Call</option>
<option value="Total Transfer">Total Transfer</option>
<option value="TPA">TPA</option>
<option value="Others">Others(Please Specify)</option>
      </select>
 </div>

 </div>
 <div class="col-sm-4">
 <div class="form-group">
         <label for="clinicals">Clinicals</label>
	<select class="form-control" id="clinicals" onchange="casetempval()">
		<option>Clinical Fax Number</option>
		<option value="NY Clinical OP">NY Clinical OP: 877-606-3803</option>
		<option value="NY Clinical IP">NY IP ASO Clinical: 888-892-0990</option>
		<option value="NY Clinical OP">NY IP FI Clinical:888-309-9672</option>
		<option value="CT OP Clinical">CT OP Clinical: 877-539-3851</option>
		<option value="ME OP Clinical">ME OP Clinical: 877-539-3855</option>
		<option value="NH OP Clinical">NH OP Clinical: 877-539-3860 or 877-539-9588</option>
		<option value="CT IP Clinical">CT IP Clinical: Concurrent(877-549-3987) / Future(877-539-3851)</option>
		<option value="ME IP Clinical">ME IP Clinical: Concurrent(877-539-9589) / Future(877-539-3855)</option>
		<option value="NH IP Clinical">NH IP Clinical: Concurrent(800-281-1049) / Future( 877-539-3860 or 877-539-9588)</option>
      	</select>
 </div>

<div class="form-group">
    <label for="cbn">Work ID/Case No.</label>
    <input type="text" class="form-control" id="caseno" placeholder="Enter Case No./ Work ID" onchange="casetempval()">
  </div>

<div class="form-group">
    <label>Additional Note:</label><br>
    <textarea id="addnote" Placeholder="Enter your notes here" style="width: 95%" onchange="casetempval()"></textarea>
  </div>

<div class="form-group">
    <label>Case Template:</label><br>
    <textarea id="casetemp" disabled style="width: 95%"></textarea>
  </div>

<br>
<br>
<button type="button" id="clearall" class="btn btn-danger" style="float:right; margin-left:5px;" onclick="reset()">Clear</button>
<button type="button" id="trackdivbtn" class="btn btn-secondary" onclick="tracktable()" style="float:right; margin-left:5px;">Table Tracker</button>
<button type="button" id="historydivbtn" class="btn btn-secondary" onclick="historytable()" style="float:right">History</button>

 </div>
</div>



</form>
</div>
<div id="historydiv" style="display:none; padding:5px">
<button id="btnexporthistory" class="btn btn-success" style="float:right; margin:5px;" onclick="exportTableToExcel1()">Export</button>

<div id="tableWrapHistory" style="display:block; overflow-x: auto;" class="table">
    <table class="table table-bordered table-hover">
    <thead>
    <tr>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Name</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Phone Number</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Provider NPI</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Facility NPI</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Member ID #</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Region</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Place of Service</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Type of Service</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">CPT</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">DX</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Type of Call</th>
    <th style="background-color:#5f8fc2; color: white; width: 100px; border: 1px solid black">Transfer</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Clinicals</th>
    <th style="background-color:#5f8fc2; color: white; width: 300px; border: 1px solid black">Multiple Member or code</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Work ID/Case Number</th>
    <th style="background-color:#5f8fc2; color: white; width: 300px; border: 1px solid black">Remarks</th>
    <th style="background-color:#5f8fc2; color: white; border: 1px solid black">Min</th>
    <th style="background-color:#5f8fc2; color: white; border: 1px solid black">Sec</th>
    </tr>
    </thead>
    <tbody id="tableWrapBodyHistory">
   
    </tbody>
    </table>
</div>
    </div>


<div id="trackdiv" style="display:none; padding:5px">
<button id="btnexport" class="btn btn-success" style="float:right; margin:5px;" onclick="exportTableToExcel()">Export</button>

<div id="tableWrap" style="display:block" class="tally table">
    <table id="tabletracker" class="table table-bordered table-hover">
    <thead>
    <tr>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Name</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Type of Call</th>
    <th style="background-color:#5f8fc2; color: white; width: 100px; border: 1px solid black">Transfer</th>
    <th style="background-color:#5f8fc2; color: white; width: 100px; border: 1px solid black">Region</th>
    <th style="background-color:#5f8fc2; color: white; width: 200px; border: 1px solid black">Work ID/Case Number</th>
    <th style="background-color:#5f8fc2; color: white; width: 300px; border: 1px solid black">Multiple Member or code</th>
    <th style="background-color:#5f8fc2; color: white; width: 300px; border: 1px solid black">Remarks</th>
    <th style="background-color:#5f8fc2; color: white; border: 1px solid black">Min</th>
    <th style="background-color:#5f8fc2; color: white; border: 1px solid black">Sec</th>
    </tr>
    </thead>
    <tbody id="tableWrapBody">
   
    </tbody>
    </table>
</div>
    </div>
</div>


<!-- jQuery library -->
<br>
<footer><center><span style="color: rgb(220,220,220); font-size:16px"><div class="popup"  id="myPopup">Copyright &copy 2019</span>
</div></span><center><center><span style="color: rgb(220,220,220); font-size:16px"><div class="popup"  id="myPopup">Created | Updated by: J Altarejos & JL Matnog</span>
</div></span><center></footer>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/4.3.1/jquery.min.js"></script>

<script type="text/javascript">

$(document).ready(function()
{
    $(window).bind("beforeunload", function() {
        exportTableToExcel();
    });
});

setInterval(function(){exportTableToExcel();}, 3600000);
function send() {
window.open('mailto:Christian.Garcia2@anthem.com');
}
</script>
<script type="text/javascript">
function nameperm() {
$("#aname").attr("disabled", true);
document.getElementById("aname").style.backgroundColor="";
}






var transfer = document.getElementById("transfer");

function selectXfer() {
if (transfer.value == "AIM") {
alert("AIM - 877-430-2288");
	}
if (transfer.value == "Appeals") {
alert("Appeals - Onshore");
	}
if (transfer.value == "Behavioral") {
alert("Behavioral - 800-626-3643");
	}
if (transfer.value == "Blue Card") {
alert("Blue Card - 800-810-2583");
	}
if (transfer.value == "Federal Employee Program") {
alert("FEP - 800-860-2156");
	}
if (transfer.value == "National Account") {
alert("National Account - 855-342-7592");
	}
if (transfer.value == "NE Onshore") {
alert("NE Onshore - 855-478-4369");
	}
if (transfer.value == "Nurse") {
alert("Nurse - IP: 855-711-8592 | OP: 855-711-8955");
	}
if (transfer.value == "NY Onshore - Abroad Excluded") {
alert("NY Onshore - Abroad Excluded - 866-604-0936");
	}
if (transfer.value == "Peer to Peer") {
alert("Peer to Peer - 800-688-1019 Option 4");
	}
if (transfer.value == "Provider Services") {
alert("Check Phonebook Tab for All Provider services numbers");
	}
if (transfer.value == "Specialty Drug") {
alert("Specialty Drug - 833-293-0659");
	}
if (transfer.value == "State of CT") {
alert("State of CT - 800-238-2227");
	}
if (transfer.value == "State of CT") {
alert("State of CT - 800-238-2227");
	}
}


function exportTableToExcel(){
    var downloadLink;
    var dataType = 'application/vnd.ms-excel';
    var tableHTML = encodeURIComponent($('#tableWrap').html());
    var today = new Date();
var dd = String(today.getDate()).padStart(2, '0');
var mm = String(today.getMonth() + 1).padStart(2, '0'); //January is 0!
var yyyy = today.getFullYear();

today = mm + '/' + dd + '/' + yyyy;
    if (document.getElementById("aname").value != "Choose your Name") {
    var aname = document.getElementById("aname").value + "-Call Tracker-" + today;
}
if (document.getElementById("aname").value == "Choose your Name") {
    var aname = "Call Tracker-" + today;
}
    // Specify file name
    filename = aname?aname+'.xls':'excel_data.xls';
   
    // Create download link element
    downloadLink = document.createElement("a");
   
    document.body.appendChild(downloadLink);
   
    if(navigator.msSaveOrOpenBlob){
        var blob = new Blob(['\ufeff', tableHTML], {
            type: dataType
        });
        navigator.msSaveOrOpenBlob( blob, filename);
    }else{
        // Create a link to the file
        downloadLink.href = 'data:' + dataType + ', ' + tableHTML;
   
        // Setting the file name
        downloadLink.download = filename;
       
        //triggering the function
        downloadLink.click();

    }
}
function exportTableToExcel1(){
    var downloadLink;
    var dataType = 'application/vnd.ms-excel';
    var tableHTML = encodeURIComponent($('#tableWrapHistory').html());
    var today = new Date();
var dd = String(today.getDate()).padStart(2, '0');
var mm = String(today.getMonth() + 1).padStart(2, '0'); //January is 0!
var yyyy = today.getFullYear();

today = mm + '/' + dd + '/' + yyyy;
    if (document.getElementById("aname").value != "Choose your Name") {
    var aname = document.getElementById("aname").value + "-History-" + today;
}
if (document.getElementById("aname").value == "Choose your Name") {
    var aname = "History-" + today;
}
    // Specify file name
    filename = aname?aname+'.xls':'excel_data.xls';
   
    // Create download link element
    downloadLink = document.createElement("a");
   
    document.body.appendChild(downloadLink);
   
    if(navigator.msSaveOrOpenBlob){
        var blob = new Blob(['\ufeff', tableHTML], {
            type: dataType
        });
        navigator.msSaveOrOpenBlob( blob, filename);
    }else{
        // Create a link to the file
        downloadLink.href = 'data:' + dataType + ', ' + tableHTML;
   
        // Setting the file name
        downloadLink.download = filename;
       
        //triggering the function
        downloadLink.click();

    }
}
function selectcolor() {
var supernotes = document.getElementById('supernotes');
var theme = document.getElementById('theme');

if (theme.value == 'theme') {
supernotes.style.backgroundColor = "#ededed";
supernotes.style.color = "black";
}
if (theme.value == 'Thistle') {
supernotes.style.backgroundColor = "#d3cce3";
supernotes.style.color = "black";
}
if (theme.value == 'LightSalmon') {
supernotes.style.backgroundColor = "#e8c1bc";
supernotes.style.color = "black";
}
if (theme.value == 'PaleTurquoise') {
supernotes.style.backgroundColor = "#abd6d6";

}
if (theme.value == 'Coral') {
supernotes.style.backgroundColor = "#deb1a2";
supernotes.style.color = "black";

}
if (theme.value == 'DarkSeaGreen') {
supernotes.style.backgroundColor = "#b0d6ab";
supernotes.style.color = "black";

}
if (theme.value == 'LemonChiffon') {
supernotes.style.backgroundColor = "#dadba2";
supernotes.style.color = "black";

}
if (theme.value == 'Plum') {
supernotes.style.backgroundColor = "#f0cce8";
supernotes.style.color = "black";
}
if (theme.value == 'PapayaWhip') {
supernotes.style.backgroundColor = "#e3d5bc";
supernotes.style.color = "black";
}
if (theme.value == 'LightSteelBlue') {
supernotes.style.backgroundColor = "#c5cbeb";
supernotes.style.color = "black";
}
if (theme.value == 'PeachPuff') {
supernotes.style.backgroundColor = "#f7c5c1";
supernotes.style.color = "black";
}
}


function reset() {
var min = document.getElementById("min").value = "0";
var sec = document.getElementById("sec").value = "0";
var cname = document.getElementById("cname").value = "";
var cbn = document.getElementById("cbn").value = "";
var provnpi = document.getElementById("provnpi").value = "";
var facinpi = document.getElementById("facinpi").value = "";
var memid = document.getElementById("memid").value = "";
var region = document.getElementById("region").value = "None";
var placeofservice = document.getElementById("placeofservice").selectedIndex = "0";
var typeofservice = document.getElementById("typeofservice").selectedIndex = "0";
var cpt = document.getElementById("cpt").value = "";
var icd = document.getElementById("ICD").value = "";
var typeofcall = document.getElementById("typeofcall").selectedIndex = "0";
var transfer = document.getElementById("transfer").selectedIndex = "0";
var clinicals = document.getElementById("clinicals").selectedIndex = "0";
var caseno = document.getElementById("caseno").value = "";
var addnote = document.getElementById("addnote").value = "";
var casetemp = document.getElementById("casetemp").value = "";
document.getElementById("tempnotedivne").style.display = "none";
document.getElementById("tempnotedivny").style.display = "none";
document.getElementById("tempnotene").value = "";
document.getElementById("tempnoteny").value = "";
document.getElementById("multiplemem").value ="no";
document.getElementById("multiplecode").value ="no";
}
</script>

<script type="text/javascript">
function my_onkeydown_handler( event ) {
    switch (event.keyCode) {
        case 116 : // 'F5'
            event.preventDefault();
            event.keyCode = 0;
            window.status = "F5 disabled";
            break;
    }
}
document.addEventListener("keydown", my_onkeydown_handler);
</script>
<script>
function tracktable() {
     var x = document.getElementById("trackdiv")
  if (x.style.display === 'none') {
    x.style.display = 'block';
  } else {
    x.style.display = 'none';
  }
}


function historytable() {
     var x = document.getElementById("historydiv")
  if (x.style.display === 'none') {
    x.style.display = 'block';
  } else {
    x.style.display = 'none';
  }
}
function casetempval() {

var aname = document.getElementById("aname").value;
if (aname == "Choose your Name") {
aname = "N/A";
}
var cname = document.getElementById("cname").value;
if (cname == null || cname == "") {
cname = "N/A";
}
var cbn = document.getElementById("cbn").value;
if (cbn == null || cbn == "") {
cbn = "N/A";
}
var provnpi = document.getElementById("provnpi").value;
if (provnpi == null || provnpi == "") {
provnpi = "N/A";
}
var facinpi = document.getElementById("facinpi").value;
if (facinpi == null || facinpi == "") {
facinpi = "N/A";
}
var memid = document.getElementById("memid").value;
if (memid == null || memid == "") {
memid = "N/A";
}
var region = document.getElementById("region").value;
if (region == "Region") {
region = "N/A";
}
var placeofservice = document.getElementById("placeofservice").value;
if (placeofservice == "Enter Place of Service") {
placeofservice = "N/A";
}
var typeofservice = document.getElementById("typeofservice").value;
if (typeofservice == "Enter Type of Service") {
typeofservice = "N/A";
}
var cpt = document.getElementById("cpt").value;
if (cpt == null || cpt == "") {
cpt = "N/A";
}
var ICD = document.getElementById("ICD").value;
if (ICD == null || ICD == "") {
ICD = "N/A";
}
var typeofcall = document.getElementById("typeofcall").value;
if (typeofcall == "Enter Type of Call") {
typeofcall = "N/A";
}
var transfer = document.getElementById("transfer").value;
if (transfer == "Enter Transfer") {
transfer = "N/A";
}
var clinicals = document.getElementById("clinicals").value;
if (clinicals == "Clinical Fax Number") {
clinicals = "N/A";
}
var caseno = document.getElementById("caseno").value;
if (caseno == null || caseno == "") {
caseno = "N/A";
}
var addnote = document.getElementById("addnote").value;
if (addnote == null || addnote == "") {
addnote = "N/A";
}
var casetemp = document.getElementById("casetemp").value;
if (casetemp == null || casetemp == "") {
casetemp = "N/A";
}
var min = document.getElementById("min").value;
if (min == null || min == "") {
min = "0";
}
var sec = document.getElementById("sec").value;
if (sec == null || sec == "") {
sec = "0";
}

var casetemp = document.getElementById("casetemp");
var tempnotedivne = document.getElementById("tempnotedivne");
var tempnotene = document.getElementById("tempnotene").value;
var tempnotedivny = document.getElementById("tempnotedivny");
var tempnoteny = document.getElementById("tempnoteny").value;
if (typeofcall == "Initial Authorization/Case Created" || typeofcall == "Authorization Status Check" || typeofcall == "Precertification Check") {
	casetemp.value = "Agent: " + aname + 
"\n---Call Details---\n" +
"Caller Name: " + cname + "\n" + 
"Caller CBN: " + cbn + "\n" +
"Provider NPI: " + provnpi + "\n" + 
"Facility NPI: " + facinpi + "\n" + 
"Member ID #: " + memid + "\n" + 
"State: " + region + "\n" +
"Place of Service: " + placeofservice + "\n" + 
"Type of Service: " + typeofservice + "\n" + 
"CPT: " + cpt + " Dx: " + ICD + "\n" +
"Type of Call: " + typeofcall + "\n" +  
"Transfer: " + transfer + "\n" + 
"Clinical Fax: " + clinicals + "\n" + 
"Case Number: " + caseno + "\n" + 
"Additional Notes: " + addnote + "\n" +
"\n---End---\n";
    if (region == "NE Local") {
	tempnotedivne.style.display = "block";
	tempnotedivny.style.display = "none";
	if  (tempnotene == "Precert Created") {
		casetemp.style.color = "blue";
		casetemp.value = "Non-Clinical notes: \n" +
		cname + ", from NPI:" + provnpi + "/" + facinpi + 		"\n" + "CPT Codes no review: " + cpt + "\n" +
		"UR#:\n" +
		"Gave Fax #";
	}
        if  (tempnotene == "Case Status Check – No Changes to Case") {
		casetemp.style.color = "blue";
		casetemp.value = "Non-Clinical notes: \n" +
		"Adv Case status: Pending / Approved" + "\n" +
		"Details if escalation sent: N/A";
		
	}
	if  (tempnotene == "Case Update / Extension Request") {
		casetemp.style.color = "blue";
		casetemp.value = "Non-Clinical notes: \n" +
		cname + ", from NPI:" + provnpi + "/" + facinpi + "\n" +
		"Details of update / extension: ";
		
	}
	if  (tempnotene == "No Review Required") {
		casetemp.style.color = "blue";
		casetemp.value = "Non-Clinical notes: \n" +
		cname + ", from NPI:" + provnpi + "/" + facinpi +
		"\nPX: " + cpt +
		"\nDX: " + ICD +
		"\nSetting: " + placeofservice;
		
	}
	if  (tempnotene == "Inpatient Surgery/Outpatient Surgery/DME") {
		casetemp.style.color = "blue";
		casetemp.value = "Non-Clinical notes: \n" +
		cname + ", from NPI:" + provnpi + "/" + facinpi +
		"\nCPT Codes no review: N/A" + "\n" +
		"UR#: " +
		"\nPX: " + cpt +
		"\nDX: " + ICD +
		"\nSetting: " + placeofservice;
		
	}
	if  (tempnotene == "ER Cases") {
		casetemp.style.color = "blue";
		casetemp.value = "Non-Clinical notes: \n" +
		cname + ", from NPI:" + provnpi + "/" + facinpi +
		"\nAdditional Codes: N/A" +
		"DCN: N/A " +
		"UR#: " +
		"\nPX: " + cpt +
		"\nDX: " + ICD +
		"\nSetting: " + placeofservice;
		
	}
	if  (tempnotene == "Genetic Testing") {
		casetemp.style.color = "blue";
		casetemp.value = "Non-Clinical notes: \n" +
		cname + ", from NPI:" + provnpi + "/" + facinpi +
		"\nCPT Codes no review: N/A" +
		"\nPX: " + cpt +
		"\nDX: " + ICD;
		
	}
    }
    if (region == "NY Local") {
	tempnotedivne.style.display = "none";
	tempnotedivny.style.display = "block";
	if  (tempnoteny == "ER Cases") {
		casetemp.style.color = "blue";
		casetemp.value = "Additional Codes: \n" +
		"DCN:\n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "All Other Inpatient (IP) and Outpatient (OP) Cases") {
		casetemp.style.color = "blue";
		casetemp.value = "Additional Codes: \n" +
		"Benefit Max /Limitations: N/A \n" +
		"DCN: N/A \n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "Case Status Check – No Changes to Case") {
		casetemp.style.color = "blue";
		casetemp.value = "Caller Name: " + name + "\n" +
		"Caller Phone: " + cbn + "\n" +
		"Case Status Provided: \n" +
		"DCN: N/A \n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "No Review Required") {
		casetemp.style.color = "blue";
		casetemp.value = "PX: " + cpt + "\n" +
		"DX: " + ICD + "\n" +
		"Setting:" + placeofservice + "\n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "No Benefit") {
		casetemp.style.color = "blue";
		casetemp.value = "PX: " + cpt + "\n" +
		"DX: " + ICD + "\n" +
		"Setting:" + placeofservice + "\n" +
		"No Benefit \n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "Coverage Terminated") {
		casetemp.style.color = "blue";
		casetemp.value = "MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "Pre-D Suggested and Caller Declines") {
		casetemp.style.color = "blue";
		casetemp.value = "PX: " + cpt + "\n" +
		"DX: " + ICD + "\n" +
		"Setting:" + placeofservice + "\n" +
		"Caller Declined - Precert Not Required/ Pre-d Recommended \n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "Pre-Note and Auto Approval") {
		casetemp.style.color = "blue";
		casetemp.value = "Additional Codes: " + "\n" +
		"DCN: N/A \n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "Changes to a Case") {
		casetemp.style.color = "blue";
		casetemp.value = "Updates Made: " + "\n" +
		"DCN: N/A \n" +
		"MCRT: N \n" +
		"Call Recorded Notification: N/A \n" +
		"Trans to: RN";
	}
	if  (tempnoteny == "Non-Urgent to Urgent") {
		casetemp.style.color = "blue";
		casetemp.value = "Level of service changed from elective to urgent per request received today from ___.  Date and time fields updated to support turnaround time.";
	}
    }	
} else {
casetemp.value = "Agent: " + aname + 
"\n---Call Details---\n" +
"Caller Name: " + cname + "\n" + 
"Caller CBN: " + cbn + "\n" +
"Provider NPI: " + provnpi + "\n" + 
"Facility NPI: " + facinpi + "\n" + 
"Member ID #: " + memid + "\n" + 
"State: " + region + "\n" +
"Place of Service: " + placeofservice + "\n" + 
"Type of Service: " + typeofservice + "\n" + 
"CPT: " + cpt + " Dx: " + ICD + "\n" +
"Type of Call: " + typeofcall + "\n" +  
"Transfer: " + transfer + "\n" + 
"Clinical Fax: " + clinicals + "\n" + 
"Case Number: " + caseno + "\n" + 
"Additional Notes: " + addnote + "\n" +
"\n---End---\n";
}
}
function addRow() {

var aname = document.getElementById("aname").value;
if (aname == "Choose your Name") {
aname = "N/A";
}
var cname = document.getElementById("cname").value;
if (cname == null || cname == "") {
cname = "N/A";
}
var cbn = document.getElementById("cbn").value;
if (cbn == null || cbn == "") {
cbn = "N/A";
}
var provnpi = document.getElementById("provnpi").value;
if (provnpi == null || provnpi == "") {
provnpi = "N/A";
}
var facinpi = document.getElementById("facinpi").value;
if (facinpi == null || facinpi == "") {
facinpi = "N/A";
}
var memid = document.getElementById("memid").value;
if (memid == null || memid == "") {
memid = "N/A";
}
var region = document.getElementById("region").value;
if (region == "Region") {
region = "N/A";
}
var placeofservice = document.getElementById("placeofservice").value;
if (placeofservice == "Enter Place of Service") {
placeofservice = "N/A";
}
var typeofservice = document.getElementById("typeofservice").value;
if (typeofservice == "Enter Type of Service") {
typeofservice = "N/A";
}
var multiplecode = document.getElementById("multiplecode").value;
if (multiplecode == 'no') {
multiplecode = "";
} else {
multiplecode = "Multiple Codes";
}

var cpt = document.getElementById("cpt").value;
if (cpt == null || cpt == "") {
cpt = "N/A";
}
var ICD = document.getElementById("ICD").value;
if (ICD == null || ICD == "") {
ICD = "N/A";
}
var typeofcall = document.getElementById("typeofcall").value;
if (typeofcall == "Enter Type of Call") {
typeofcall = "N/A";
}
var transfer = document.getElementById("transfer").value;
if (transfer == "Enter Transfer") {
transfer = "N/A";
}
var clinicals = document.getElementById("clinicals").value;
if (clinicals == "Clinical Fax Number") {
clinicals = "N/A";
}
var caseno = document.getElementById("caseno").value;
if (caseno == null || caseno == "") {
caseno = "N/A";
}
var multiplemem = document.getElementById("multiplemem").value;
if (multiplemem == 'no') {
multiplemem = "";
} else {
multiplemem = "Multiple Members";
}

var addnote = document.getElementById("addnote").value;
if (addnote == null || addnote == "") {
addnote = "N/A";
}
var casetemp = document.getElementById("casetemp").value;
if (casetemp == null || casetemp == "") {
casetemp = "N/A";
}
var min = document.getElementById("min").value;
if (min == null || min == "") {
min = "0";
}
var sec = document.getElementById("sec").value;
if (sec == null || sec == "") {
sec = "0";
}
var aname1= $('#aname');
        var cname1 = $('#cname');
        var cbn1 = $('#cbn');
        var memid1 = $('#memid');
        var region1 = $('#region');
        var typeofcall1 = $('#typeofcall');
var caseno1 = $('#caseno');
var min1 = $('#min');
var sec1 = $('#sec');
var queue1 = $('#queue');
        if (aname1.val() == 'Choose your Name') {
            aname1.addClass('error')
        } else {
            aname1.removeClass('error')
        }
       
        if (!cname1.val()) {
            cname1.addClass('error')
        } else {
            cname1.removeClass('error')
        }

        if (!cbn1.val()) {
            cbn1.addClass('error')
        } else {
            cbn1.removeClass('error')
        }

        if (!memid1.val()) {
            memid1.addClass('error')
        } else {
            memid1.removeClass('error')
        }

if (region1.val() == 'None') {
            region1.addClass('error')
        } else {
            region1.removeClass('error')
        }

        if (typeofcall1.val() == 'Enter Type of Call') {
            typeofcall1.addClass('error')
        } else {
            typeofcall1.removeClass('error')
        }

if (!caseno1.val()) {
            caseno1.addClass('error')
        } else {
            caseno1.removeClass('error')
        }

if (min1.val() == '0') {
            min1.addClass('error')
        } else {
            min1.removeClass('error')
        }
if (sec1.val() == '0') {
            sec1.addClass('error')
        } else {
            sec1.removeClass('error')
        }
if (queue1.val() == 'Queue') {
            queue1.addClass('error')
        } else {
            queue1.removeClass('error')
        }


if (aname == "N/A") {

alert("Agent's Name should be populated!");
} else if (cname == "N/A") {

alert("Caller's Name should be populated!");
} else if (cbn == "N/A") {

alert("Caller's CBN should be populated!");
} else if (memid == "N/A") {

alert("Member ID should be populated!");
} else if (region == "None") {
alert("Contracting State should be populated!");
} else if (typeofcall == "N/A") {
alert("Type of Call should be populated!");
} else if (min == "0") {
alert("Minutes should be populated!");
}  else if (sec == "0") {
alert("Seconds should be populated!");
} else if (caseno == "N/A") {
alert("Case Number/Work ID should be populated!");
} else {
var tablebody = document.getElementById("tableWrapBody");
tablebody.innerHTML += "<tr class='sum'>" +
"<td contenteditable='true' style='border: 1px solid black'>" + aname + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + typeofcall + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + transfer + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + region + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + caseno + "</td>" +
"<td style='border: 1px solid black'>" + multiplemem + " " + multiplecode + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + addnote + "</td>" +
"<td contenteditable='true' class='min' style='border: 1px solid black'>" + min + "</td>" +
"<td contenteditable='true' class='sec' style='border: 1px solid black'>" + sec + "</td></tr>";

var tablebody = document.getElementById("tableWrapBodyHistory");
tablebody.innerHTML += "<tr>" +
"<td contenteditable='true' style='border: 1px solid black'>" + cname + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + cbn + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + provnpi + "</td>" +
"<td style='border: 1px solid black'>" + facinpi + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + memid + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + region + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + placeofservice + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + typeofservice + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + cpt + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + ICD + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + typeofcall + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + transfer + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + clinicals + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + caseno + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + multiplemem + " " + multiplecode + "</td>" +
"<td contenteditable='true' style='border: 1px solid black'>" + addnote + "</td>" +
"<td  contenteditable='true' style='border: 1px solid black'>" + min + "</td>" +
"<td  contenteditable='true' style='border: 1px solid black'>" + sec + "</td></tr>";


$(document).ready(function(){
    var min = 0;
       $(".min").each(function(){
          var value = parseInt($(this).text())*60;
          min += value;

       });
    var sec = 0;
       $(".sec").each(function(){
          var value1 = parseInt($(this).text());
          sec += value1;

       });
    var rowCount = $('#tableWrap tr').length - 1;
    $("#rowcount").val(rowCount);
      total = min + sec;
     
    $("#aht").val(total/rowCount);
    if (parseInt($("#aht").val()) >= 381) {
$("#aht").css("backgroundColor", "red");
$("#aht").css("color", "white");
    }
    if (parseInt($("#aht").val()) <= 380) {
$("#aht").css("backgroundColor", "green");
$("#aht").css("color", "white");
    }
});

reset();
alert("Successful!");
}
}

</script>

<script>

  var hook = true;
  window.onbeforeunload = function() {
    if (hook) {

      return "Did you save your stuff?"
    }
  }
  function unhook() {
    hook=false;
  }

// When the user clicks on <div>, open the popup
function myFunction() {
  var popup = document.getElementById("myPopup");
  popup.classList.toggle("show");
}


/* tool opener js*/

<script src="https://ajax.googleapis.com/ajax/libs/jquery/4.3.1/jquery.min.js"></script>
<script type="text/javascript">
var sourcediv = document.getElementById("sourcediv");
var aimelem = document.getElementById("aimelem");
var source = document.getElementById("source");
var aimdiv = document.getElementById("aimdiv");
var aimcov = document.getElementById("aimcov");
var groupdiv = document.getElementById("groupdiv");
var grouplist = document.getElementById("grouplist");
var ftdiv = document.getElementById("ftdiv");
var ft = document.getElementById("ft");

var pcpelem = document.getElementById("pcpelem");
var pcpsource = document.getElementById("pcpsource");
var pcpsourcediv = document.getElementById("pcpsourcediv");
var umregion = document.getElementById("umregion");
var umregiondiv = document.getElementById("umregiondiv");
var contractdiv = document.getElementById("contractdiv");
var contract = document.getElementById("contract");
var mddiv = document.getElementById("mddiv");
var md = document.getElementById("md");



function selectPcpoffices() {
	if (pcpelem.value == "yes") {
		pcpsourcediv.style.display = "block";
	}
	if (pcpelem.value == "no") {
		alert("Referral can only be initiated by the PCP. Please ask the caller to let the PCP call us.");
			pcpsourcediv.style.display = "none";
			clearalldiv();
	}
}

function selectPcpsources() {
	if (pcpsource.value == "yes") {
		umregiondiv.style.display = "block";
	}
	if (pcpsource.value == "no") {
		alert("Advise to let the member call the member services and update the PCP information.");
			pcpsourcediv.style.display = "block";
			umregiondiv.style.display = "none";
	}
}

function selectUmregion() {
	if (umregion.value == "nehplocal") {
		contractdiv.style.display = "block";
	}
	if (umregion.value == "nelocal") {
		alert("Check Athem.com and/or MCW for Participating status\n\n-INN: No referral is needed\n-OON : OON referral is needed and pend for review!");
		contractdiv.style.display = "none";
	}
}

function selectContractstate() {
	if (contract.value == "yes") {
		mddiv.style.display = "block";		
	}
	if (contract.value == "no") {
		alert("Refer the provider to their respective BCBS Home state!");
		mddiv.style.display = "none";	
	}
}

function selectMdloc() {
	if (md.value == "home") {
		alert("Require cross-border referrals when a participating provider is outside the PCP Contract State.\n\n*If PCP and specialist is contracted within the same state.\n-PAR - No case required\n-NON-PAR - IFO case required, pend it for review!\n\nNote: Please only use Anthem.com | MCW in checking PAR status for CT/NH/ME.");	
	}
	if (md.value == "host") {
		alert("Require cross-border referrals when a participating provider is outside the PCP Contract State.\n\n*Please use respective BCBS website to check participating status.\n-PAR - Referral can be approve for 6 months (can backdate)\n-NON-PAR - Referral should pend for review.\n\nNote: Reason of referral approval should be NCS approval Only!");	
	}
}


		
/* aim tab */

function selectAim() {
	sourcediv.style.display = "block";
}
function selectSource() {
   	if (aimelem.value == "gen") {                                          
	    	if (source.value == "star" || source.value == "wgs" || source.value == "nasco") {
		alert("Transfer to AIM, regardless of the funding type (ASO/FI) - 918774302288");
		clearalldiv();
		} 
           if (source.value == "aces") {
			aimdiv.style.display = "block";
		}
	} 
	if (aimelem.value == "radcar") {         
		if (source.value == "star" || source.value == "wgs" || source.value == "nasco") {
			groupdiv.style.display = "block";
			aimdiv.style.display = "none";
		} 
		if (source.value == "aces") {
			aimdiv.style.display = "block";
			groupdiv.style.display = "none";
		}
	}
	if (aimelem.value == "drug") {         
		if (source.value == "star" || source.value == "wgs" || source.value == "nasco" || source.value == "aces") {
			groupdiv.style.display = "block";
			aimdiv.style.display = "none";
		} 
		
	}
	if (aimelem.value == "msk") {         
		if (source.value == "star" || source.value == "wgs" || source.value == "nasco") {
			ftdiv.style.display = "block";
			aimdiv.style.display = "none";
		} 
		if (source.value == "aces") {
			aimdiv.style.display = "block";
			ftdiv.style.display = "none";
		}
	}
	if (aimelem.value == "upgi") {         
		if (source.value == "star" || source.value == "wgs" || source.value == "nasco") {
			ftdiv.style.display = "block";
			aimdiv.style.display = "none";
		} 
		if (source.value == "aces") {
			aimdiv.style.display = "block";
			ftdiv.style.display = "none";
		}
	}

}
function selectAimCov() {
	if (aimelem.value == "gen") {    
		 if (source.value == "aces") {
			if (aimcov.value == "umcm") {
				alert("Transfer to AIM - 918774302288");
				clearalldiv();
			}
			if (aimcov.value == "na") {
				alert("Check applicable MP and CG. Create a case if needed");
				clearalldiv();
			}
		}
	}
	if (aimelem.value == "radcar") {    
		 if (source.value == "aces") {
			if (aimcov.value == "umcm") {
				alert("Transfer to AIM - 918774302288");
			}
			if (aimcov.value == "na") {
				alert("Check applicable MP and CG. Create a case if needed");
				clearalldiv();
			}
		}
	} 
	if (aimelem.value == "msk") {    
		 if (source.value == "aces") {
			if (aimcov.value == "umcm") {
				alert("Transfer to AIM - 918774302288");
				clearalldiv();
			}
			if (aimcov.value == "na") {
				alert("Check applicable MP and CG. Create a case if needed");
				clearalldiv();
			}
		}
	} 
	if (aimelem.value == "upgi") {    
		 if (source.value == "aces") {
			if (aimcov.value == "umcm") {
				alert("Transfer to AIM - 918774302288");
				clearalldiv();
			}
			if (aimcov.value == "na") {
				alert("Check applicable MP and CG. Create a case if needed");
				clearalldiv();
			}
		}
	} 
}
function selectgroup() {
	if (aimelem.value == "radcar") {    
		 if (source.value == "star" || source.value == "wgs" || source.value == "nasco") {
			if (grouplist.value == "yes") {
				alert("Transfer to AIM - 918774302288");
				clearalldiv();
			}
			if (grouplist.value == "no") {
				alert("Check applicable MP and CG. Create a case if needed");
				clearalldiv();
			}
		}
	} 
}
function selectgroup() {
	if (aimelem.value == "drug") {    
		 if (source.value == "star" || source.value == "wgs" || source.value == "nasco" || source.value == "aces") {
			if (grouplist.value == "yes") {
				alert("Transfer to AIM: 8774302288 | SRx Dept: 833-293-0659");
				clearalldiv();
			}
			if (grouplist.value == "no") {
				alert("Check applicable MP and CG. Create a case if needed");
				clearalldiv();
			}
		}
	} 
}
function selectft() {
	if (aimelem.value == "msk") {    
		 if (source.value == "star" || source.value == "wgs" || source.value == "nasco") {
			if (ft.value == "aso") {
				alert("No PreC is required");
				clearalldiv();
			}
			if (ft.value == "fi") {
				alert("Trasnfer to AIM - 918774302288");
				clearalldiv();
			}
		}
	} 
}
function clearalldiv() {
	aimdiv.style.display = "none";
	ftdiv.style.display = "none";
	sourcediv.style.display = "none";
	aimelem.value = "";
	ft.value="";
	source.value="";
	aimcov.value="";
        groupdiv.style.display = "none";
	grouplist.value = "";
	pcpelem.value=""
	pcpsource.value=""
	pcpsourcediv.style.display = "none";
	umregion.value=""
	umregiondiv.style.display = "none";
	contractdiv.style.display = "none";
	contract.value=""
	mddiv.style.display = "none";
	md.value=""
	
}


</script>


<script>
$(document).ready(function(){
  // convert selects already on the page at dom load
  $('select.form-control').combobox();
  $('#it').click(function(e){
    $('ul.dropdown-menu').toggle();
  });
 
//  $('input').focus(function(e){
//    $('ul.dropdown-menu').toggle();
//  });
 
});


</script>
<script>
$(document).ready(function(){
for (var i = 0; i < 6; i++) {
$('#tab'+i+' a').on('click', function() {
  $('#historydiv').hide();
  $('#trackdiv').hide();
});
}
 
});
</script>



</body>

</html>
