<template>
  <div>
    <header>
      <el-menu mode="horizontal" text-color="black">
        <el-menu-item>
          <img src="~/static/img/logo.png" width="300px" height="58px" />
        </el-menu-item>
        <el-menu-item class="myFont" index="1">
          <nuxt-link to="/">首页</nuxt-link>
        </el-menu-item>
        <el-menu-item class="myFont">
          <a href="https://www.ele.me" target="_blank">关于站点</a>
        </el-menu-item>
        <el-menu-item class="myFont">
          <a href="/login"><el-button round class="loginButton">登录</el-button></a>
        </el-menu-item>
      </el-menu>

      <el-menu mode="horizontal" text-color="black">
        <el-menu-item class="myFont" index="1">
          &nbsp;
          <a href="/classify/1">人文社科</a>
        </el-menu-item>
        <el-menu-item class="myFont" index="2"><a href="/classify/2">经管法律</a></el-menu-item>
        <el-menu-item class="myFont" index="3"><a href="/classify/3">小说文艺</a></el-menu-item>
        <el-menu-item class="myFont" index="4"><a href="/classify/4">期刊报纸</a></el-menu-item>
        <el-menu-item class="myFont" index="5"><a href="/"><span style="color:red">首页</span></a></el-menu-item>
      </el-menu>
    </header>
    <nuxt />
    <footer>
      <div class="footer">
        <p>电子书资源库-----------@广东财经大学版权所有</p>
        <p>Copyright ©2015 GDUFE Library. All rights reserved .</p>
        <p>如有问题，请联系管理员小蔡：QQ：xxxxxxxx 电话：xxxxxxxxxxx</p>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: "1"
    };
  }
};
</script>

<style>
a {
  text-decoration: none;
  color: #333;
}
.footer {
  text-align: center;
  font-size: 15px;
  margin-top: 30px;
  background-color: darkslategray;
  color: #fff;
}
.loginButton {
  margin-left: 600px;
}
.myFont {
  font-size: 20px;
  margin-left: 20px;
}
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
