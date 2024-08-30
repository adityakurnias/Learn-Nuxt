<template>
  <div>
    <figure class=" flex flex-col items-center h-72">
        <div class=" w-full h-2/3 bg-white flex justify-center rounded-xl shadow-sm overflow-hidden">
          <img :src="product.image" :alt="product.title" class=" h-full transition-all duration-400 hover:scale-105"/>
        </div>
        <figcaption>
            <p>{{ product.title }}</p>
        </figcaption>
        <p>&dollar;{{ product.price }}</p>
        <p>&dollar;{{ product.category }}</p>
    </figure>
  </div>
</template>

<script lang="ts" setup>
    const { product } = defineProps(['product'])
</script>

<style>

</style>