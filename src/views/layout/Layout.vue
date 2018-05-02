<template>
  <div class="app-wrapper" :class="{hideSidebar:!sidebar.opened}">
    <!-- 左侧导航 -->
    <sidebar class="sidebar-container"></sidebar>
    <div class="main-container">
      <!-- 头部导航 -->
      <navbar></navbar>
      <!-- 中间内容部分 -->
      <app-main></app-main>
    </div>
  </div>
</template>

<script>
import { Navbar, Sidebar, AppMain } from '@/views/layout/components'

export default {
  name: 'layout',
  components: {
    Navbar,
    Sidebar,
    AppMain
  },
  computed: {
    sidebar () {
      return this.$store.state.app.sidebar
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
// @import 'src/styles/mixin.scss'
.app-wrapper
  content ''
  display table
  clear both
  position relative
  height 100%
  width 100%
</style>
