<template>
  <div class="mx-w-lg">
    <div class="flex mb-8">
      <input
        v-model="searchQuery"
        type="search"
        autocomplete="off"
        ref="search"
        class="text-4xl text-purple-600 bg-transparent focus:outline-none p-4 cursor-text w-full"
        placeholder="Search topics, posts, or tags"
      />
    </div>
    <h4 v-if="posts.length > 0">Search Results:</h4>
    <post-card v-for="post in posts" :key="post.slug" :post="post"></post-card>
  </div>
</template>

<script>
export default {
  head: {
    title: "Search",
  },
  data() {
    return {
      searchQuery: "",
      posts: [],
    };
  },
  watch: {
    async searchQuery(searchQuery) {
      if (!searchQuery) {
        this.posts = [];
        return;
      }
      this.posts = await this.$content("posts")
        .limit(6)
        .search(searchQuery)
        .fetch();
    },
  },
  mounted() {
    this.$refs.search.focus();
  },
};
</script>

<style>
</style>