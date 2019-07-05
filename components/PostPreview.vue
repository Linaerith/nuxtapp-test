<template>
    <nuxt-link :to="'/blog/'+id">
      <article class="post-preview">
        <div
        class="post-thumbnail"
        :style="{backgroundImage: 'url('+thumbnail+')'}">
        </div>
        <div class="post-content">
          <h1>{{title}}</h1>
          <p>{{contentPreview}}</p>
        </div>
      </article>
    </nuxt-link>
</template>

<script>
export default{
  props:{
    id:{
      type: String,
      required: true
    },
    title:{
      type: String,
      required: true
    },
    contentPreview:{
      type: String,
      required: true
    },
    thumbnail:{
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>

.post-preview {
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
  width: 90%;
  height:100%;
}
a {
  text-decoration: none;
  color: black;
}
@media (min-width: 850px) {
  .post-preview {
    width: 400px;
    margin: 10px;
  }
}
.post-thumbnail {
  width: 100%;
  height: 200px;
  background-position: center;
  background-size: cover;
/*  background-image: url('../assets/post-preview.png');*/
}
.post-content {
  padding: 10px;
  text-align: center;
  max-width: 100%;
}
a:hover .post-content,
a:active .post-content {
  background-color: #DB7093;
}
</style>
