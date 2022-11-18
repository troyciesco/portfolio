<script setup>
  defineProps(["content", "number"])
</script>
<template>
  <span :id="`#superscript-${number}`">{{ content }}</span>
  <sup>
    <a
      :href="`#footnote-${number}`"
      class="font-bold no-underline text-primary-700">
      {{ number }}
    </a>
  </sup>
</template>
