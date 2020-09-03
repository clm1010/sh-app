<template>
  <div class="container">
    <div>
      <logo />
    </div>
  </div>
</template>

<script>
import Logo from '@/components/Logo.vue'
export default {
  components: {
    Logo
  }
}
</script>

<style lang="stylus" scoped>
.container
  margin 0 auto
  min-height 100vh
  display flex
  justify-content center
  align-items center
  text-align center
</style>
