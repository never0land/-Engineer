<template>
    <div class="app-index">
        <!---search--->
        <div class="app-header">
        <div class="app-selector">全国</div>
      <input type="text" placeholder="搜索" class="app-search" autofocus>
     <router-link class="msg" to="javascript:;">
         <span class="mui-icon-extra mui-icon-extra-comment">
             </span>
             </router-link>
        </div>
        <!--search end---->
        <!--swiper----->
            <div class="text-xs-center box" style="width:90%;margin-left:12%;background-color: #fff;">
             <div v-swiper:mySwiper="swiperOption" class="inbox">
               <div class="swiper-wrapper">
                  <div class="swiper-slide" v-for="(banner,i) in banners" :key="'key'+i">
                   <img class='boxitem' :src="banner">
                 </div>
               </div>
               <div class="swiper-pagination"></div>
             </div>
         </div>
<!---swiper end---->
         <!---弹性1--->
         <div class="indexproject_main">
            <div class="swiper_box1">
                <h5>项目招募</h5>
                <strong class="box-title">1个</strong>
                <p class="box-subtitle">最新招募</p>
                <img class="box-img" src="/img/car1.png">
            </div>
            <div class="swiper_box2">
                    <h5 >信用分</h5>
                <strong class="box-title">80分</strong>
                <p class="box-subtitle">信用:一般</p>
                <img src="/img/car2.png" class="box-img">
            </div>
            <div class="swiper_box3">
                    <h5>能力值</h5>
                <strong class="box-title">300分</strong>
                <p class="box-subtitle">心灵手巧</p>
                <img src="/img/car3.png" class="box-img">
            </div>
         </div>
         <!---弹性end--->
         <!-----namecar1----->
         <div class="mui-card " @click="Secret" >
				<div class="mui-card-content">
					<div class="mui-card-content-inner">
						<div class="card_title_1">
                           <img src="/img/namecar1.png" >
                           <div class="car-content">
                            <label class="card_font">一体机广告机商用</label>
                            <div>服务难度:☆☆☆☆☆</div>
                            <div>服务类型：单屏安装</div>
                            <div >工单号：T190151244121242</div>
                        </div>
                            <span class="car-address">广东广州市黄埔区城中...</span>
                                <button type="button" class="mui-btn mui-btn-primary mui-btn-block card_btn index-mui-btn" >接单</button>
                        </div>
                        </div>
                    </div>
                </div>
         <!--namecar end---->
          <!-----namecar2----->
          <div class="mui-card">
				<div class="mui-card-content">
					<div class="mui-card-content-inner">
						<div class="card_title_1">
                           <img src="/img/namecar1.png">
                             <div class="car-content">
                            <label class="card_font">一体机广告机商用</label>
                            <div>服务难度:☆☆☆☆☆</div>
                            <div>服务类型：单屏安装</div>
                            <div>工单号:T190151244121242</div>
                        </div>
                            <span class="car-address">广东广州市黄埔区城中...</span>
                            <div>
                                <button type="button" class="mui-btn mui-btn-primary mui-btn-block card_btn index-mui-btn">接单</button>
                            </div>
                        </div>
                        </div>
                    </div>
                </div>
         <!--namecar end---->
          <!-----namecar3----->
          <div class="mui-card" >
				<div class="mui-card-content">
					<div class="mui-card-content-inner">
						<div class="card_title_1">
                           <img src="/img/namecar1.png" >
                           <div class="car-content">
                            <label class="card_font">一体机广告机商用</label>
                            <div>服务难度:☆☆☆☆☆</div>
                            <div>服务类型：单屏安装</div>
                            <div>工单号:T190151244121242</div>
                        </div>
                            <span class="car-address">广东广州市黄埔区城中...</span>
                            <div>
                                <button type="button" class="mui-btn mui-btn-primary mui-btn-block card_btn index-mui-btn" >接单</button>
                            </div>
                        </div>
                        </div>
                    </div>
                </div>
                <!---客服框框 start---->
              
                <!-----客服 end------>
         <!--namecar end---->
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
import Vue from 'vue'
if (process.browser) {
  const VueAwesomeSwiper = require('vue-awesome-swiper/dist/ssr')
  Vue.use(VueAwesomeSwiper)
}
import 'swiper/dist/css/swiper.css'
 import {Toast} from "mint-ui"
  export default {
    data() {
      return {
        banners:[ '/img/swiper1.png', '/img/swiper2.png'],
        swiperOption: {
          effect:'cube',
          autoplay:true,
          delay:3000,
          speed:800,
          pagination: {
            el: '.swiper-pagination',
            dynamicBullets: true
          },
        },
      }
    },methods:{
        Secret(){
           Toast("请电联签署保密合约");
        },
        created() {
			this.Login();
		},
    Login(){
       console.log(1);
	  },
    }
  }      
</script>
<style>
/*box1*/
.swiper_box1{background-color: #ff9f8f;width: 95px;height:85px;margin:5px;margin-left:10%;display: inline-block}
.swiper_box1>h5{color:lightcyan;margin-left:5px;margin-top:7px;}

/*public*/
.box-title{font-size: 14px;margin-left:5px;}
.box-subtitle{margin-left:5px;color:black;margin-bottom: 7px;margin-top:3px;}
.box-img{width:24px;height:24px;float:left;margin-left:65px;margin-top:-50px}
.mui-card-content-inner .index-mui-btn{background-color:#bdc626;border:0px;color:black;width:60px;float:left;margin-left:250px;margin-top:-100px;}
.car-content{margin-left:100px;margin-top:-60px;}
.car-address{margin-left:10px;margin-top:5px;}

/*box2*/
.swiper_box2{background-color: #98abf1;width: 95px;height:85px;margin:5px;display: inline-block}
.swiper_box2>h5{margin-left:5px;color:lightblue;margin-top:7px;}

/*box3*/
.swiper_box3{background-color: #82d6fc;width: 95px;height:85px;margin:5px;display: inline-block}
.swiper_box3>h5{margin-left:5px;color:#fff;margin-top:7px;}






.indexproject_main{background-color: #fff;}
 .app-index .app-header .app-selector{display:inline;margin-left:20px;}
 .app-index .app-header .app-search{width:65%;margin:10px;}
.app-index{background-color: #fff;}
.app-index>.header>.search{width:70%;margin-left: 10px;margin-right: 10px;}
.app-index>.header>.msg>span{margin-top:0px;}
</style>