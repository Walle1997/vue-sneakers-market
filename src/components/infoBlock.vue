<script setup>
defineProps({
  title: String,
  description: String,
  imageUrl: String
})
</script>


<template>
  <div class="flex flex-col item-center text-center">
    <img height="70" width="70" :src="imageUrl" alt="Info image" />
    <h2 class="mt-4 text-2xl font-medium">{{ title }}</h2>
    <p class="text-gray-400 mt-1">{{ description }}</p>
  </div>

</template>
