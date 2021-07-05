<template>
  <div class="sidebar-menu">
    <div class="settings">
      <b-button @click="settingActive = !settingActive" variant="secondary">Settings<i :class="['fas' , {'fa-sort-down': !settingActive} , {'fa-sort-up': settingActive}]"></i></b-button>
      <ul v-show="settingActive">
        <li>
          <router-link to="">
            setting 1
          </router-link>
        </li>
        <li>
          <router-link to="">
            setting 1
          </router-link>
        </li>
        <li>
          <router-link to="">
            setting 1
          </router-link>
        </li>
      </ul>
    </div>
    <div class="trade mt-2">
      <b-button @click="tradeActive = !tradeActive" variant="secondary">Trade<i :class="['fas' , {'fa-sort-down': !tradeActive} , {'fa-sort-up': tradeActive}]"></i></b-button>
      <ul v-show="tradeActive">
        <li>
          <router-link to="">
            trade 1
          </router-link>
        </li>
        <li>
          <router-link to="">
            trade 1
          </router-link>
        </li>
        <li>
          <router-link to="">
            trade 1
          </router-link>
        </li>
      </ul>
    </div>
    <div class="settings mobile-size">
      <b-button @click="settingActive = !settingActive" variant="secondary"><i class="fas fa-cog"></i> <i :class="['fas' , {'fa-sort-down': !settingActive} , {'fa-sort-up': settingActive}]"></i></b-button>
      <ul v-show="settingActive">
        <li>
          <router-link to="">
            <i class="fas fa-cog"></i> <span>1</span>
          </router-link>
        </li>
        <li>
          <router-link to="">
            <i class="fas fa-cog"></i><span>2</span>
          </router-link>
        </li>
        <li>
          <router-link to="">
            <i class="fas fa-cog"></i><span>3</span>
          </router-link>
        </li>
      </ul>
    </div>
    <div class="trade mt-2 mobile-size">
      <b-button @click="tradeActive = !tradeActive" variant="secondary"><i class="fas fa-trademark"></i><i :class="['fas' , {'fa-sort-down': !tradeActive} , {'fa-sort-up': tradeActive}]"></i></b-button>
      <ul v-show="tradeActive">
        <li>
          <router-link to="">
            <i class="fas fa-trademark"></i><span>1</span>
          </router-link>
        </li>
        <li>
          <router-link to="">
            <i class="fas fa-trademark"></i><span>2</span>
          </router-link>
        </li>
        <li>
          <router-link to="">
            <i class="fas fa-trademark"></i><span>3</span>
          </router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "sideBar",
  data(){
    return{
      settingActive : true,
      tradeActive : false
    }
  }
}
</script>

<style scoped>

</style>