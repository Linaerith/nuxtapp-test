<template>
    <div class="single-blog-post">
      <Post
      id="1"
      title="Catkkuma"
      contentPreview="Rilakkuma wants to be a cat"
      author="Linaerith"/>

    </div>
</template>

<script>
import Post from '~/components/Post.vue';
export default{
  components:{
    Post
  }
}


</script>

<style scoped>
.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}
</style>
