<template>
  <div>
    <Head @sidenavToggle= "display = !display"/>
    <SideNav :show="display"/>
    <nuxt/>
  </div>
</template>

<script>
import Head from '~/components/Head.vue';
import SideNav from "~/components/Sidenav.vue";
export default{
  components: {
    Head,
    SideNav
  },
  data(){
    return{
      display: false
    }
  }
}
</script>

<style>
html {
  font-family: "DM Serif Text", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background-color: #FFE4E1;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}


</style>
