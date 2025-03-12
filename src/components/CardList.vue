<script setup>
import Card from './Card.vue'
import { inject } from 'vue'

defineProps({
  items: Array,
})
const onClickAdd = () => {
  alert('Добавлено!')
}

const addToFavorite = inject('addToFavorite')
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      v-for="item in items"
      :key="item.id"
      :id="item.id"
      :price="item.price"
      :title="item.title"
      :imageUrl="item.imageUrl"
      :onClickAdd="onClickAdd"
      :onClickFavorite="() => addToFavorite(item)"
      :isFavorite="item.isFavorite"
    />
  </div>
</template>
