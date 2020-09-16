<template>
  <el-row :gutter="10">
    <el-col
      v-for="(item, index) in fieldImgData"
      :key="index"
      :xs="8"
      :sm="8"
      :md="8"
      :lg="1"
      :xl="1"
    >
      <el-card
        shadow="hover"
        :body-style="{ padding: '0px' }"
        @mouseenter.native="handlMouseOver(index)"
        @mouseleave.native="handlMouseLeave(index)"
      >
        <el-image :src="item.src">
          <div slot="error" class="image-slot">
            <i class="el-icon-picture-outline"></i>
          </div>
        </el-image>
        <div :class="index == current ? 'active' : ''" class="text-desc">
          {{ item.text }}
        </div>
      </el-card>
    </el-col>
  </el-row>
</template>

<script>
export default {
  name: 'Field',
  components: {},
  data() {
    return {
      current: -1,
      fieldImgData: [
        {
          id: 1,
          src: '/img/field-01.jpg',
          text: '仓储物流'
        },
        {
          id: 2,
          src: '/img/field-02.jpg',
          text: '仓储物流'
        },
        {
          id: 3,
          src: '/img/field-03.jpg',
          text: '仓储物流'
        },
        {
          id: 4,
          src: '/img/field-04.jpg',
          text: '仓储物流'
        },
        {
          id: 5,
          src: '/img/field-05.jpg',
          text: '仓储物流'
        }
      ],
      active: ''
    }
  },
  methods: {
    handlMouseOver(index) {
      this.current = index
    },
    handlMouseLeave(index) {
      this.current = -1
    }
  }
}
</script>

<style lang="stylus" scoped>
.el-row
  border 1px solid red
  .el-card
    cursor pointer
    >>>
      .el-image
        width 100%
        min-height 202px
        text-align center
        color $color-PlaceholderText
        .image-slot
          i
            font-size 100px
      .text-desc
        font-size 18px
        font-weight 500
        text-align center
        min-height 60px
        line-height 60px
    .active
      color #ffffff
      background-color $color-Brand
</style>
