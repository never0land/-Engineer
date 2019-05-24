<template>
    <div class="app-temp">
        <header class="mui-bar mui-bar-nav ">
           <div class="header_style">头条</div>
        </header>
   <div class="mui-content my_headlines_card">
			<div style="padding: 10px 10px;">
				<div id="segmentedControl" class="mui-segmented-control mui-segmented-control-inverted mui-segmented-control-primary ">
					<a class="mui-control-item mui-active" href="#item1">
				全部
			</a>
					<a class="mui-control-item" href="#item2">
				公告
			</a>
					<a class="mui-control-item" href="#item3">
				活动
			</a>
				</div>
			</div>
    <!--1,2,3子项--->
    <ul>
   <div class="mui-card">
		   <a href="">
			 <h3 class="mui-card-title">鲁班工程师</h3> 
			 <h6 class="mui-card-subtitle">lubangongchengshi</h6>
		   </a>
			<div class="mui-card-header mui-card-media" style="background-image:url(../img/8.jpeg)"></div>
				<div class="mui-card-content">
					<div class="mui-card-content-inner">
						<h5><strong>绑定微信仅三步，从此抢单快N步</strong></h5>
						<p style="color: #333;">绑定鲁班工程师平台微信公众号，适合您的工单都会推送给您...</p>
					</div>
				</div>
				<div class="mui-card-footer">
					<a class="mui-card-link">Like</a>
					<a class="mui-card-link">Read more</a>
				</div>
	</div>
  
<!---CARD2---->
 <div class="mui-card">
			<a href="">
			 <h3 style="margin-top:10px;margin-left:4px;color:black">鲁班工程师</h3> 
			 <h6 style="margin-left:10px;margin-top:-5px;font-weidth:16px;">lubangongchengshi</h6>
		   </a>
				<div class="mui-card-header mui-card-media mui-card-img" style="background-image:url(../img/8.jpeg)"></div>
				<div class="mui-card-content">
					<div class="mui-card-content-inner">
						<p>Posted on January 18, 2016</p>
						<p style="color: #333;">这里显示文章摘要，让读者对文章内容有个粗略的概念...</p>
					</div>
				</div>
				<div class="mui-card-footer">
					<a class="mui-card-link">Like</a>
					<a class="mui-card-link">Read more</a>
				</div>
			</div>
</ul>





        </div>
<!---底部选项卡----->
<nav class="mui-bar mui-bar-tab">
        <router-link class="mui-tab-item mui-active" to="/index">
            <span class="mui-icon mui-icon-home"></span>
            <span class="mui-tab-label">主页</span>
        </router-link>
        <router-link class="mui-tab-item" to="/temp">
            <span class="mui-icon mui-icon-extra mui-icon-extra-peoples"></span>
            <span class="mui-tab-label">团队</span>
        </router-link>
        <router-link class="mui-tab-item" to="/Headlines">
            <span class=" mui-icon mui-icon-extra mui-icon-extra-new"></span>
            <span class="mui-tab-label">头条</span>
        </router-link>
        <router-link class="mui-tab-item" to="Training_Institute">
            <span class="mui-icon mui-icon-extra mui-icon-extra-university"></span>
            <span class="mui-tab-label">培训</span>
        </router-link>
        <router-link class="mui-tab-item" to="/login">
            <span class="mui-icon mui-icon-extra mui-icon-extra-addpeople"></span>
            <span class="mui-tab-label">我</span>
        </router-link>
    </nav>
</div>   
         

</template>
<script>
export default {
    data(){
        return{

		}
		methods: {
			
		}
    }
}
</script>
<style>
header{text-align: center;}
.header_style{margin:10px;}
.header_style2{color:red;font-size: 0.5rem;margin-left:85%;margin-top:-20px;float: left;}
.my_headlines_card{margin-top:-50px;background-color: #fff}
.mui-card-title{margin-top:10px;margin-left:4px;color:black}
.mui-card-subtitle{margin-left:10px;margin-top:-5px;font-weight:16px;}
.mui-card-img{height:180px;}

</style>

