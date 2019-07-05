<template>
  <div class="header-container">
    <header class="the-header">
      <TheSideNavToggle @toggle="$emit('sidenavToggle')" />
      <div class="header">
          <div>
            <img class="icon" src="https://66.media.tumblr.com/30f8463f2dff7186ca3a85c30f60d0b9/tumblr_pa7tewd3LF1xqbpm5o1_r1_500.gif" alt="logo" height="100">
          </div>
          <nuxt-link to="/"> <h1 class="title"><span>RILAKKUMA リラックマ </span></h1>
          </nuxt-link>

        <div class="spacer"></div>
        <div class="navigation-items" style="float:right">
          <ul class="nav-list">
            <li class="nav-item"><nuxt-link to="/blog">Blog</nuxt-link></li>
            <li class="nav-item"><nuxt-link to="/about">About</nuxt-link></li>
            <li class="nav-item"><nuxt-link to="/admin">Admin</nuxt-link></li>
          </ul>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
import TheSideNavToggle from "~/components/SideNavToggle";
export default {
  name: "TheHeader",
  components: {
    TheSideNavToggle
  }
};
</script>


<style scoped>
.the-header{
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
}
.header{
  background-color: #FAEBD7; /*antiquewhite*/
  width: 100%;
  height: 120px;
  border-bottom:5px solid #DC143C;
  display: block;

}

.header:hover{
  background-color: #FFFFFF;
  background-image: url('../assets/yes.png');
  background-position: 25% 25%;
  background-size: 180px;
  background-repeat: repeat-x;
}

.icon{
  margin: auto;
  margin-top: 10px;
  display: inline-block;
  position: absolute;
}

.title{
  color: #000000;
  margin: auto;
  margin-left: 170px;
  position: absolute;
  display: inline-flex;
  margin-top: 25px;
  font-weight: 300;

}

span{
  background-color: #FAEBD7;
  opacity: 0.8;
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 50px;
  display:  table-header-group;
}

.spacer {
  flex: 1;
}
.navigation-items {
  display: none;
}
@media (min-width: 768px) {
  .navigation-items {
    display: inline-flex;

  }
}
.nav-list {
  display: block;
  list-style: none;
  margin: 45px 0px 0px 0px;
}
.nav-item {
  display:inline;
  margin-right: 20px;
  font-size: 30px;
  background-color: #FAEBD7;
  opacity: 0.8;
}
.nav-item a {
  text-decoration: none;
  color: #000000;

}
.nav-item a:hover,
.nav-item a:active,
.nav-item a.nuxt-link-active {
  color: #DC143C;
}

</style>
