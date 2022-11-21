<script setup lang="ts">
  const { path } = useRoute()

  const { data } = await useAsyncData(`content-${path}`, () => queryContent().where({ _path: path }).findOne())
</script>

<template>
  <div class="px-8 pt-10">
    <div class="mb-8">
      <h1 class="leading-tight text-3xl mb-2 md:text-[4rem] font-bold text-center px-4">{{ data?.title }}</h1>
      <p class="text-center">
        {{ new Date(data?.date).toLocaleDateString("en", { year: "numeric", month: "long", day: "numeric" }) }}
      </p>
    </div>
    <main class="mx-auto prose max-w-prose">
      <ContentDoc />
      <!-- <ContentRenderer
        v-if="data"
        :value="data">
        <template #empty>
          <p>No content found.</p>
        </template>
      </ContentRenderer> -->
    </main>
  </div>
</template>

<style scoped lang="scss">
  main {
    p {
      font-size: 1.125rem;
      margin-bottom: 2rem;
      color: #0051a8 !important;
      & strong {
        color: #0051a8 !important;
      }
    }

    ul {
      color: #0051a8 !important;
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
