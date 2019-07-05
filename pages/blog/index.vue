<template>
  <div class="all-posts">
    <div class="title">
      <h1>List of Riri's stories</h1>
    </div>
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
</template>

<script>
import PostPreview from "~/components/PostPreview"
export default{
  components: {
    PostPreview
  }
}
</script>

<style scoped>
.all-posts{
  display:block;
  align-content: center;
  justify-content: center;
  margin-top: 20px;
}
.title{
  display: flex;
  align-content: center;
  justify-content: center;
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
