<template>
  <div class="m-1">
    <h1>Tag : {{ tag }}</h1>
    <post-card v-for="post in posts" :key="post.slug" :post="post"></post-card>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: `Articles about ${this.tag}`,
    };
  },
  async asyncData({ $content, params }) {
    const posts = await $content("posts")
      .where({ tags: { $contains: [params.tag] } })
      .fetch();
    return { posts, tag: params.tag };
  },
};
</script>

<style>
</style>
