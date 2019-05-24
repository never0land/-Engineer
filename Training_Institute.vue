<template>
<div class="app-Training_Institute">
        <!--头条-->
        <header class="mui-bar mui-bar-nav ">
           <div class="header_style">培训学院</div>
        </header>
        <!--头选项卡-->
        <div>
        <div id="segmentedControl" class="mui-segmented-control mui-segmented-control-inverted mui-segmented-control-primary">
                <a href="javascript:;" class="mui-control-item mui-active item"  @click="train_item1">
                    <div class="item1">视频点播</div>
                </a>
                <a href="javascript:;" class="mui-control-item item" @click="train_item2">
                    <div class="item2" >我的学习</div>
                </a>
                <a href="javascript:;" class="mui-control-item item"  @click="train_item3">
                    <div class="item3">资质考试</div>
                </a>
        </div>
        <ul style="liststyle:none;" id="boxs">
        <div  class="box" v-for="(block,i) in blocks" :key="'key'+i">          
        <router-link to="video">
            <div class="title">{{block.title}}</div>
            <span class="subtitle">{{block.subtitle}}</span>
            </router-link>
         </div>
         </ul>
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
</div>
</template>
<script>
export default {
    data(){
        return{ 
       blocks:[{title:'ip视频设备，网络安全设备，无线网络设备，疏通网络设备类学习课程',subtitle:'It网络类课程',color:'lightblue',pic_route:"http://127.0.0.1:3000/img/menu1.png"},
         {title:'服务器核心交换机调试维护。机房工程装修建设，强电设备安装，弱电综合布线，视频监控安装维护类学习课程',subtitle:'安防监控课程',pic_route:"http://127.0.0.1:3000/img/menu2.png"},
         {title:'各类智能门锁学习课程',subtitle:'智能门锁课程',pic_route:'http://127.0.0.1:3000/img/menu3.png'},
         {title:'led屏，单屏，拼接屏，弱电工程类学习课程',subtitle:'商显设备课程',pic_route:'http://127.0.0.1:3000/img/menu4.png'},
         {title:'闸机，娱乐机，售货机，缴费排队机等等学习课程',subtitle:'自助设备课程',pic_route:'http://127.0.0.1:3000/img/menu5.png'},
         {title:'平台规则制度，如何接单录单，如何与客户沟通，如何获得客户的好评，如何提现等学习课程',subtitle:'基础课程',pic_route:'http://127.0.0.1:3000/img/menu6.png'}
            ]}
      },methods:{
          train_item2(){
            var item2=document.getElementsByClassName("box");
            var item2_title=document.getElementsByClassName("title");
            for(var i=0;i<item2.length;i++){
                var i2=document.getElementsByClassName("")  
            }
          var item2_html=`    
           <div  class="box" v-for="(block,i) in blocks" :key="'key'+i">          
        <router-link to="video">
            <div class="title">{{block.title}}</div>
            <span class="subtitle">{{block.subtitle}}</span>
            </router-link>
         </div>`
            item2.innerHTML=item2_html;
            console.log("1112");
      console.log(this.blocks[0].title);
         //console.log(item2);

          },   
           train_item1(){
            var item1=document.getElementsByClassName("box");
            console.log("1111");
          },   
           train_item3(){
            var item3=document.getElementsByClassName("box");
            console.log("1113");
          },
          bgc_color(){
              var r=Math.random()*256;
              var g=Math.random()*256;
              var b=Math.random()*256;
              return r,g,b;
          }

          }
      }
    

</script>
<style>
.box{width: 165px;display:inline-block;font-size: 12px;margin-left:14px;}
.title{border-radius: 8px;padding: 5px;margin:5px;width:155px;height: 115px;margin-top:8px;color:rgb(54, 163, 231);background-color: #f90;}
.subtitle{margin-top:5px;margin-bottom: 5px;margin-left:30px;font-size: 14px;color:lightslategray}
.title2{background-color:#f90;width:270px;margin-left:55px;padding:10px;border-radius:8px;margin-bottom:8px;width:270px;height:100px;}
.subtitle2{margin-left:125px;}
.img2{float:left;width:45px;height:45px;margin-top:13px;}
</style>
