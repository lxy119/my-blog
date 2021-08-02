<template>
  <div id="AppNav">
    <div class="content">
      <!--logo-->
      <div class="logo">
        <a href="/">afei.fun</a>
      </div>
      <!--导航-->
      <div class="nav">
        <router-link to="/">首页</router-link>
        <router-link to="/article">文章</router-link>
        <router-link to="/message">留言</router-link>
        <router-link to="/daily">生活</router-link>
        <router-link to="/link">友链</router-link>
        <router-link to="about">关于</router-link>
      </div>
      <!--登陆注册-->
      <div class="user">
        <el-button class="login" type="primary" size="mini">登陆</el-button>
        <el-button class="register" type="success" size="mini">注册</el-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppNav"
}
</script>

<style lang="less" scoped>
#AppNav{
  width: 100%;
  height: 50px;
  background-color: #fff;
  box-shadow: 0 0 2px #999;

  .content{
    display: flex;
    justify-content: space-between;
    box-sizing: border-box;
    width: 100%;
    height: 100%;
    max-width: 1300px;
    padding: 0 15px;
    //background-color: pink;
    margin: 0 auto;

    /*logo*/
    .logo{
      width: 130px;
      height: 50px;
      a{
        display: block;
        width: 100%;
        height: 100%;
        line-height: 42px;
        font-size: 26px;
        letter-spacing: 5px;
        font-family: "Pacifico","serif";
        color: rgba(0,0,0,.7);
      }
    }

    /*导航*/
    .nav{
      width: 470px;
      height: 50px;
      //background-color: aquamarine;
      a{
        float: left;
        display: block;
        height: 98%;
        border-bottom: 2px solid transparent;
        padding: 0 25px;
        color: #777;
        line-height: 48px;
        font-weight: bolder;
        transition: all .3s;

        &.router-link-exact-active{
          color: #00b7ff;
          border-color: #00b7ff;
        }

        &:hover{
          color: #00b7ff;
        }
      }

    }

    /*登陆与注册*/
    .user{
      width: 125px;
      height: 50px;
      //background-color: antiquewhite;
      .el-button{
        display: block;
        margin-top: 11px;
      }
      .login{
        float: left;
      }
      .register{
        float: right;
      }
    }

  }

}


</style>














