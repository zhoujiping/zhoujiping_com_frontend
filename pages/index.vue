<template>
  <div class="doc">
    <div class="zjp-section">
      <div class="container">
        <div class="title">
          <h2 class="title__h">计算机基础 <i class="el-icon-circle-plus-outline zjp-icon__click"></i></h2>
          <p class="title__sub">计算机基础知识是每个程序员必须要学习并掌握的</p>
        </div>
        <el-row :gutter="38" class="zjp-card">
          <el-col class="zjp-card__item" :span="8" v-for="(o, index) in 6" :key="index">
              <el-card :body-style="{ padding: '0px' }" shadow="hover">
                <nuxt-link to="/docs/1">
                  <img class="image" src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" >
                </nuxt-link>
                <div class="zjp-card-content">
                    <h3 class="zjp-card-content__h3">
                      <nuxt-link class="link" to="/docs/1">小白兔的开发之路</nuxt-link>
                    </h3>
                  <p class="zjp-card-content__sub">从零开始学开发从零开始学开发</p>
                </div>
                <div class="meta">
                  <span>更新: 2020-07-23</span>
                  <span class="pull-right">
                      文章: 1篇
                      <i class="el-icon-edit-outline zjp-icon__click"></i>
                      <i class="el-icon-delete zjp-icon__click"></i>
                      </span>
                </div>
              </el-card>
          </el-col>
        </el-row>
      </div>
    </div>
   <div class="zjp-section">
      <div class="container">
        <div class="title">
          <h2 class="title__h">前端开发</h2>
          <p class="title__sub">HTML5、JavaScript、Vue.js</p>
        </div>
      </div>
    </div>
    <div class="zjp-section">
      <div class="container">
        <div class="title">
          <h2 class="title__h">后端开发</h2>
          <p class="title__sub">PHP、Lavel</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="stylus" scoped>
.zjp-section:nth-child(even)
  background-color: #f4f4f4
  background: url('~assets/image/white-noise.png')
.zjp-section:nth-child(odd)
  background-color: #f6f6fa
.zjp-section
  padding: 60px 0
  min-height: 500px
  .title
    text-align: center
    margin-bottom: 50px
  .title__h
    font-size: 38px;
    font-weight: 300
    line-height: 1.2
    margin-bottom: 20px
    color: #333333;
  .title__sub
    font-size: 16px;
    color: #666666
  .image
    width: 333px
    height: 138px
.zjp-card
  .zjp-card__item
    margin-bottom: 38px
  .zjp-card-content
    text-align: center
    padding: 10px;
  .zjp-card-content__h3
    font-size: 20px
    line-height: 40px
    .link
      color: #333
      text-decoration: none
      &:hover
        text-decoration: underline
  .zjp-card-content__sub
    font-size: 16px
    line-height: 16px
    color: #666666
    margin-bottom: 20px
  .meta
    font-size: 14px
    padding: 10px
    color: #888888
    border-top: 1px solid #f1f1f1

</style>
