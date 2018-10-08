# jamboe.net
<html>
<head>
<meta http-equiv="Content-type" content="text/html;charset=UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>QR SCAN</title>
<style type="text/css">
.parent{
background: url('scan-icon.gif') no-repeat center; 
 position: absolute;
 display:block;
  top: 0;
  left: 0;
  }
.modal {
display: none; 
position: fixed; 
z-index: 1;
padding-top: 30px;
left: 0;
top: 0;
width: 100%; 
height: 100%; 
overflow: auto; 
background-color: rgb(0,0,0); 
background-color: rgba(0,0,0,0.4); 
}
.modal-content {
background-color: #000;
margin: auto;
padding: 10px;
border: 2px solid #111;
width: 260px;
-moz-border-radius:3px; 
-khtml-border-radius:5px; 
-webkit-border-radius:5px ; 
border-radius:5px ;
color:red;
font-weight:bold
}
.close {float: right;
font-size: 15px;
font-weight: bold;}
.close:hover,.close:focus {
text-decoration: none;
cursor: pointer;
}
#mainbody{
width:100%;
display:none;
}
.selector{
	display:none;
	visibility: hidden;
}
#result{
display:none;
	visibility: hidden;
}

#v{
width:240px;
height:200px;
}
#qr-canvas{
display:none;
}
#outdiv{
padding:0;
width:240px;
height:200px;
border: solid;
border-width: 3px 3px 3px 3px;
-moz-border-radius:3px; 
-khtml-border-radius:5px; 
-webkit-border-radius:5px ; 
border-radius:5px ;
color:#555;
background: #000;
}
.tsel{
padding:0;
}
blink {
    -webkit-animation: 2s linear infinite condemned_blink_effect; // for android
    animation: 2s linear infinite condemned_blink_effect;
}
@-webkit-keyframes condemned_blink_effect { // for android
    0% {
        visibility: hidden;
    }
    50% {
        visibility: hidden;
    }
    100% {
        visibility: visible;
    }
}
@keyframes condemned_blink_effect {
    0% {
        visibility: hidden;
    }
    50% {
        visibility: hidden;
    }
    100% {
        visibility: visible;
    }
}
</style>
<script type="text/javascript" src="llqrcode.js"></script>
<script type="text/javascript" src="webqr.js"></script>
</head>
<body>
<button style="margin-right:10px; width: 120px;height: 35px;background: #888;border: 2px solid #999;cursor: pointer;border-radius: 2px;	color: #fff;font-family: 'Open Sans', sans-serif;font-size: 16px;font-weight: bold;padding: 6px;margin-top: 10px;" id="myBtn">QR SCAN</button>




<div id="myModal" class="modal">
<div class="modal-content">
<center><span class="scanning">▒▒▒▒▒▒▒<blink> ▓ scanning ▓ </blink>▒▒▒▒▒▒▒</span></center>
<div id="mainbody">
<div class="selector" id="webcamimg" onclick="setwebcam()" align="left" ></div>
<table class="tsel" border="0" width="100%">
<td valign="top" align="center" width="50%">
<table class="tsel" border="0">
<td colspan="1" align="center">
<div id="outdiv"></div>
</td>
</table>
</td>
<div id="result"></div>
</table>
<span class="close"></span>
<center><span style="font-weight:bold;font-size:12px; color:#999;">Scan QR code yang ada pada vouhcer anda</span></center>
</div>
<canvas id="qr-canvas" width="100%" height="100%"></canvas>
</div>
</div>
<script type="text/javascript">
var modal = document.getElementById('myModal');
var btn = document.getElementById("myBtn");
var span = document.getElementsByClassName("close")[0];
btn.onclick = function() {
modal.style.display = "block";
}
span.onclick = function() {
modal.style.display = "none";
}
window.onclick = function(event) {
if (event.target == modal) {
modal.style.display = "none";
}
}
</script>
<script type="text/javascript">load();</script>
</body>
</html>
