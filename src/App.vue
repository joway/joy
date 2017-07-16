<template>
  <side-bar>
    <router-view></router-view>
  </side-bar>
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
