<template>
  <div class="single-blog-post">
      <section class="post">
          <h1>{{title}}</h1>
          <div class="post-details">
              <div>Written By : {{author}}</div>
          </div>
          <p>{{contentPreview}}</p>
      </section>
      <section class="post-feedback">
          Please provide your comments below..
      </section>
  </div>
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
    author:{
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}
.post {
  padding-top: 20px;
  width: 100%;
}
@media (min-width: 768px) {
  .post {
    width: 600px;
    margin: auto;
  }
}
.post-title {
  margin: 0;
}
.post-details {
  padding: 10px;
  box-sizing: border-box;
  border-bottom: 3px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
@media (min-width: 768px) {
  .post-details {
    flex-direction: row;
  }
}
.post-detail {
  color: rgb(88, 88, 88);
  margin: 0 10px;
}
.post-feedback{
  padding: 20px;
}
.post-feedback a {
  color: red;
  text-decoration: none;
}
.post-feedback a:hover,
.post-feedback a:active {
  color: salmon;
}
</style>
