<template>
  <div>
    <div class="book-info">
      <el-row>
        <el-col :span="14" class="book-info-left">
          <div class="book-info-title">
            <el-row>
              <el-col :span="18">
                <div class="book-info-name">书籍名称</div>
              </el-col>
              <el-col :span="6">
                <div style="book-download">
                  <el-button type="primary" size="mini">下载书籍</el-button>
                </div>
              </el-col>
            </el-row>
          </div>
          <div class="book-info-summary">
            <el-row :gutter="1">
              <el-col :span="4">
                <el-badge :value="12" class="item">
                  点赞
                </el-badge>
              </el-col>
              <el-col :span="4">
                <el-badge :value="12" class="item">
                  点赞
                </el-badge>
              </el-col>
              <el-col :span="4">
                <el-badge :value="12" class="item">
                  点赞
                </el-badge>
              </el-col>
              <el-col :span="4">
                <a href="/tutorial/1" style="color:red">在线试读</a>
              </el-col>
              <el-col :span="5">
                评分
                <el-rate
                  v-model="value"
                  disabled
                  show-score
                  text-color="#ff9900"
                  score-template="{value}"
                ></el-rate>
              </el-col>
            </el-row>
          </div>
          <div class="book-info-intro">
            <div class="intro-title">
              <span style="padding-left:10px">书籍介绍</span>
            </div>

            <div class="book-info-intro-content">
              。。。。。。
            </div>
          </div>
        </el-col>

        <el-col :span="8" class="book-info-comment">
          <div class="book-comment-title">
            <el-row>
              <el-col :span="18">
                <div class="book-comment-area">评论区</div>
              </el-col>
              <el-col :span="6">
                <div style="book-comment-start">
                  <el-button type="primary" @click="dialogFormVisible = true" size="mini">发表评论</el-button>
                </div>
              </el-col>
            </el-row>
          </div>
          <div class="book-comment-content">
            <el-card class="box-card" shadow="hover">
              <div slot="header" class="comment-username">
                <span>用户名称</span>
                <el-button style="float: right; padding: 3px 0" type="text">回复</el-button>
              </div>
              <div class="text">评论内容</div>
              <div class="comment-time">2020-01-01 00:00 00</div>
            </el-card>
          </div>
          <div class="book-comment-content">
            <el-card class="box-card" shadow="hover">
              <div slot="header" class="comment-username">
                <span>用户名称</span>
                <el-button style="float: right; padding: 3px 0" type="text">回复</el-button>
              </div>
              <div class="text">评论内容</div>
              <div class="comment-time">2020-01-01 00:00 00</div>
            </el-card>
          </div>
          <div class="book-comment-content">
            <el-card class="box-card" shadow="hover">
              <div slot="header" class="comment-username">
                <span>用户名称</span>
                <el-button
                  style="float: right; padding: 3px 0"
                  type="text"
                >回复</el-button>
              </div>
              <div class="text">评论内容</div>
              <div class="comment-time">2020-01-01 00:00 00</div>
            </el-card>
          </div>
        </el-col>
      </el-row>
    </div>
    <el-dialog title="评论" :visible.sync="dialogFormVisible">
      <el-form :model="comment">
        <el-form-item label="评论内容">
          <el-input type="textarea" v-model="comment.info"></el-input>
        </el-form-item>

      </el-form>
      <div slot="footer" class="dialog-footer">
        <el-button @click="dialogFormVisible = false">取 消</el-button>
        <el-button type="primary" @click="dialogFormVisible = false">评 论</el-button>
      </div>
    </el-dialog>
  </div>
</template>
<script>
export default {
  data() {
    return {
      value: 3.7,
      dialogFormVisible: false,
      comment: {
          info: '',
        },
    };
  }
};
</script>

<style>
.book-info-intro-content{
  margin-top: 10px;
}
.comment-username {
  height: 5px;
}
.comment-time {
  font-size: 12px;
  text-align: right;
}
.text {
  font-size: 14px;
  border-bottom: 1px solid #ebebeb;
}
.book-comment-content {
  margin-top: 5px;
}
.book-comment-title {
  border-bottom: 1px solid #ebebeb;
  padding: 5px;
}
.intro-title {
  border-bottom: 1px solid #ebebeb;
}
.book-info-intro {
  border: 1px solid #ebebeb;
  border-radius: 4px;
  padding: 16px;
  margin-top: 30px;
}
.book-info-summary {
  padding: 10px;
  text-align: center;
  margin-left: 60px;
}
.book-info-name {
  padding-top: 3px;
  text-align: center;
  border: 1px solid #ebebeb;
  border-radius: 4px;
  padding: 16px;
  margin-left: 60px;
}
.book-download {
  margin-left: 50px;
  padding: 16px;
}
.book-info-title {
  text-align: center;
}
.book-info {
  margin-left: 80px;
  margin-top: 30px;
}
.book-info-left {
  background-color: white;
  border: 1px solid #ebebeb;
  border-radius: 4px;
  padding: 24px;
}
.book-info-comment {
  margin-left: 50px;
  background-color: white;
  border: 1px solid #ebebeb;
  border-radius: 4px;
  padding: 24px;
}
</style>