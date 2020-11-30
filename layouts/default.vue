<template>
  <div>
    <header class="flex justify-between px-12 py-4">
      <nuxt-link to="/" class="ml-1 flex space-x-4 no-underline">
        <Logo />
        <h4>Moon Blogger</h4>
      </nuxt-link>
      <nav>
        <nuxt-link to="/search">
          <search-icon @click=""></search-icon>
        </nuxt-link>
      </nav>
    </header>
    <div class=" max-w-4xl mx-auto my-12 grid grid-cols-3 gap-16">
      <div class="col-span-2">
        <Nuxt />
      </div>
      <div class="col-span-1">
        <div class="border-purple-400 border-dashed border-2 w-full p-4">
          <h2>Moon Blogger</h2>
          <p>Hi, I'm a full-stack developer who likes to blog about tech.</p>
          <p>Get in touch with me @ the following links.</p>
          <social-links></social-links>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
</style>
