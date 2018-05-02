<template>
  <div id="app">
    <!-- <el-row><nav-menu/></el-row> -->
    <el-row class="tac" style="text-align:left">
    <div style="float: left">
      <list-menu></list-menu>
    </div>
    <div style="float:left">
      <img src="./assets/logo.png">
      <div>
          <el-button @click="startHacking">Start</el-button>
      </div>
    </div>
    </el-row>
  </div>
</template>

<script scoped>
import NavMenu from "./vue/NavMenu.vue";
import ListMenu from "./vue/ListMenu.vue";

export default {
  components : {
    "nav-menu" : NavMenu,
    "list-menu" : ListMenu
  },
  methods: {
    startHacking () {
      this.$notify({
        title: 'It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    }
  }
}
</script>

<style scoped>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
