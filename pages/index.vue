<template>
  <div>
    <div class="main">
      <section class="center-section">
        <div class="carousel-wrap" >
            <div class="grid-content bg-purple">
              <el-carousel :interval="4000" type="card" height="450px" style="padding-top:50px">
                <el-carousel-item v-for="item in 4" :key="item">
                  <a :href="'/ebook/'+item"><img src="~/static/img/logo.png" width="100%" height="100%" /></a>
                </el-carousel-item>
              </el-carousel>
            </div>
        </div>
        <div class='recent-books-wrap' style="margin-left:40px">
            <ul>
              <li>
                <div class="new-book-list">最新书籍</div>
              </li>
              <li v-for="(o,index) in 3" :key="o">
                <el-card :body-style="{ padding: '0px' }">
                  <a :href="'/ebook/'+index"><img src="~/static/img/logo.png" class="image" /></a>
                  <div style="padding: 14px;">
                    <span>好吃的汉堡</span>
                    <div class="bottom clearfix">
                      <time class="time">2020-01-01</time>
                      <el-button type="text" class="button">下载</el-button>
                    </div>
                  </div>
                </el-card>
              </li>
            </ul>
        </div>
      </section>

      <section class="recommend-wrap">
        <div class="hot-book-list">
              推荐书籍
        </div>
        <div class="book-list-wrap">
          <div  class="book-list" v-for="(o, index) in 10" :key="o">
            <el-card :body-style="{ padding: '0px' }">
              <a :href="'/ebook/'+index"><img src="~/static/img/logo.png" class="image" /></a>
              <div style="padding: 14px;">
                <span>好吃的汉堡</span>
                <div class="bottom clearfix">
                  <time class="time">2020-01-01</time>
                  <el-button type="text" class="button">下载</el-button>
                </div>
              </div>
            </el-card>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  }
};
</script>

<style>
.center-section {
  display: flex;
}
.carousel-wrap {
  flex: 2;
}
.recent-books-wrap {
  flex: 1;
}
.recommend-wrap {
  display: flex;
  flex-direction: column;
}
.book-list-wrap{
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}

.book-list {
  width: 300px;
  margin-top: 20px;
  margin-left: 20px
}
.new-book-list{
  font-size: 20px;
  font-family: "微软雅黑";
  margin-left: 5px;
  margin-bottom: 10px;
  border-bottom: 1px solid #ebebeb;
}
.hot-book-list{
  width: 800px;
  font-size: 20px;
  font-family: "微软雅黑";
  margin-left: 10px;
  border-bottom: 1px solid #ebebeb;
}
ul li{
  list-style-type: none;
}
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  height: 105px;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both;
}
.main {
  margin-top: 10px;
  margin-left: 30px;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

</style>
