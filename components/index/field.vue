<template>
  <el-row type="flex" justify="center" :gutter="16">
    <el-col>
      <el-card shadow="hover" :body-style="{ padding: '0px' }">
        <el-image src="/img/field-01.jpg">
          <div
            slot="error"
            class="image-slot"
            @mouseover.native="handlMouseOver"
            @mouseleave.native="handlMouseLeave"
          >
            <i class="el-icon-picture-outline"></i>
          </div>
        </el-image>
        <div :style="active" class="text-desc">
          仓储物流
        </div>
      </el-card>
    </el-col>
    <el-col>
      <el-card
        shadow="hover"
        :body-style="{ padding: '0px' }"
        @mouseover.native.prevent="handlMouseOver"
        @mouseleave.native.prevent="handlMouseLeave"
      >
        <el-image src="/img/field-02.jpg">
          <div slot="error" class="image-slot">
            <i class="el-icon-picture-outline"></i>
          </div>
        </el-image>
        <div class="text-desc">
          11111
        </div>
      </el-card>
    </el-col>
    <el-col>
      <el-card shadow="hover" :body-style="{ padding: '0px' }">
        <el-image src="/img/field-03.jpg">
          <div slot="error" class="image-slot">
            <i class="el-icon-picture-outline"></i>
          </div>
        </el-image>
        <div class="text-desc">
          11111
        </div>
      </el-card>
    </el-col>
    <el-col>
      <el-card shadow="hover" :body-style="{ padding: '0px' }">
        <el-image src="/img/field-04.jpg">
          <div slot="error" class="image-slot">
            <i class="el-icon-picture-outline"></i>
          </div>
        </el-image>
        <div class="text-desc">
          11111
        </div>
      </el-card>
    </el-col>
    <el-col>
      <el-card shadow="hover" :body-style="{ padding: '0px' }">
        <el-image src="/img/-05.jpg">
          <div slot="error" class="image-slot">
            <i class="el-icon-picture-outline"></i>
          </div>
        </el-image>
        <div class="text-desc">
          11111
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
      active: ''
    }
  },
  methods: {
    handlMouseOver() {
      this.active = 'background-color:#409EFF;'
    },
    handlMouseLeave() {
      this.active = ''
    }
  }
}
</script>

<style lang="stylus" scoped>
.el-row
  border 1px solid red
  .el-card
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
        font-weight 600
        text-align center
        border 1px solid red
</style>
