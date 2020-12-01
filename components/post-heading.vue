<template>
  <div>
    <nuxt-link class="no-underline" :to="`/posts/${link}`">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="w-5 h-5 fill-current text-purple-700 inline align-middle"
        viewBox="0 0 20 20"
      >
        <path
          fill="#9f7aea"
          d="M14 5h-4v2h4V5zm0 3h-4v1h4V8zM9 5H6v4h3V5zm0 6h5v-1H9v1zm3 2h2v-1h-2v1zm2 1H6v1h8v-1zm-3-2H6v1h5v-1zm-3-2H6v1h2v-1zm9-9H3a1 1 0 00-1 1v16a1 1 0 001 1h14a1 1 0 001-1V2a1 1 0 00-1-1zm-1 16H4V3h12v14z"
        />
      </svg>
      <h2 class="inline align-middle">{{ title }}</h2>
    </nuxt-link>
  </div>
</template>

<script>
export default {
    props:{
        title: "",
        link:""
    }
};
</script>

<style>
</style>