<template>
  <div id="loginWrapper">
    <div id="loginContent">
        <el-card class="box-card">
        <div slot="header" class="clearfix">
            <span>系统登录</span>
            <el-button style="float: right; padding: 3px 0" type="text">忘记密码</el-button>
        </div>
        <div id="loginContentBody">
            <el-input id="username" v-model="user.username" clearable></el-input>
            <el-input id="password" v-model="user.password" show-password clearable></el-input>
        </div>
        <div id="loginSubmit">
            <el-button id="systemSubmit">登录</el-button>
        </div>
        </el-card>
    </div>
  </div>
</template>

<script>
export default {
    name:"login",
    data(){
        return {
            user:{
                username:"",
                password:""
            }
        }
    },
    methods:{
        loginSystem(){
            Axios.get('/login').then(function(response){
                alret(response.data)
            })
        }
    }
}; 
//导出默认的自变量
</script>

<style>
#loginWrapper {
  /* background-color: red; */
  height: 100%;
}
#loginContent {
    width: 400px;
    margin: 0 auto;
    padding-top: 45px;
}
#systemSubmit {
    display: block;
    margin: 0 auto;
    background: #0a9588;
    color: white;
    border-color: #0a9588;
}
#password {
    margin-top: 5px;
    margin-bottom: 8px;
}
</style>