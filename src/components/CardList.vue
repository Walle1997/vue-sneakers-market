<script setup>
import Card from './Card.vue'

defineProps({
  items: Array,
})
const onClickAdd = () => {
  alert('Добавлено!')
}
</script>
Привет
<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      v-for="item in items"
      :key="item.id"
      :price="item.price"
      :title="item.title"
      :imageUrl="item.imageUrl"
      :onClickAdd="onClickAdd"
    />
  </div>
</template>
