<template>
    <div class="app-login">
      <header class="mui-bar mui-bar-nav head">
		    <div class="back">
				 <a href="#/index" class="page-back router-link-active">
         <i class="mintui mintui-back"></i>
         </a>
		    </div>
        <div class="header_style">欢迎来到鲁班工程师</div>
      </header>
      <div class="mui-content my_headlines_card Subheading login-input">
			<div class="mui-control-item  phone-login" href="javascript:;" id="item1" @click="tel">
				手机号登录
			</div>
			<div class="mui-control-item Verification-login" href="javascript:;" id="item2" @click="Verification">
				验证码登录
			</div> 
            <!--账号-->
       <div style="background-color:#fff" >
		   <div id="main">
         	<div class="mui-input-row">
						<input type="text" class="mui-input-clear" placeholder="请输入11位手机号码"  maxlength="11"   id="phone" v-model="phone" autofocus>
					</div>
        <div class="mui-input-row mui-password">
					<input type="password" class="mui-input-password" data-input-password="3" maxlength="6" minlength="6" placeholder="请输入6位密码" id="upwd" v-model="pwd">
				</div>
        </div> 

      <div class="login-btn">
          <button type="button" class="mui-btn mui-btn-yellow mui-btn-block card_btn " @click="btnLogin">
        登录</button>
          </div>
        <!--底部-->
        <div class="bottom">
                <a class="bottom-right">新用户注册</a>|<a class="bottom-left">咨询客服</a></div>
                    <a href="javascript:;" class="Agreement">《鲁班工程师注册协议》</a>
        
        </div> 
        </div>
   </div>
</template>
<script>
 //0:在export  之前引入需要组件
  import {Toast} from "mint-ui"
  export default {
    data(){
      return {
        phone:"",  //双向绑定用户名
        pwd:""    //双向绑定密码
      }
    },
    methods:{
      btnLogin(){
       //功能:获取用户输入用户名和密码
       //验证如果通过发送ajax请求给服务器
       //程序并且获得返回结果 13
       console.log(1);
       //1:获取用户输入用户名和密码
       var phone = this.phone;
       var pwd = this.pwd;
       console.log("2:"+phone+":"+pwd);
       //2:创建正则表达式 
       //   用户名 字母数字下划线 3~8
       var ureg = /^(13[0-9]|14[5|7]|15[0|1|2|3|5|6|7|8|9]|18[0|1|2|3|5|6|7|8|9])\d{8}$/;
       //   密码   数字          3~8
       if(!ureg.test(phone)){
        //3:验证用户名如果失败 提示错误信息
        //console.log("3:验证失败");
        Toast("用户名格式不正确，请检查！");
        return;
       }
       console.log("4");
       //4:验证密码如果失败   提示错误信息
       var preg = /^[0-9]d{6}$/;
      // if(!preg.test(pwd)){
        //Toast("密码格式不正确");
        //return;
       //}
       //5:发送ajax请求 axios
       //在main.js 引入库
       //脚手架 8080   --> app.js 3000
       var url = "http://127.0.0.1:3000";
       url+="/login?phone="+phone+"&pwd="+pwd;
       this.axios.get(url).then(result=>{
        console.log(result.data.code);
         console.log("服务器返回结果");
         //6:获取返回结果
         //7:提示 登录成功或者用户名或密码有误
         if(result.data.code==1){
           Toast("登录成功");
           location.assign("/#/Backstage")
         }else{
           Toast("用户名或密码有误");
         }
       })
	  },

Verification(){
		  var item2=document.getElementById("item2").style;
		  var main=document.getElementById("main");
		  var html=` 		<div class="mui-input-row">
						<input type="text" class="mui-input-clear" placeholder="请输入11位手机号码" pattern="^(13[0-9]|14[5|7]|15[0|1|2|3|5|6|7|8|9]|18[0|1|2|3|5|6|7|8|9])\d{8}$" maxlength="11"   id="phone" v-model="phone" autofocus>
					</div>
            <div class="mui-input-row mui-password">
					<input type="password" class="mui-input-password" data-input-password="3" maxlength="6" minlength="6" placeholder="请输入6位验证码" id="upwd" v-model="pwd">
				</div>`
		  main.innerHTML=html;
		    console.log(main);
	  },tel(){
		    var item1=document.getElementById("item1").style;
		  var main=document.getElementById("main");
		  var html=` 		<div class="mui-input-row">
						<input type="text" class="mui-input-clear" placeholder="请输入11位手机号码" pattern="^(13[0-9]|14[5|7]|15[0|1|2|3|5|6|7|8|9]|18[0|1|2|3|5|6|7|8|9])\d{8}$" maxlength="11"   id="phone" v-model="phone" autofocus>
					</div>
            <div class="mui-input-row mui-password">
					<input type="password" class="mui-input-password" data-input-password="3" maxlength="6" minlength="6" placeholder="请输入6位密码" id="upwd" v-model="pwd">
				</div>`
		    main.innerHTML=html;
		    console.log(main);
	  }
    }
  }
</script>
<style >
.Verification-login{display:inline-block;margin-left:36%;padding:10px;}
.phone-login{display:inline-block;margin-left:4%;padding:10px;border:1px;}
.login-input{margin-top:-20px;background-color:#fff}
.bottom{margin-left:13%;margin-bottom:15px;}
.bottom-left{margin-left:30px;margin-right:30px;color:black}
.bottom-right{margin-left:30px;margin-right:30px;color:black}
.login-btn{background-color:#fff}
  .Agreement{margin-left:24%;color:#e78d38;width: 95%}
	.app-login #phone{line-height: 21px; width: 99%;height: 40px;margin-bottom: 15px;padding: 10px 15px;-webkit-user-select: text;border: 1px solid rgba(0, 0, 0, .2);border-radius: 60px; outline: none;background-color: #fff;
	-webkit-appearance: none;}
	.app-login #upwd{line-height: 21px; width: 99%;height: 40px;margin-bottom: 15px;padding: 10px 15px;-webkit-user-select: text;border: 1px solid rgba(0, 0, 0, .2);border-radius: 60px; outline: none;background-color: #fff;
	-webkit-appearance: none;}
	.app-login .mui-btn{line-height: 21px; width: 99%;height: 40px;margin-bottom: 15px;padding: 10px 15px;-webkit-user-select: text;border: 1px solid rgba(0, 0, 0, .2);border-radius: 60px; outline: none;
	margin-bottom: 75%;margin-top: 15px;
	}
	.back{
		float:left;margin-left:10px;
		margin-top:12px;
		position:absolute;
		z-index: 2;
		color:black;
	}
	.back>a{color:black;}
</style>