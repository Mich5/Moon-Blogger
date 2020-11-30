<template>
  <article>
    <post-heading :title="post.title" :link="post.slug"></post-heading>
    <post-meta :date="post.createdAt" :tags="post.tags"></post-meta>
    <nuxt-content class="mt-6" :document="post" />
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    const param = params.post || "index";
    const post = await $content("posts", param)
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: "Page not found" });
      });
    return {
      post,
    };
  },
};
</script>