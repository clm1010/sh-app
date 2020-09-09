<template>
  <el-menu
    :default-active="activeIndex"
    class="el-menu-demo"
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
</template>

<script>
export default {
  name: 'MyNav',
  data() {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>

<style lang="scss"></style>
