<template>
  <div class="dashboard-container">
    <!-- <div class="dashboard-text">测试路由123</div> -->
    <!-- <div class="dashboard-text">卧槽，真牛逼</div> -->
    <div class="block">
      <!-- <span class="demonstration">显示总数</span> -->
      <el-pagination @current-change="handleCurrentChange" :current-page.sync="currentPage1" :page-size="1" layout="total, prev, pager, next" :total="2050">
      </el-pagination>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ceshi',
  data () {
    return {
      currentPage1: ''
    }
  },
  created () {
    this.currentPage1 = (new Date()).getFullYear()
  },
  methods: {
    handleSizeChange (val) {
      console.log(`每页 ${val} 条`)
    },
    handleCurrentChange (val) {
      console.log(`年份: ${val}`)
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
.block .el-pager li
  font-size 50px
  color red
</style>
