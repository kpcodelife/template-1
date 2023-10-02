<template>
  <div class="pageDescription w-full md:w-[320px]">
    <p class="font-bold text-lg">{{ pageDescription }}</p>
  </div>
</template>

<script setup>
defineProps({
  pageDescription: {
    type: String,
    required: true
  }
})
</script>

<style lang="scss">
</style>