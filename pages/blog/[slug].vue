<script setup lang="ts">
  const { params } = useRoute()

  const { data } = await useAsyncData("blog", () => queryContent("/blog").where({ slug: params.slug }).findOne())
</script>

<template>
  <div>
    <h1>This is the post page</h1>
    <ContentRenderer
      v-if="data"
      :value="data">
      <template #empty>
        <p>No content found.</p>
      </template>
    </ContentRenderer>
  </div>
</template>
