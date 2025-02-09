<script setup>
const props = defineProps({
  label: {
    type: String,
  },
})
</script>

<template>
  <button
    class="bg-gradient-to-r from-green-400 to-blue-400 text-white font-bold text-[15  px] px-6 py-3 rounded-full hover:shadow-lg transition-shadow duration-300 ease-in-out"
  >
    {{ props.label }}
  </button>
</template>
