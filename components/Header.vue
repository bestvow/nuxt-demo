<template>
  <div class="header flex">
    <el-breadcrumb separator="/">
      <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
      <el-breadcrumb-item>
        <a href="/">活动管理</a>
      </el-breadcrumb-item>
      <el-breadcrumb-item>活动列表</el-breadcrumb-item>
      <el-breadcrumb-item>活动详情</el-breadcrumb-item>
    </el-breadcrumb>
    <div class="quick-link">
      <el-link :underline="false" type="primary">处理中心</el-link>
      <el-link :underline="false" type="success">我得工作台</el-link>
      <el-link :underline="false" type="warning">消息中心</el-link>
      <el-link :underline="false" type="danger">订单中心</el-link>
      <el-link :underline="false" disabled icon="el-icon-user">管理员</el-link>
      <el-link :underline="false">退出登录</el-link>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  }
};
</script>
<style scoped>
.header {
  padding: 0 20px;
  height: 60px;
  border-bottom: 1px solid #ccc;
  background: #fefefe;
  justify-content: space-between;
  align-items: center;
}
.quick-link .el-link + .el-link {
  padding: 0 10px;
}
</style>