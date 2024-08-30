<template>
  <div>
    
  </div>
</template>

<script setup>
  const { id } = useRoute().params
  const uri = 'https://fakestoreapi.com/products/' + id

  const { data: product } = await useFetch(uri)

</script>

<style>

</style>