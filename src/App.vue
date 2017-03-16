<template>
  <div id="app">
    <top-nav></top-nav>
    <index-nav></index-nav>
    <!--<puke></puke>-->
  </div>
</template>

<script>
import IndexNav from './components/HomeNav.vue'
import TopNav from './components/header.vue'
import puke from './components/puke'
export default {
  name: 'app',
  components: {
    IndexNav,
    TopNav,
    puke
  }

}
</script>

<style>
@import './style/reset.css';

body{
  background-image:url(./assets/bg.png);
  background-repeat:no-repeat;
  background-size:100% 100%;
  background-attachment: fixed;
  background-size: cover;
}

</style>
