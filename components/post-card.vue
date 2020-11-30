<template>
  <div class="p-6 border-b-2 border-dotted border-purple-200">
    <post-heading :link="post.slug" :title="post.title"></post-heading>
    <post-meta :date="post.createdAt" :tags="post.tags"></post-meta>
    <post-description :description="post.description" :link="post.slug"></post-description>
  </div>
</template>

<script>
export default {
  props: {
    post: {},
  },
};
</script>

<style>
</style>