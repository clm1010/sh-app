<template>
  <el-container>
    <el-header>
      <my-header></my-header>
    </el-header>
    <div class="slider-container">
      <my-slider></my-slider>
    </div>
    <el-main>
      <nuxt />
    </el-main>
    <el-footer>
      <my-footer></my-footer>
    </el-footer>
    <el-backtop :right="10"></el-backtop>
  </el-container>
</template>
<script>
import MyHeader from '@/components/public/header/index'
import MySlider from '@/components/public/slider/slider'
import MyFooter from '@/components/public/footer/index'
export default {
  components: {
    MyHeader,
    MySlider,
    MyFooter
  },
  data() {
    return {}
  },
  methods: {}
}
</script>
<style lang="stylus" scoped></style>
