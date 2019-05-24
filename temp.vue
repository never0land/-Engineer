<template>
    <div class="app-temp">
        <header class="mui-bar mui-bar-nav ">
           <div class="header_style">团队</div>
           <span class="header_style2">常见问题</span> 
        </header>
        <div class="mui-card">
				<div class="mui-card-content">
					<div class="mui-card-content-inner">
						<div class="card_title_1">
                            <span class="mui-icon-extra mui-icon-extra-peoples card_png " data-toggle=""></span>
                            <label class="card_font">我是服务商</label>
                        </div>
                       <button type="button" class="mui-btn mui-btn-warning mui-btn-block card_btn">我要创建服务团队</button>
                       <!--创建服务团队说明-->
                       <div class="Explain">
                       <div class="mui-input-row mui-checkbox mui-left " >
						<label>阅读&nbsp;<router-link class="Connect" to="javascript:;">创建服务团队说明</router-link></label>
						<input name="checkbox" value="Item 2" type="checkbox" id="Choice">
                        </div>
                        <!--end--->
					</div>
					</div>
				</div>
			</div>
            <!--下部卡片-->
               <div class="mui-card">
				<div class="mui-card-content">
					<div class="mui-card-content-inner">
						<div class="card_title_1">
                           <span class="mui-icon mui-icon-contact mui-icon-icon-contact-filled card_png"></span>
                            <label class="card_font">我是工程师</label>
                        </div>
                        <input type="text" placeholder="请输入团队编码" class="search_input" autofocus>
                       <button type="button" class="mui-btn mui-btn-primary mui-btn-block card_btn">我要加入团队</button>
                       <!--创建服务团队说明-->
                       <div class="Explain">
                       <div class="mui-input-row mui-checkbox mui-left">
						<label>阅读&nbsp;<router-link class="Connect" to="javascript:;">创建服务团队说明</router-link></label>
						<input name="checkbox" value="Item 2" type="checkbox" >
                        </div>
                        <!--end--->
					</div>
					</div>
				</div>
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
        return{}
    },methods:{	
	}
}
</script>

<style>
header{text-align: center;}
.header_style{margin:10px;}
.header_style2{color:red;font-size: 0.5rem;margin-left:85%;margin-top:-20px;float: left;}
.card_png{margin-right:5px;height: 32px;width:32px;}
.card_font{margin-top:-5px;display: inline-block}
.mui-card-content-inner .card_btn{border-radius: 50px;width:90%;height:10%;margin:0px;padding:5px;margin-left:15px;margin-bottom: 15px;margin-top:10px;}
.Explain{margin-left:40px;}
.Explain .Connect{color:#e28787}
.mui-card-content-inner .search_input{border-radius: 80px;width:93%;margin-left:23px;margin:10px;}
</style>

