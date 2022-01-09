<template>
  <PostList />
</template>

<script>
import PostList from "~/components/posts/PostList";

export default {
  components: {
    PostList,
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
