<template>
  <div class="pageContact w-full md:w-fit">
    <a :href="`mailto:${pageContact}`" class="font-bold text-lg">{{ pageContact }}</a>
  </div>
</template>

<script setup>
defineProps({
  pageContact: {
    type: String,
    required: true
  }
})
</script>

<style lang="scss">
</style>