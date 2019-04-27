# my-first-project
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="keywords" cintent="">
	<title>js之手风琴</title>
<style>
	body{margin:0;}
	body,html{position:relative;height:100%;}
	p{margin:0;}
	ul{list-style: none;margin:0;padding-left:0;}
	.wrap{position:absolute;width:100%;height:100%;background:url("image/1.jpg") no-repeat center/cover;}
    .wrap:nth-child(2){
    	background-image: url("image/2.jpg");
    }
    .wrap:nth-child(3){
    	background-image: url("image/3.jpg");
    }
    .wrap:nth-child(4){
    	background-image: url("image/4.jpg");
    }
    .content{position:absolute;top:50%;left:50%;width:1089px;height:429px;transform:translate(-50%,-50%);}
    .list{
    	width:100px;
    	height:429px;
    	background-image:url("image/1.jpg");
    	float:left;
    }
    .list:nth-child(2){
    	background-image:url("image/2.jpg");
    }
    .list:nth-child(3){
    	background-image:url("image/3.jpg");
    }
    .list:nth-child(4){
        width: 789px;
    	background-image:url("image/4.jpg");
    }
    .list div{
       width:100px;
       height:429px;
       background-color: rgba(0,0,0,0.5);
    }
    .list div p{
    	padding:10px 40px;
    	color:rgba(255,255,255,0.5);
        font-size:35px;
    }
</style>
</head>
<body>
    <div class="wrap"></div>
    <div class="wrap"></div>
    <div class="wrap"></div>
    <div class="wrap"></div>
    <div class="content">
    	<ul>
    		<li class="list">
    			<div>
    				<p>我的小旅行 || 故事一</p>
    			</div>
    		</li>
    		<li class="list">
    			<div>
    				<p>我的小旅行 || 故事二</p>
    			</div>
    		</li>
    		<li class="list">
    			<div>
    				<p>我的小旅行 || 故事三</p>
    			</div>
    		</li>
    		<li class="list">
    			<div>
    				<p>我的小旅行 || 故事四</p>
    			</div>
    		</li>
    	</ul>
    </div>
    <script src="https://code.jquery.com/jquery-3.4.0.js"></script>
    <script>
    	var li=$(".list");
    	li.click(function(){
    		var index=$(this).index()
    		$(this).stop().animate({
           width:"789px"
    		},200).siblings("li").stop().animate({
            width:"100px"
    		},200);
    		$(".wrap").eq(index).fadeIn().siblings(".wrap").fadeOut();
    	})
    </script>
</body>
</html>
