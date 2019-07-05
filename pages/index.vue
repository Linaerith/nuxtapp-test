<template>
  <div class="home-page">
    <div class="container">
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
        title="Rilakkuma at the Carot Café"
        contentPreview="A themed café with bunnies"
        thumbnail="https://wallpaperaccess.com/full/32116.gif"/>
        <PostPreview
          id="3"
          title="Mad about Pandas"
          contentPreview="Riri has a new obsession"
          thumbnail="https://wallpaperaccess.com/full/417869.jpg"/>

        </section>
    </div>
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

.container{
  margin: 50px 115px 50px 115px;
  border-radius: 10px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
}
.intro {
  height: 100px;
  position: relative;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
}
.intro h1 {
  position: absolute;
  top: 10%;
  left: 2%;
  width: 96%;
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
  max-height:400px;
  overflow:auto;
}

.featured-posts::-webkit-scrollbar
{
	width: 12px;
	background-color: white;
}
.featured-posts::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey;
  border-radius: 10px;
}
.featured-posts::-webkit-scrollbar-thumb {
  border-radius: 10px;
  -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
  background-color: #DB7093;
}
</style>
