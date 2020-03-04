<template>
  <div>
    <div style="margin-left:50px">
      <el-low :gutter="20">
        <el-col
          :span="4"
          class="book-list"
          v-for="(o, index) in 10"
          :key="o"
          :offset="index > 0 ? 0 : 0"
        >
          <el-card :body-style="{ padding: '0px' }">
            <img src="~/static/img/logo.png" class="image" />
            <div style="padding: 14px;">
              <span>好吃的汉堡</span>
              <div class="bottom clearfix">
                <time class="time">2020-01-01</time>
                <el-button type="text" class="button">下载</el-button>
              </div>
            </div>
          </el-card>
        </el-col>
      </el-low>
    </div>
    <div style="margin-top:30px;text-align:center">
      <el-pagination background layout="prev, pager, next" :total="total" :page-size="pageSize"></el-pagination>
    </div>
  </div>
</template>
<script>
import "~/assets/style.css";
export default {
  data() {
    return {
      pageSize: 6,
      total: 30
    };
  }
};
</script>