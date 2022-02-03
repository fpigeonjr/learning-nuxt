<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" @submit="handleSubmit" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "~/components/admin/AdminPostForm";
import axios from "axios";

export default {
  components: {
    AdminPostForm,
  },
  layout: "admin",
  asyncData(context) {
    return axios
      .get(
        "https://nuxt-blog-eda00-default-rtdb.firebaseio.com/posts/" +
          context.params.postId +
          ".json"
      )
      .then((res) => {
        return {
          loadedPost: {...res.data, id: context.params.postId},
        };
      })
      .catch((e) => context.error(e));
  },
  methods: {
    handleSubmit(postData) {
      this.$store.dispatch("editPost", postData).then(() => {
        this.$router.push("/admin");
      });
    },
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
