<template>
  <div class="site">
    <header class="site-header">
      <div class="container">
        <!-- logo -->
        <a class="logo" href="/"><img class="logo-img" src="~/assets/image/logo.png" alt="周继平的博客"></a>
        <!-- 导航菜单 -->
        <ul class="nav main-menu">
          <li class="nav-item">
            <nuxt-link class="nav-link active" to="/">专栏</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/articles">文章</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/codes">代码片段</nuxt-link>
          </li>
        </ul>
        <!-- 搜索 -->
        <div class="search">
          <input class="search-input" type="text" placeholder="搜索...">
        </div>
        <!-- 注册登录 -->
        <ul class="nav login-menu">
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/doc">注册</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link" to="/doc">登录</nuxt-link>
          </li>
        </ul>
      </div>
    </header>
    <Nuxt />
    <!-- 底部 -->
    <footer class="site-footer">
      <div class="container">
        这里是站点底部
      </div>
    </footer>
  </div>
</template>

<style lang="stylus">
html
  font-family: "Open Sans", "Segoe UI", Helvetica, sans-serif
  font-size: 16px
  word-spacing: 1px
  -ms-text-size-adjust: 100%
  -webkit-text-size-adjust: 100%
  -moz-osx-font-smoothing: grayscale
  -webkit-font-smoothing: antialiased
  box-sizing: border-box

*, *::before, *::after
  box-sizing: border-box
  margin: 0
ol, ul
  padding: 0
  margin: 0
.site
  width: 100%
  background-color: #f5f5fa
  min-height: 100vh

.site-header
  height: 47px
  line-height: 47px
  color: #d7d7d7
  font-size: 14px
  background-color: rgba(0, 0, 0, .9)
  background: url('~assets/image/navbar-bg.png') repeat-x
  .logo
    float: left
    display: block
    width: 150px
    .logo-img
      width: 150px
      vertical-align: middle
      border: 0
  .nav
    float: left
    .nav-item
      display: inline-block
      list-style: none
      .nav-link
        color: #d7d7d7
        text-shadow: 1px 0 1px rgba(0,0,0,0.5)
        text-decoration: none
        padding: 15px 20px 15px 20px
        &:hover
          background-color: rgba(0, 0, 0, .3)
      .active
        background-color: rgba(0, 0, 0, .3)
        color: #ffffff
        border-right: 1px solid #000000
        border-left: 1px solid #000000
  .main-menu
    margin-left: 20px
  .search
    float: left
    margin-left: 30px
    .search-input
      background:rgba(0, 0,0, .3)
      border: none
      color: #7d7d7d
      width: 230px
      font-size: 14px
      height: 30px
      padding: 6px 10px
      margin-bottom: 0
      border-radius: 2px
  .login-menu
    float: right
    .nav-item
      .nav-link
          padding: 15px 10px

.container
  margin: 0 auto
  width: 1080px
  &:before,&:after
    display: table
    line-height: 0
    content: " "
.pull-right
  float:right
.site-footer
  background: url('~assets/image/bottom-bg.png') #202020
  color: #a1a1a1
  padding: 30px 0
.zjp-icon__click
  color: #1890ff
  cursor: pointer
  
  &:hover
    color: #47abfc
</style>
