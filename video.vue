<template>
    <div class="app-video">
        <header class="mui-bar mui-bar-nav ">
           <div class="header_style">IT网络类课程</div>
           	 <div class="video_back" style=" float: left;margin-left:0px;margin-top:-30px;width:24px;height:24px;display: inline-block;">
                <a href="#/Training_Institute" class="page-back  router-link-active"><i class="mintui mintui-back"></i></a></div>
        </header>
        <div class="video" >
            
        <video controls="true" name="media" style="width:375px;height:255px;margin-top:-15px;"><source src="http://127.0.0.1:3000/mp4/1.mp4" type="video/mp4" ></video>
        </div>
        <div>
            <ul style="list-style:none;display:flex;margin-bottom:10px;">
                <div style="margin-left:12%;margin-top:5px;" class="lab1">视频
                </div>
                <li style="margin-left:12%;margin-top:5px;" class="lab2" @click="video_m">简介</li>
                <li style="margin-left:12%;margin-top:5px;" class="lab3">资料</li>
                <li style="margin-left:12%;margin-top:5px;" class="lab4">评价</li>
            </ul>
            <div class="video_main">
                <div style="margin-left:10px;">01:易点租服务流程讲解</div>
            </div>
        </div>
        
        
        
        
        
    </div>
</template>
<script>
export default {
    data(){
        return{}
    },methods:{
        video_m(){
            var l1=document.getElementsByClassName(".lab1");
            var l2=document.getElementsByClassName(".lab2");
            var video_main=document.getElementsByClassName(".video_main");
            var html11=`<div style="margin-left:10px;">01:易点租服务流程讲解</div>`
            var html12=`<div style="margin-left:10px;">
                    <h4>神州光大[易点租面签]项目</h4>
                    <span>综合评价: 5|学习人数：892</span>
                    <span>平云小江与神州光大签署战略合作协议，本课程主要介绍了其中一个"易点租面签"项目的作业流程</span>
            </div>`
           
            video_main.innerHTML=html12;

            

        }
    }
}
</script>
<style>
.video .mui-bar video_back{
   }
</style>
