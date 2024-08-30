<template>
  <div>
    
  </div>
</template>

<script setup>
  const { word } = useRoute().params
  const uri = 'https://api.dictionaryapi.dev/api/v2/entries/en/' + word

  const { data: words } = await useFetch(uri)

</script>

<style>

</style>