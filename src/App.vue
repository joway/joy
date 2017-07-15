<template>
  <div id="app">
    <side-bar>
      <router-view></router-view>
    </side-bar>
  </div>
</template>

<script>
import SideBar from './components/sidebar/SideBar'

export default {
  name: 'app',
  components: {
    'side-bar': SideBar,
  },
}
</script>

<style>

</style>
