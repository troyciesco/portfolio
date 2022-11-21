<script lang="ts" setup>
  const route = useRoute()
</script>
<template>
  <header class="grid items-center justify-between grid-cols-3 p-4 md:p-8 md:grid-cols-4">
    <NuxtLink
      to="/"
      class="col-span-1 text-3xl font-bold tracking-wide font-logo"
      ><span>{</span><span class="text-secondary-600">tmc</span><span>}</span></NuxtLink
    >
    <nav class="flex col-span-1 md:justify-center md:col-span-2">
      <ul class="flex items-center gap-8 font-mono">
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
