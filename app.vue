<script lang="ts" setup>
  const app = useAppConfig()
  useHead({
    title: app.title,
    script: [{ src: "https://identity.netlify.com/v1/netlify-identity-widget.js" }],
  })
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
