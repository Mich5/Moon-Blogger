<template>
  <div class="min-h-screen flex flex-col">
    <header class="flex justify-between px-12 py-4">
      <nuxt-link to="/" class="ml-1 flex space-x-4 no-underline">
        <Logo />
        <h4>Moon Blogger</h4>
      </nuxt-link>
      <nav>
        <nuxt-link to="/search">
          <search-icon></search-icon>
        </nuxt-link>
      </nav>
    </header>
    <div class=" flex-auto max-w-4xl mx-auto px-6 my-12 md:grid md:grid-cols-3 gap-16">
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

    <footer class="w-full p-6 text-center text-xs">
      <div class="mx-auto">
        Made with
        <a href="https://nuxtjs.org/" target="_blank" rel="noopener">
          Nuxt.js 
        </a>,
        <a href="https://tailwindcss.com/" target="_blank" rel="noopener">
          TailwindCSS
        </a>
        and ❤️ by 
        <a href="https://micho.me/" target="_blank" rel="noopener">
          Micho Ngoma
        </a> <span class="mx-2 text-purple-900">•</span>
        <a href="https://github.com/Mich5/Moon-Blogger" target="_blank" rel="noopener">
          Source on github
        </a>

      </div>
    </footer>
  </div>
</template>

<style>
</style>
