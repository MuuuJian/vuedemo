<template>
  <div>
    <el-menu
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b"
      style="height: calc(100vh - 61px)"
    >
      <el-menu-item index="1" @click="jumpTo('test1')" id="item1">test1:mock</el-menu-item>
      <el-menu-item index="2" @click="jumpTo('test2')" id="item2">选项2</el-menu-item>
      <el-menu-item index="3" @click="jumpTo('test3')" id="item3">test3:$props</el-menu-item>
      <el-menu-item index="4" @click="jumpTo('test4')" id="item4">test4:保存res</el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: "navigator",
  components: {},
  data() {
    return {};
  },
  mounted() {},
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
    jumpTo: function(params) {
      this.$router.push(params);
    }
  },
  watch: {}
};
</script>

<style scoped>
.width200 {
  width: 200px;
}
.width80 {
  width: 80px;
}
</style>
