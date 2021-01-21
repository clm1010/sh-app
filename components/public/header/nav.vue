<template>
  <div>
    <el-menu
      :default-active="activeIndex"
      class="hidden-xs-only el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
    >
      <el-menu-item index="1">
        <nuxt-link to="/">首页</nuxt-link>
      </el-menu-item>
      <el-submenu index="2">
        <template slot="title">产品中心</template>
        <el-menu-item index="2-1">选项1</el-menu-item>
        <el-menu-item index="2-2">选项2</el-menu-item>
        <el-menu-item index="2-3">选项3</el-menu-item>
        <el-submenu index="2-4">
          <template slot="title">选项4</template>
          <el-menu-item index="2-4-1">选项1</el-menu-item>
          <el-menu-item index="2-4-2">选项2</el-menu-item>
          <el-menu-item index="2-4-3">选项3</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-menu-item index="3">应用领域</el-menu-item>
      <el-menu-item index="4">服务与支持</el-menu-item>
      <el-menu-item index="5"
        ><a href="https://www.ele.me" target="_blank">联系我们</a></el-menu-item
      >
    </el-menu>
    <div class="nav-mini hidden-sm-and-up">
      <div class="nav-mini-title">
        <el-button
          type="defalut"
          plain
          icon="el-icon-menu"
          @click="navMiniShow = !navMiniShow"
        ></el-button>
      </div>
      <div class="nav-mini-body">
        <el-collapse-transition>
          <div v-show="navMiniShow">
            <div class="nav-mini-item">
              <nuxt-link to="/">首页</nuxt-link>
            </div>
            <div
              class="nav-mini-item"
              @click="navProductShow = !navProductShow"
            >
              <a href="javascript:(0);"
                >产品中心
                <i
                  style="border: 1px solid red; width: 10px; height: 10px;display: inline-block;color: blue;"
                  icon="el-icon-caret-bottom"
                ></i
              ></a>
            </div>
            <el-collapse-transition>
              <div v-show="navProductShow">
                <div class="nav-mini-item">
                  <nuxt-link to="/">产品1</nuxt-link>
                </div>
                <div class="nav-mini-item">
                  <nuxt-link to="/">产品2</nuxt-link>
                </div>
                <div class="nav-mini-item">
                  <nuxt-link to="/">产品3</nuxt-link>
                </div>
              </div>
            </el-collapse-transition>
            <div class="nav-mini-item">
              <nuxt-link to="/">应用领域</nuxt-link>
            </div>
            <div class="nav-mini-item">
              <nuxt-link to="/">服务与支持</nuxt-link>
            </div>
          </div>
        </el-collapse-transition>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyNav',
  data() {
    return {
      activeIndex: '1',
      navMiniShow: false,
      navProductShow: false
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath)
    },
    handleOpen(key, keyPath) {
      console.log(key, keyPath)
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>

<style lang="stylus" scoped>
.nav-mini
  position relative
  right 0
  left 0
  z-index 9999
  .nav-mini-title
    height 60px
    line-height 60px
    text-align right
    .el-button
      border-radius 0
      font-size 48px
      line-height 1.2
      padding 0 6px
  .nav-mini-body
    box-shadow 0 4px 6px rgba(10,10,10, 0.6)
    background-color rgba(255,255,255, .8)
    .nav-mini-item
      font-size 20px
      border-bottom 1px solid rgba(200,200,200, .6)
      a
        width 100%
        padding 8px 0
        display inline-block
</style>
