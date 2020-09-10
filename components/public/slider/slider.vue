<template>
  <el-carousel :height="sliderHeight + 'px'">
    <el-carousel-item v-for="(item, index) in sliderList" :key="index">
      <img :src="item.src" alt="" />
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  name: 'MySlider',
  props: {
    sliderHeight: {
      type: Number,
      default: () => {
        return 600
      }
    }
  },
  data() {
    return {
      sliderList: [
        {
          url: '#abc',
          src: '/img/slider-01.jpg'
        },
        {
          url: '#abc',
          src: '/img/slider-02.jpg'
        },
        {
          url: '#abc',
          src: '/img/slider-03.jpg'
        },
        {
          url: '#abc',
          src: '/img/slider-04.jpg'
        },
        {
          url: '#abc',
          src: '/img/slider-05.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped></style>
