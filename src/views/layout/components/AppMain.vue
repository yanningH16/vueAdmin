<template>
  <section class="app-main">
    <transition name="fade" mode="out-in">
      <!-- <keep-alive :include="cachedViews"> -->
        <router-view></router-view>
      <!-- </keep-alive> -->
      <!-- <router-view :key="key"></router-view> -->
    </transition>
  </section>
</template>

<script>
export default {
  name: 'AppMain',
  computed: {
    // key () {
    //   return this.$route.name !== undefined ? this.$route.name + +new Date() : this.$route + +new Date()
    // }
  }
}
</script>
