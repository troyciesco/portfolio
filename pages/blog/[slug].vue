<script setup lang="ts">
  const { params } = useRoute()

  const { data } = await useAsyncData("blog", () => queryContent("/blog").where({ slug: params.slug }).findOne())
</script>

<template>
  <div class="pt-10 px-8">
    <div class="mb-8">
      <h1 class="leading-tight text-3xl mb-2 md:text-[4rem] font-bold text-center px-4">{{ data?.title }}</h1>
      <p class="text-center">
        {{ new Date(data?.date).toLocaleDateString("en", { year: "numeric", month: "long", day: "numeric" }) }}
      </p>
    </div>
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

<style lang="scss">
  main {
    p {
      font-size: 1.125rem;
      margin-bottom: 2rem;
    }

    ul {
      font-size: 1.125rem;
      margin-bottom: 2rem;
      margin-left: 1rem;
      list-style: disc;
    }

    li {
      margin-bottom: 0.5rem;
    }
  }
</style>
