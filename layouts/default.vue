<template>
  <div>
    <my-header></my-header>
    <nuxt />
  </div>
</template>
<script>
import MyHeader from '@/components/header/index.vue'
export default {
  name: 'Default',
  components: {
    MyHeader
  },
  data() {
    return {}
  },
  methods: {}
}
</script>
<style></style>
