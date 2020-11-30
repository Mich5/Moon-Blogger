<template>
  <div class="m-1">
    <post-card v-for="post in posts" :key="post.slug" :post="post"></post-card>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const posts = await $content("posts", params.slug).fetch();
    console.log(posts);
    return { posts };
  },
};
</script>

<style>
</style>
