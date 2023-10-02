<template>
  <h1 class="font-bold text-xl uppercase">{{ pageHeading }}</h1>
</template>

<script setup>
defineProps({
  pageHeading: {
    type: String,
    required: true
  }
})
</script>