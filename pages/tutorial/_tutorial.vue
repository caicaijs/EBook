<template>
  <div>
    <el-row>
      <el-col :span="16">
        <div class="book-tutorial">
          <div>
            <el-row>
              <el-col :span="20">
                <div class="book-tutorial-title">XXXX书籍在线试读</div>
              </el-col>
            </el-row>
          </div>

          <div class="video-tutorial">
            <p>视频讲解</p>
            <!-- <a href="#" style="float:right">下载视频</a> -->
          </div>
          <div class="video-tutorial-play">
            <video width="500" height="300" controls="controls" src="http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4"></video>
          </div>
          <div class="article-tutorial">
            <p>图文讲解</p>
          </div>
          <div>
            <el-row>
              <el-col :span="23">
                  <div class="article-tutorial-play">内容</div>
              </el-col>
            </el-row>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>
<script>
export default {
  
}
</script>
<style>
.article-tutorial-play{
  border-radius: 3px;
  border: 1px solid #ebebeb;
  padding: 10px;
  margin-left: 50px;
}
.article-tutorial{
  font-size: 19px;
  margin: 80px;
  padding: 10px;
  margin-top: 10px;
}
.video-tutorial-play{
  text-align:center;
}
.video-tutorial{
  font-size: 19px;
  margin: 80px;
  padding: 10px;
}
.book-tutorial-title{
  border-radius: 3px;
  border: 1px solid #ebebeb;
  text-align: center;
  padding: 10px;
  margin-left: 150px;
  font-size: 20px;
}
.book-tutorial{
  padding: 24px;
  border-radius: 3px;
  border: 1px solid #ebebeb;
  margin-left: 200px;
  margin-top: 20px;
}
</style>