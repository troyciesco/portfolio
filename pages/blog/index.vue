<script setup lang="ts">
  const { data: posts } = await useAsyncData("blog", () => queryContent("/blog").find())
</script>

<template>
  <div>
    <h1>This is the blog page</h1>
    <li
      v-for="post of posts"
      :key="post.slug">
      <NuxtLink :to="`blog/${post.slug}`">{{ post.title }}</NuxtLink>
    </li>
  </div>
</template>
