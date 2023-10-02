<template>
  <div class="pageContact w-full md:w-fit">
    <a :href="`mailto:${pagePrivacyLink}`" target="_blank" class="font-bold text-lg underline underline-offset-2">{{ pagePrivacyText }}</a>
  </div>
</template>

<script setup>
defineProps({
  pagePrivacyText: {
    type: String,
    required: true
  },
  pagePrivacyLink: {
    type: String,
    required: true
  },
})
</script>

<style lang="scss">
</style>