<template>
  <div class="admin-new-post-page">
    <section class="new-post-form">
      <form @submit.prevent="onSave">
        <AppInputControl v-model="editedPost.author">Author Name</AppInputControl>
        <AppInputControl v-model="editedPost.title">Title</AppInputControl>
        <AppInputControl v-model="editedPost.thumbnailLink">Thumbnail Link</AppInputControl>
        <AppInputControl control-type="textarea" v-model="editedPost.content">Content</AppInputControl>
        <AppButton type="submit">Save</AppButton>
        <AppButton
          type="button"
          style="margin-left: 10px"
          btn-style="cancel"
          @click="onCancel">Cancel</AppButton>
      </form>
    </section>
  </div>
</template>

<script>

import AppInputControl from "~/components/UI/AppControlInput";
import AppButton from "~/components/UI/AppButton";
export default {
  components: {AppButton, AppInputControl},
  data() {
    return {
      editedPost: {
        author: '',
        title: '',
        thumbnailLink: '',
        content: ''
      }
    }
  },
  methods: {
    onSave() {
      //Save post
      console.log(this.editedPost)
    },
    onCancel() {
      //Navigate back
      this.$router.push('/admin')
    }
  }
}
</script>
