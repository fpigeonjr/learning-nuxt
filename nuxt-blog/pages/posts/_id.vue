<template>
  <div class="single-post update-form">
    <section class="post">
      <h1>{{ loadedPost.title }}</h1>
      <div class="post-details">
        <div>Last updated on {{ loadedPost.updatedDate }}</div>
        <div>written by {{ loadedPost.author }}</div>
      </div>
      <p>{{ loadedPost.content }}</p>
    </section>
    <section class="post-feedback">
      <p>
        Let me know what you think about the post, please send an email
        <a href="mailto:frank.pigeonjr@gmail.com">frank.pigeonjr@gmail.com</a>
      </p>
    </section>
  </div>
</template>

<script>
import axios from "axios";
export default {
  asyncData(context) {
    return axios
      .get(
        "https://nuxt-blog-eda00-default-rtdb.firebaseio.com/posts/" +
          context.params.id +
          ".json"
      )
      .then((res) => {
        return {
          loadedPost: res.data,
        };
      })
      .catch((e) => context.error(e));
  },
};
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
