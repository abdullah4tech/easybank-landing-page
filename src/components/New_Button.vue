<script setup>

const props = defineProps({
  label: {
    type: String
  }
})

</script>


<template>
  <button class="py-3 px-8 rounded-full bg-linear-to-r/shorter from-lime-200 to-blue-300 font-bold text-white">{{ props.label }}</button>
</template>
