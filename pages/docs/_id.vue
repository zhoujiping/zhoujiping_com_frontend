<template>
  <div class="docs-page">
    <div class="container">
      <el-row class="main-wrapper">
        <el-col :span="5" class="menu-wrapper">
          <div class="doc-title"><img class="doc-icon" src="~/assets/image/doc-icon.png"> 小白基础教程</div>
          <ul class="menu-item-wrapper">
            <li class="menu-item-group">
              <div class="menu-item-group-title">
                第一章: 教程简介
              </div>
              <ul class="menu-item-group-list">
                <li class="sub-menu-item selected">
                  <nuxt-link class="sub-menu-item__link" to="/">
                    1. 布局的布局
                  </nuxt-link>
                </li>
                <li class="sub-menu-item">2. 不是怒拒</li>
              </ul>
            </li>
            <li class="menu-item-group">
              <div class="menu-item-group-title">
                第一章: 教程简介
              </div>
              <ul class="menu-item-group-list">
                <li class="sub-menu-item">
                  <nuxt-link class="sub-menu-item__link" to="/">
                    1. 布局的布局
                  </nuxt-link>
                </li>
                <li class="sub-menu-item">
                  <nuxt-link class="sub-menu-item__link" to="/">
                    2. 速度速度 速度擦拭擦擦撒擦大adfadaafadf
                  </nuxt-link>
                </li>
              </ul>
            </li>
          </ul>
        </el-col>
        <el-col :span="19" class="article-wrapper">
          <p>在真实项目开发中，你可能会需要 Redux 或者 MobX 这样的数据流方案，Ant Design React 作为一个 UI 库，可以和任何 React 生态圈内的数据流方案以及应用框架搭配使用。我们基于 Redux 推出了自己的最佳实践 dva，以及可插拔的企业级应用框架 umi，推荐你在项目中使用。
          </p>
        </el-col>
      </el-row>
    </div>
  </div>
</template>


<script>
export default {
  
}
</script>

<style lang="stylus" scoped>
.main-wrapper
  margin-top: 40px
  margin-bottom: 60px
  .menu-wrapper
    height: 100%
    min-height: 100vh
    overflow: hidden
    font-size: 13px
    border-right: 1px solid #dddddd
    cursor: default
    .doc-title
      font-size: 16px
      font-weight: bold
      color: #333
      .doc-icon
        vertical-align: middle
        margin-top: -3px
        width:25px
    .menu-item-wrapper
      margin-top: 20px
      .menu-item-group-title
        height: 35px
        line-height: 35px
        margin-bottom: 8px
        margin-right: 16px
        color: #333333
        font-weight: bold
        border-bottom: 1px solid #dddddd
      .menu-item-group-list
        padding: 0
        margin: 0 0 10px 0
        list-style: none
        .sub-menu-item
          padding-left: 16px
          height: 35px
          line-height: 35px
          cursor: pointer
          overflow: hidden
          text-overflow: ellipsis
          .sub-menu-item__link
            text-decoration: none
            &:visited
              color: #333
            &:hover
              color: #1890ff
        .selected
          background: #e7f7ff
          border-right: 2px solid #1890ff
          > a
            color: #1890ff

  .article-wrapper
    padding-left: 40px
    line-height: 1.8
</style>