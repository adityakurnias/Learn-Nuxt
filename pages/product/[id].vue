<template>
  <main class=" w-screen h-screen p-8 grid grid-cols-2 ">
    <img :src="product.image" :alt="product.title" class=" h-full">
    <div>
      <div class="p-4">
        <h1 class=" font-bold text-4xl border-b-2 pb-6">{{ product.title }}</h1>
        <p class=" text-lg p-1 border-b-2 pb-3">{{ product.description }}</p>
        <p class=" font-semibold pt-3">&dollar;{{ product.price }}</p>
      </div>
      <button class=" btn" v-on:click="Back">&leftarrow;Back</button>
    </div>
  </main>
</template>

<script lang="js" setup>
  const { id } = useRoute().params
  const uri = 'https://fakestoreapi.com/products/' + id

  const { data: product } = await useFetch(uri)

  function Back() {
    window.history.back()
  }

</script>

<style>

</style>