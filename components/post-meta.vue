<template>
  <span class="italic text-xs my-2">
    {{ new Date(date).toDateString() }} in
    <nuxt-link class="px-2" v-for="tag in tags" :key="tag" :to="`/tag/${tag}`">
    {{tag}}</nuxt-link>
  </span>
</template>

<script>
export default {
    props:{
        date: "",
        tags: null
    }
};
</script>

<style>
</style>