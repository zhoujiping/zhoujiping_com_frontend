<template>
  <div class="doc">
    <div class="zjp-section">
      <div class="container">
        <div class="title">
          <h2 class="title__h">计算机基础 <i class="el-icon-circle-plus-outline zjp-icon__click" @click="test()"></i></h2>
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
    <!-- 创建文档对话框 -->
    <el-dialog
      title="创建专栏"
      :visible.sync="docDiaLogVisible"
      width="500px">
      <div class="uploader-wrapper">
        <el-upload
          class="cover-uploader"
          :action="actionUrl"
          :headers="uploadHeader"
          name="cover"
          accept="image/png, image/jpeg"
          :show-file-list="false"
          :on-success="handleCoverSuccess"
          :on-progress="()=>(uploadLoading=true)"
          :before-upload="beforeUpload">
          <el-button size="mini" type="primary">上传封面</el-button>
          <span class="font-size:12px;color:#ff5555">「封面的大小为333px * 138px」</span>
        </el-upload>
        <div class="doc-cover-box">
          <img src="~/assets/image/doccover.png">
        </div>
      </div>
      <span slot="footer" class="dialog-footer">
        <el-button size="small" @click="docDiaLogVisible = false">取 消</el-button>
        <el-button size="small" type="primary" @click="docDiaLogVisible = false">确 定</el-button>
      </span>
      <el-form :model="form">
        <el-form-item label="名称">
          <el-input v-model="form.name" autocomplete="off"></el-input>
        </el-form-item>
        <el-form-item label="描述">
          <el-input v-model="form.name" autocomplete="off"></el-input>
        </el-form-item>
        <el-form-item label="排序">
          <el-input v-model="form.name" autocomplete="off"></el-input>
        </el-form-item>
      </el-form>
    </el-dialog>
  </div>
</template>

<script>
import axios from 'axios'
axios.defaults.headers.common['Content-Type'] = 'application/json'
export default {
  name: 'Documents',
  data () {
    return {
      docDiaLogVisible: false,
      form: {}
    }
  },
  methods: {
    test () {
      axios.get('/api/docs/hot').then((res) => {
        console.log(res)
      })
    }
  }
}
</script>

<style lang="stylus" scoped>
.uploader-wrapper
  .doc-cover-box
    width: 335px
    height: 140px
    border: 1px solid #DCDFE6
    background-color: #f5f5fa
    margin-top: 10px
    margin-bottom: 10px
    border-radius: 4px
    > img
      width: 100%
      height: auto
/deep/.el-dialog__header
  padding: 15px 20px
  background-color: #f5f5fa
/deep/.el-dialog__body
  padding: 20px
.el-form-item
  margin-bottom: 10px
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
