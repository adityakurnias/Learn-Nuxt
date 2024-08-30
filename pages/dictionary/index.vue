<template>
  <div class="w-screen h-screen flex flex-col justify-center items-center">
    <form class="shadow-nol rounded-lg overflow-hidden text-xl flex items-center justify-center p-2 gap-2">
      <input v-model="word" class="h-12 w-72 outline-none p-2 border border-gray-300 rounded-md" type="text" placeholder="Input a Word..." />
      <input class=" bg-blue-500 text-white p-2 rounded-lg cursor-pointer" type="submit" value="Search" />
    </form>
    <div class="mt-5 text-center">
      <h2 class="text-2xl font-bold"></h2>
      <p class="mt-2">{{ words }}</p>
    </div>
  </div>
</template>

<script lang="ts" setup>

  import { ref } from 'vue'
  const word = ref('')

  const uri = 'https://api.dictionaryapi.dev/api/v2/entries/en/' + word

  const { data: words } = await useLazyFetch(uri)
 
</script>

<style>
/* Add custom styling here */
</style>
