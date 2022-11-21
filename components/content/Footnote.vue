<script setup>
  defineProps(["number"])
</script>
<template>
  <div
    :id="`footnote-${number}`"
    class="flex gap-2">
    <span class="mt-[1em]">
      <a
        :href="`#superscript-${number}`"
        class="font-bold no-underline text-primary-700">
        <sup>{{ number }}</sup>
      </a>
    </span>
    <div class="content">
      <slot />
    </div>
  </div>
</template>

<style scoped lang="scss">
  .content {
    & p {
      font-size: 0.8rem !important;
    }
  }
</style>
