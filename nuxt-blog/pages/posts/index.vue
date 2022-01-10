<template>
  <PostList :posts="loadedPosts" />
</template>

<script>
import PostList from "~/components/posts/PostList";

export default {
  components: {
    PostList,
  },

  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts;
    },
  },
  name: "PostsPage",
};
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-content: center;
}
</style>
