<template>
    <div class="app-Backstage">
        <div class="data">
            <div class="data-right" style="float:left;">
                <img src="http://127.0.0.1:3000/img/menu6.png" alt="暂时不知道你脑袋长啥样" style="width:90px;height:90px;margin:20px;margin-left:20px;">
            </div>
            <div class="data-left" style="margin-top:30px;margin-left:15px;float:left;" >
                <ul> 
                <div style="margin:3px;">姓名</div>
                <div style="margin:3px;">工号</div>
                <div style="margin:3px;">账号</div>
                </ul>
            </div>
               </div>
                <ul class="door" style="display:inline-flex;margin-left:45px;">
                    <div style="width:120px;height:60px;padding:10px;">
                       <a class="active" style="display:block">
                           <span class="mui-icon-extra mui-icon-extra-gold">
                               </span>
                               </a>
                                <div style="margin-left:-7px;">钱包</div>
                        </div>
                   <div style="width:120px;height:60px;padding:10px;">
                         <a class="active">
                            <span class="mui-icon mui-icon-chat"></span>
                                 </a>
                                <div style="margin-left:-4px;">消息</div>
                    
                        </div>
                  <div style="width:120px;height:60px;padding:10px;">
                    <a id="icon-info" class="active">
                     <span class="mui-icon mui-icon-info-filled"></span>
                    </a>
                        <div style="margin-left:-10px;">信用值</div>
                        </div>
                </ul>
     
        <!--无聊框框-->
    <ul class="mui-table-view" style="font-size:8px;">
				<li class="mui-table-view-cell mui-media">
					<a href="javascript:;" class="">
						<img class="mui-media-object mui-pull-left" src="">
					<a id="icon-icon-contact">
                        <span class="mui-icon mui-icon-contact">
                           <span style="margin-left:18px;">实名验证</span> 
                            </span>
                            </a>
					</a>
				</li>
				<li class="mui-table-view-cell mui-media">
					<a href="javascript:;">
						<img class="mui-media-object mui-pull-left" src="">
					<a >
                        <span class="mui-icon mui-icon-compose active">
                            <span style="margin-left:18px;">个人信息</span> 
                            </span>
                            </a>
					</a>
				</li>
				<li class="mui-table-view-cell mui-media">
					<a href="javascript:;">
						<img class="mui-media-object mui-pull-left" >
					<a >
                        <span class="mui-icon-extra mui-icon-extra-order">
                        <span style="margin-left:18px;">常见问题</span> 
                        </span>
                        </a>	
					</a>
				</li>
                <li class="mui-table-view-cell mui-media">
					<a href="javascript:;">
						<img class="mui-media-object mui-pull-left" >
					<a >
                        <span class="mui-icon-extra mui-icon-extra-peoples">
                        <span style="margin-left:18px;">关于鲁班工程师</span> 
                        </span>
                        </a>
					</a>
				</li>
               <li class="mui-table-view-cell mui-media">
					<a href="javascript:;">
						<img class="mui-media-object mui-pull-left" >
                    <a >
                        <span class="mui-icon-extra mui-icon-extra-gold">
                            <span style="margin-left:18px;">接单说明</span> 
                            </span>
                            </a>
					</a>
				</li>
                        <li class="mui-table-view-cell mui-media">
					<a href="javascript:;">
						<img class="mui-media-object mui-pull-left" >
                            <a id="icon-gear" >
                                <span class="mui-icon mui-icon-gear-filled">
                                    <span style="margin-left:18px;">设置</span> 
                                    </span>
                                    </a>
					</a>
				</li>
			</ul>
        <!---无聊框框 end-->
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
        <router-link class="mui-tab-item" to="/Backstage">
            <span class="mui-icon mui-icon-extra mui-icon-extra-addpeople"></span>
            <span class="mui-tab-label">我</span>
        </router-link>
    </nav>
 



    </div>
</template>
<script>
export default {
    data(){
        return{}
    },methods:{
            btnLogin(){
       //功能:获取用户输入用户名和密码
       //验证如果通过发送ajax请求给服务器
       //程序并且获得返回结果 13
       console.log("进入成功");
       //1:获取用户输入用户名和密码
      
       console.log("2:"+phone+":"+pwd);
    
      var phone;
      var pwd;
       //5:发送ajax请求 axios
       //在main.js 引入库
       //脚手架 8080   --> app.js 3000
       var url = "http://127.0.0.1:3000";
       url+="//Backstage?phone="+phone+"&pic_router="+pwd;
       this.axios.get(url).then(result=>{
        console.log(result.data.code);
         console.log("服务器返回结果");
         //6:获取返回结果
         //7:提示 登录成功或者用户名或密码有误
         if(result.data.code==1){
           Toast("登录成功");
           location.assign("/#/index")
         }else{
           Toast("用户名或密码有误");
         }
       })
   
	  }






    }
}
</script>
<style>
.mui-table-view li a a span span{font-size: 14px;color:black}
</style>
