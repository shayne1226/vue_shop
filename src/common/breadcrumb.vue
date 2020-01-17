<template>
  <div>
    <el-breadcrumb separator-class="el-icon-arrow-right">
      <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
      <el-breadcrumb-item>{{aa}}</el-breadcrumb-item>
      <el-breadcrumb-item>{{bb}}</el-breadcrumb-item>
    </el-breadcrumb>
  </div>
</template>
<script>
export default {
  props: ['aa', 'bb']
}
</script>
<style lang="less">
</style>
