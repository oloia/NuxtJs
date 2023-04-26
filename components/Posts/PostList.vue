<template>
  <section class="posts-list">
    <PostPreview
      id="1"
      title="Hello there"
      thumbnail="https://www.netscribes.com/wp-content/uploads/2019/06/Technology-Watch.jpg"
      previewText="This is my first post!"
    />
  </section>
</template>
<script>

import PostPreview  from "~/components/Posts/PostPreview";

export default {
components:{
PostPreview
}
}
</script>

<style scoped>

.posts-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
