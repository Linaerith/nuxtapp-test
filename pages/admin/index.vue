<template>
  <div class="admin-page">
    <h1>Admin Page</h1>
    <div class="new-post">
      <button @click="$router.push('admin/newPost')">
        Create a post
      </button>
    </div>
    <div class="existing-post">
      <h3>Existing posts</h3>
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
.admin-page {
  padding: 20px;
}
.new-post {
  text-align: center;
  border-bottom: 2px solid #ccc;
  padding-bottom: 20px;
}
.existing-posts h1 {
  text-align: center;
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

h3{
  align-items: center;
  justify-content: center;
  text-align: center;
  padding:5px;
}

</style>
