<template>
    <div class="app-learn">
        <ul>
        <div class="box" v-for="(block,i) in blocks" :key="'key'+i">    
        <router-link to="javascript:;">
            <div class="title">{{block.title}}</div>
            <span class="subtitle">{{block.subtitle}}</span>
        </router-link>
         </div>
        </ul> 
    </div>
</template>
<script>
export default {
    data(){
          return{ co:['lightblue','lightgreen','lightycan','lightslategray','lightcoral','lightblue'],
         blocks: [ {title:'ip视频设备，网络安全设备，无线网络设备，疏通网络设备类学习课程',subtitle:'It网络类课程',color:'lightblue'},
         {title:'服务器核心交换机调试维护。机房工程装修建设，强电设备安装，弱电综合布线，视频监控安装维护类学习课程',subtitle:'安防监控课程'},
         {title:'各类智能门锁学习课程',subtitle:'智能门锁课程'},{title:'led屏，单屏，拼接屏，弱电工程类学习课程',subtitle:'商显设备课程'},
         {title:'闸机，娱乐机，售货机，缴费排队机等等学习课程',subtitle:'自助设备课程'},
         {title:'平台规则制度，如何接单录单，如何与客户沟通，如何获得客户的好评，如何提现等学习课程',subtitle:'基础课程'}]
            }
    }
}
</script>
<style>

</style>
