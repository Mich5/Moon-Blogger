<template>
  <div class="m-1">
      <h1>Tag : {{tag}}</h1>
    <post-card v-for="post in posts" :key="post.slug" :post="post"></post-card>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const posts = await $content('posts').where({ tags: { $contains: [params.tag] }}).fetch();
    console.log(posts);
    return { posts, tag:params.tag };
  },
};
</script>

<style>
</style>
