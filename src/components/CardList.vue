<script setup>
import Card from './Card.vue'

const onClickAdd = () => {
    alert('Добавлено!');
}
</script>

<template>
    <div class="grid grid-cols-4 gap-5 ">
     <Card
     :price="12999"
     title="Мужские кроссовки Nike Blazer Mid Suede"
     image-url="/sneakers/sneakers-1.jpg"
     :is-favorite="false"
     :onClickAdd="onClickAdd"
     :is-added="true"
     
     
     />

   </div>
</template>