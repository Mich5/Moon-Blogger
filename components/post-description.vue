<template>
      <p class="mt-4">
      {{ description }}<nuxt-link class="mx-2" :to="`/posts/${link}`">Read More</nuxt-link>
    </p>
</template>

<script>
export default {
    props: {
        description: "",
        link: ""
    }
}
</script>

<style>

</style>