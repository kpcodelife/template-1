<template>
  <div class="pageNav w-fit">
    <ul>
      <li v-for="(item, index) in navItems" :key="item.uid" class="my-2 text-xl cursor-pointer hover:underline" @click="menuClick(index)">
        {{ item.name }}
      </li>
    </ul>
  </div>
</template>

<script setup>
const emit = defineEmits(['navigateTo'])

defineProps({
  navItems: {
    type: Array,
    default: [
      {
        uid: 'a1',
        name: 'Index 1'
      },
      {
        uid: 'a2',
        name: 'Index 2'
      },
      {
        uid: 'a3',
        name: 'Index 3'
      },
      {
        uid: 'a4',
        name: 'Index 4'
      },
      {
        uid: 'a5',
        name: 'Index 5'
      },
    ]
  },
})

const menuClick = index => {
  emit('navigateTo', index)
}
</script>

<style lang="scss">
</style>