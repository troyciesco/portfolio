<script setup lang="ts">
  const { data: posts } = await useAsyncData("blog", () => queryContent("/blog").find())
</script>

<template>
  <main class="max-w-7xl mx-auto flex flex-col items-center justify-center">
    <h1 class="mb-8 leading-tight text-[4rem] font-bold">Blog</h1>

    <section class="min-h-screen">
      <ul v-if="posts && posts.length > 0">
        <li
          v-for="post of posts"
          :key="post.slug">
          <NuxtLink :to="`blog/${post.slug}`">{{ post.title }}</NuxtLink>
        </li>
      </ul>
    </section>
  </main>
</template>
