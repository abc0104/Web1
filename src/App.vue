<template>
  <div id="app">
    <!-- 使用子组件 -->
    <el-container>
      <el-header id="headerBook">
        <Header/>
      </el-header>
      <el-main id="mainBook">
        <!-- <Login/> -->
        <router-view></router-view>
      </el-main>
      <el-footer id="footerBook">
        <Footer/>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
//导入Header子组件
import Header from "./components/Header"
// import Login from "./components/Login"
import Footer from "./components/Footer"
//2、注册 子组件
export default {
  name: 'App',
  components: {
    Header,
    // Login,
    Footer
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
}
#headerBook{
  background-color: #244152;
}
#mainBook{
  /* background-color:blue; */
  height: 450px;
}
#footerBook{
  /* background-color:green; */
  height: 150px !important;
}
</style>
