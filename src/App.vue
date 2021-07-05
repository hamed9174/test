<template>
  <div id="app">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <NavBar :sideBar.sync="sideBar" />
        </div>
        <div v-show="sideBar" class="col-2 side-bar">
          <sideBar />
        </div>
        <div :class="['main' , {'col-10' : sideBar} , {'col-12' : !sideBar}]">
          <router-view/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import sideBar from "./components/sideBar";
export default {
  components:{
    NavBar,
    sideBar
  },
  data () {
    return {
      sideBar: false
    }
  }
}
</script>

<style>

</style>
