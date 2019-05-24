<template>
    <div>
  	<div class="content">
			<div class="con">
				<router-link to="login">
				<img id="img" src="/img/luban_logo.png" >
				</router-link>
			</div>
			<router-link to="login">
			<div class="btn" id="timer">
					<div id="info">跳过</div>
				<div class="circleProgress_wrapper btn">
					<div class="wrapper right">
						<div class="circleProgress rightcircle"></div>
					</div>
					<div class="wrapper left">
						<div class="circleProgress leftcircle"></div>
					</div>
				</div>
			</div>
			</router-link>
		</div>
        <!---->
    </div>
</template>
<script>
export default {
    data(){
        return{}
    },methods:{
       go(){//bug:如果在其他页面提前跳了，4秒后依旧会飞index。要改，加if
			setTimeout(function(){location.assign("/#/index")},4000);
		}},created() {
			this.go();
		},	
    }


</script>
<style >
* {
	margin: 0;
	padding: 0;
}

html,
body {
	width: 100%;
	height: 100%;
}

.content {
	width: 100%;
	height: 100%;
}

.content .con {
	width: 100%;
	height: 100%;
	font-size: 0;
	display: flex;
	align-items: center;
}

#img {
	width: 100%;
	height: 100%;
	margin-top:-40px;
}

#timer {
	display: inline-block;
	position: fixed;
	top: 40px;
	right: 10px;
}

#info {
	position: absolute;
	top: 0;
	left: 0;
	width: 36px;
	height: 36px;
	line-height: 36px;
	border-radius: 50%;
	background-color: rgba(0, 0, 0, 0.3);
	text-align: center;
	color: #FFFFFF;
	font-size: 12px;
}

.circleProgress_wrapper {
	width: 36px;
	height: 36px;
	position: relative;
	margin-left:-3px;
	margin-top:2px;
}

.wrapper {
	width: 16px;
	height: 36px;
	position: absolute;
	top: 0;
	overflow: hidden;
}

.right {
	right: 0;
}

.left {
	left: 5px;
}

.circleProgress {
	width: 32px;
	height: 32px;
	border: 2px solid #FFFFFF;
	border-radius: 50%;
	position: absolute;
	top: 0;

}

.rightcircle {
	border-top: 2px solid #03A9F4;
	border-right: 2px solid #03A9F4;
	right: 0;
	-webkit-animation: circleProgressLoad_right 4s linear;
	/*动画停留在最后一帧*/
	animation-fill-mode: forwards;
	-moz-animation-fill-mode: forwards;
	-webkit-animation-fill-mode: forwards;
	-o-animation-fill-mode: forwards;
}

.leftcircle {
	border-bottom: 2px solid #03A9F4;
	border-left: 2px solid #03A9F4;
	left: 0;
	-webkit-animation: circleProgressLoad_left 4s linear;
	/*动画停留在最后一帧*/
	animation-fill-mode: forwards;
	-moz-animation-fill-mode: forwards;
	-webkit-animation-fill-mode: forwards;
	-o-animation-fill-mode: forwards;
}

@-webkit-keyframes circleProgressLoad_right {
	0% {
		border-top: 2px solid #03A9F4;
		border-right: 2px solid #03A9F4;
		-webkit-transform: rotate(45deg);
	}

	50% {
		border-top: 2px solid #03A9F4;
		border-right: 2px solid #03A9F4;
		border-left: 2px solid #FFFFFF;
		border-bottom: 2px solid #FFFFFF;
		-webkit-transform: rotate(225deg);
	}

	100% {
		border-left: 2px solid #FFFFFF;
		border-bottom: 2px solid #FFFFFF;
		-webkit-transform: rotate(225deg);
	}
}

@-webkit-keyframes circleProgressLoad_left {
	0% {
		border-bottom: 2px solid #03A9F4;
		border-left: 2px solid #03A9F4;
		-webkit-transform: rotate(45deg);
	}

	50% {
		border-bottom: 2px solid #03A9F4;
		border-left: 2px solid #03A9F4;
		border-top: 2px solid #FFFFFF;
		border-right: 2px solid #FFFFFF;
		-webkit-transform: rotate(45deg);
	}

	100% {
		border-top: 2px solid #FFFFFF;
		border-right: 2px solid #FFFFFF;
		-webkit-transform: rotate(225deg);
	}
}

</style>