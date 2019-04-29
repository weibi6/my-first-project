<!DOCTYPE html>
<html>
<head>
	<title></title>
<style type="text/css">
#box{width: 500px;height:300px;background: rgb(138,54,15);margin:0 auto;position:relative;}
#box1{text-align:center;}
.content{width:450px;height: 250px;border:2px solid green;display:none;background: white;border-radius:30px;position:absolute;left:10px;}
.content img{width:450px;height:250px;border-radius:30px;}
button{background: green;}
.active{background: yellow;}
</style>
</head>
<body>
<div id="box">
<div id="box1">
<button class="active">one</button>
<button>two</button>
<button>three</button>
<button>four</button>
<div class="content" style="display: block;"><img src="2/1.1.jpg"></div>
<div class="content"><img src="2/2.2.jpg"></div>
<div class="content"><img src="2/3.3.png"></div>
<div class="content"><img src="2/4.4.jpg"></div>
</div>
</div>
<script type="text/javascript">
	var btn=document.getElementsByTagName("button");
	var div=document.getElementsByClassName("content");
	for(var i=0;i<btn.length;i++)
	{
		(function(i){
btn[i].onclick=function()
		{
			for(var j=0;j<btn.length;j++)
			{
				btn[j].className="";
				div[j].style.display="none";
			}
			this.className="active";
			div[i].style.display="block";
		}
	})(i)
	}
</script>
</body>
</html>

