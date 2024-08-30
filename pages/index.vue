<template>
  <div class=" text-center w-screen h-screen">
    <h1 class=" text-4xl font-bold">My Nuxt Project</h1>
    <p>This Project is for testing my skill about data fetching in Nuxt.</p>
    <div class=" m-10">
      <NuxtLink to="/product/" class="btn">Fake Store</NuxtLink>
      <NuxtLink to="/dictionary/" class="btn">Dictionary</NuxtLink>
      <NuxtLink to="/product/" class="btn">Olsop Adli</NuxtLink>
    </div>
  </div>
</template>

<script setup>
    definePageMeta({
    layout: 'home'
  })
</script>
<style>
/* Your styling here */
</style>
