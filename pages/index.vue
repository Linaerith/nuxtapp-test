<template>
  <div class="home-page">
    <section class="intro">
      <h1>Latest News</h1>
    </section>
    <section class="featured-posts">
      <PostPreview
      id="1"
      title="Catkkuma"
      contentPreview="Rilakkuma wants to be a cat"
      thumbnail="https://wallpaperaccess.com/full/53392.png"/>
      <PostPreview
        id="2"
        title="Rilakkuma and Bunny"
        contentPreview="A themed café with bunnies"
        thumbnail="https://wallpaperaccess.com/full/32116.gif"/>
        <PostPreview
          id="3"
          title="Mad about Pandas"
          contentPreview="Riri has a new obsession"
          thumbnail="https://wallpaperaccess.com/full/417869.jpg"/>
    </section>


  </div>
</template>

<script>
import PostPreview from '~/components/PostPreview.vue';
export default{
  components:{
    PostPreview
  }
}


</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
}
.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: #DB7093;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}
@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}
.featured-posts {
  display: flex;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
