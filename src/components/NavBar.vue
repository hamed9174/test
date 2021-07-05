<template>
  <div class="row header">
    <div class="col-2 bars" @click="sidebarActive">
      <i class="fas fa-bars"></i>
    </div>
    <div class="col-9 header-menu">
      <ul class="menu-list">
        <li>
          <router-link to="" class="active">
            Home
          </router-link>
        </li>
        <li>
          <router-link to="">
            About
          </router-link>
        </li>
        <li>
          <router-link to="">
            Contact us
          </router-link>
        </li>
      </ul>
    </div>
    <div class="col-1 header-logo">
      <h3>TEST</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  props:['sideBar'],
  methods:{
    sidebarActive(){
      this.sideBar = !this.sideBar
      this.$emit('update:sideBar', this.sideBar)
    }
  }
}
</script>

<style scoped>

</style>
