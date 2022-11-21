<script setup lang="ts">
  const { data: posts, pending } = await useAsyncData("blog", () => queryContent("/blog").find())
</script>

<template>
  <main class="flex flex-col items-center justify-center mx-auto max-w-7xl">
    <h1 class="mb-8 leading-tight text-[4rem] font-bold">Blog</h1>

    <section class="min-h-screen">
      <ul v-if="!pending && posts && posts.length > 0">
        <li
          v-for="post of posts"
          :key="post._path">
          <NuxtLink :to="post._path">{{ post.title }}</NuxtLink>
        </li>
      </ul>
      <div v-else>loading....</div>
    </section>
  </main>
</template>
