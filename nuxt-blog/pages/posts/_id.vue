<template>
  <div class="single-post update-form">
    <section class="post">
      <h1>Title of Post</h1>
      <div class="post-details">
        <div>Last updated on XXX</div>
        <div>written by NAME</div>
      </div>
      <p>Content of post.</p>
    </section>
    <section class="post-feedback">
      <p>
        Let me know whast you think about the post, please send an email
        <a href="mailto:frank.pigeonjr@gmail.com">frank.pigeonjr@gmail.com</a>
      </p>
    </section>
  </div>
</template>

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
