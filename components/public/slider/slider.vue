<template>
  <el-carousel :height="bannerHeight + 'px'">
    <el-carousel-item v-for="(item, index) in sliderList" :key="index">
      <img
        ref="bannerHeight"
        :src="item.src"
        alt=""
        width="100%"
        @load="imgLoad"
      />
      <!-- <el-image
        ref="bannerHeight"
        :src="item.src"
        alt=""
        width="100%"
        @load="imgLoad"
      ></el-image> -->
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  name: 'MySlider',
  data() {
    return {
      bannerHeight: '',
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
  },
  mounted() {
    this.imgLoad()
    window.addEventListener(
      'resize',
      () => {
        this.bannerHeight = this.$refs.bannerHeight[0].height
        this.imgLoad()
      },
      false
    )
  },
  methods: {
    imgLoad() {
      this.$nextTick(() => {
        this.bannerHeight = this.$refs.bannerHeight[0].height
      })
    }
  }
}
</script>

<style lang="stylus" scoped></style>
