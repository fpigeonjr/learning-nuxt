<template>
  <section class="posts">
    <PostPreview
      id="1"
      thumbnail="https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2840&q=80"
      title="Hello There"
      previewText="This is my first post."
    />
    <PostPreview
      id="2"
      thumbnail="https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2840&q=80"
      title="Hello There Again"
      previewText="This is my second post."
    />
    <PostPreview
      id="3"
      thumbnail="https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2840&q=80"
      title="Back Again: Tres Leches "
      previewText="This is my third post."
    />
  </section>
</template>

<script>
import PostPreview from "~/components/posts/PostPreview";
export default {
  components: {
    PostPreview,
  },
  name: "PostList",
};
</script>

<style scoped>
.posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
