<template>
  <el-container style="border: 1px solid #eee">
    <Menu />
    <el-container class="is-vertical">
      <Header />
      <el-main>
        <nuxt />
      </el-main>
    </el-container>
  </el-container>
</template>
<script>
import Header from "~/components/Header.vue";
import Menu from "~/components/Menu.vue";
export default {
  components: {
    Header,
    Menu
  }
};
</script>
<style  >
.flex {
  display: flex;
}
.mauto {
  margin: 0 auto;
}
.text-center {
  text-align: center;
}
</style>