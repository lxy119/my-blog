<template>
  <div id="app">
    <!--顶部-->
    <div class="header">
      <AppNav></AppNav>
    </div>
    <!--底部-->
    <div class="footer">
      <!--侧边栏-->
      <AppSide></AppSide>
      <!--内容部分-->
      <div class="f-content">
        <router-view/>
      </div>
    </div>
    <!--备案号-->
    <p class="copyright">湘ICP备19002644号</p>
  </div>
</template>

<script>
import AppNav from "@/components/AppNav";
import AppSide from "@/components/AppSide";
export default {
  components: {
    AppNav,AppSide
  }
}
</script>

<style lang="less">
@import "./assets/css/reset.css";
@import "./assets/css/font.css";
@import "./assets/css/font/iconfont.css";



body{
  background: url("./assets/img/bg/bg-left.png") no-repeat left 50px,
              url("./assets/img/bg/bg-right.png") no-repeat right 50px;
  background-color: rgb(242,242,242);
}

html,body{
  min-width: 850px;
}

#app{
  width: 100%;
  height: 2000px;
  >.header{
    position: fixed;
    z-index: 9;
    top: 0;
    left: 0;
    width: 100%;
    min-width: 850px;
    height: 50px;
  }
  >.footer{
    display: flex;
    box-sizing: border-box;
    width: 100%;
    max-width: 1300px;
    padding: 0 15px;
    margin: 65px auto 0;

    >.f-content{
      flex: 1;
      //background-color: #c2e8ee;
    }
  }
  >.copyright{
    padding: 20px 0;
    font-weight: 400;
    text-align: center;
    font-size: 12px;
    letter-spacing: 2px;
  }
}
</style>
