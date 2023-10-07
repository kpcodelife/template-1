<template>
  <section class="w-100 h-full flex items-center justify-center flex-col" :class="`background-${backgroundColor}`">
    <div class="w-3/4 md:w-[320px] box-shadow-lg mb-4">
      <img class="w-100 object-cover" :src="`/images/${imageSrc}`"/>
    </div>
    <div class="px-6 sm:w-[420px] lg:w-[800px] md:text-center">
      <h2 class="text-center mb-4 font-bold text-xl" :class="`color-${fontColor}`">{{ heading }}</h2>
      <p class="font-bold mb-4 text-base" :class="`color-${fontColor}`">{{ description }}</p>
      <p class="font-bold text-base" :class="`color-${fontColor}`">
        See this
        <a class="text-white cursor-pointer" :href="linkUrl" :class="`color-${linkColor}`">at this link</a>
      </p>
    </div>
  </section>
</template>

<script setup>
defineProps({
  imageSrc: {
    type: String,
    required: true
  },
  heading: {
    type: String
  },
  description: {
    type: String
  },
  linkUrl: {
    type: String
  },
  backgroundColor: {
    type: String
  },
  fontColor: {
    type: String
  },
  linkColor: {
    type: String
  }
})
</script>