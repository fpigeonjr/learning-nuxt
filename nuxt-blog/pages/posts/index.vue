<template>
  <PostList :posts="loadedPosts" />
</template>

<script>
import PostList from "~/components/posts/PostList";

export default {
  components: {
    PostList,
  },
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          loadedPosts: [
            {
              id: "1",
              title: "First Post",
              previewText: "Hello World.",
              thumbnail:
                "https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2840&q=80",
            },
            {
              id: "2",
              title: "Second Post",
              previewText: "This is our second post. ",
              thumbnail:
                "https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2840&q=80",
            },
          ],
        });
      }, 1500);
    })
      .then((data) => {
        return data;
      })
      .catch((e) => {
        context.error(new Error());
      });
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
