<script lang="ts" setup>
  import "@fontsource/ibm-plex-mono/400.css"
  import "@fontsource/ibm-plex-mono/700.css"
  import "@fontsource/ibm-plex-sans/400.css"
  import "@fontsource/ibm-plex-sans/700.css"
  import "@fontsource/ibm-plex-serif/400.css"
  import "@fontsource/ibm-plex-serif/700.css"

  const app = useAppConfig()
  useHead({
    title: app.title,
    script: [{ src: "https://identity.netlify.com/v1/netlify-identity-widget.js" }],
  })
</script>

<template>
  <div>
    <NuxtLayout>
      <Header />
      <NuxtPage />
      <Footer />
    </NuxtLayout>
  </div>
</template>
