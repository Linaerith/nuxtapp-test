<template>
  <form class="new-post-form" v-on:submit.prevent="onSave()">
    <AppControlInput v-model="editedPost.author">Author Name</AppControlInput>

    <AppControlInput v-model="editedPost.title">Title</AppControlInput>

    <AppControlInput v-model="editedPost.thumbnailLink">Thumbnail Link</AppControlInput>

    <AppControlInput
              control-type="textarea"
              v-model="editedPost.content">Content</AppControlInput>

    <AppButton type="submit">Save</AppButton>

    <AppButton
              type="button"
              style="margin-left: 10px"
              btn-style="cancel"
              @click="onCancel">Cancel</AppButton>

  </form>
</template>

<script type="text/javascript">
import AppButton from '~/components/AppButton.vue';
import AppControlInput from '~/components/AppControlInput.vue';
  export default{
    components:{
      AppButton,
      AppControlInput
    },
    data(){
      return{
        editedPost:{
          title: '',
          author:'',
          thumbnailLink:'',
          content:''

        }
      }
    },
    methods:{
      onCancel(){
        this.$router.push("/admin");
      },
      onSave(){
        console.log(this.editedPost);
      }
    }
  }
</script>

<style media="screen">
.new-post-form{
  padding: 20px;
}
</style>
