<script setup lang="ts">
  const { params } = useRoute()

  const { data } = await useAsyncData("blog", () => queryContent("/blog").where({ slug: params.slug }).findOne())
</script>

<template>
  <div>
    <h1 class="mb-8 leading-tight text-[4rem] font-bold text-center">{{ data?.title }}</h1>
    <main class="max-w-prose mx-auto">
      <ContentRenderer
        v-if="data"
        :value="data">
        <template #empty>
          <p>No content found.</p>
        </template>
      </ContentRenderer>
    </main>
  </div>
</template>
