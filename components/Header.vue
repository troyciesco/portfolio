<script lang="ts" setup>
  const route = useRoute()
</script>
<template>
  <header class="p-8 grid grid-cols-5 justify-between items-center">
    <NuxtLink
      to="/"
      class="font-logo col-span-1 text-3xl font-bold tracking-wide"
      ><span>{</span><span class="text-secondary-600">tmc</span><span>}</span></NuxtLink
    >
    <nav class="flex justify-center col-span-3">
      <ul class="flex gap-8 items-center font-mono">
        <!-- <li><a href="/">Now</a></li>
        <li><a href="/">Work</a></li>
        <li><a href="/">Book Reviews</a></li>
        <li><a href="/">Mission</a></li>
        <li><a href="/">Resources</a></li>
        <li><a href="/">Uses</a></li>
        <li><a href="/">Code Snippets</a></li>
        <li><a href="/store">Store</a></li>
        <li><a href="/">Speaking</a></li> -->
        <li>
          <NuxtLink
            to="/"
            :class="{ 'underline decoration-secondary-500 font-bold': route.path === '/' }"
            >Home</NuxtLink
          >
        </li>
        <li>
          <NuxtLink
            to="/blog"
            :class="{ 'underline decoration-secondary-500 font-bold': route.path.includes('/blog') }"
            >Blog</NuxtLink
          >
        </li>
        <li>
          <NuxtLink
            to="/about"
            :class="{ 'underline decoration-secondary-500 font-bold': route.path === '/about' }"
            >About</NuxtLink
          >
        </li>
      </ul>
    </nav>
    <div class="flex justify-end col-span-1">
      <a
        class="font-bold underline decoration-secondary-500 decoration-wavy decoration-2"
        href="https://tmciesco-content.s3.amazonaws.com/img/troy-ciesco-resume.pdf"
        >Download Resume</a
      >
    </div>
  </header>
</template>
