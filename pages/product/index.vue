<template>
  <div class="flex flex-col min-h-screen">
    <header class="sticky top-0 z-50 w-full border-b bg-white/95 backdrop-blur supports-[backdrop-filter]:bg-white/60">
      <div class="container mx-auto flex h-16 items-center justify-between px-4">
        <div class="flex items-center space-x-4">
          <NuxtLink to="/" class="text-xl font-bold">FashionTech</NuxtLink>
          <nav class="hidden md:flex space-x-4">
            <NuxtLink to="/clothing" class="text-sm font-medium hover:text-gray-600">Clothing</NuxtLink>
            <NuxtLink to="/electronics" class="text-sm font-medium hover:text-gray-600">Electronics</NuxtLink>
          </nav>
        </div>
        <div class="flex items-center space-x-4">
          <div class="relative">
            <input
              type="search"
              placeholder="Search products..."
              class="pl-8 pr-2 py-1 rounded-md border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500"
            />
            <svg
              xmlns="h"
              class="h-5 w-5 absolute left-2 top-1.5 text-gray-400"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
          </div>
          <button class="p-2 rounded-full hover:bg-gray-100">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
            </svg>
          </button>
        </div>
      </div>
    </header>

    <main class="flex-grow">
      <section class="w-full py-12 md:py-24 lg:py-32 bg-[url('/placeholder.svg?height=400&width=800')] bg-cover bg-center">
        <div class="container mx-auto px-4 md:px-6">
          <div class="flex flex-col items-center space-y-4 text-center">
            <div class="space-y-2">
              <h1 class="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl lg:text-6xl/none text-white">
                Summer Sale
              </h1>
              <p class="mx-auto max-w-[700px] text-white md:text-xl">
                Up to 50% off on selected items. Limited time offer!
              </p>
            </div>
            <button class="bg-white text-black px-4 py-2 rounded hover:bg-gray-100">
              Shop Now
            </button>
          </div>
        </div>
      </section>

      <section class="w-full py-12 md:py-24 lg:py-32">
        <div class="container mx-auto px-4 md:px-6">
          <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl mb-8">Featured Clothing</h2>
          <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
            <div v-for="p in productsCloth"  class="group relative overflow-hidden rounded-lg">
              <img
                :src="p.image"
                :alt="p.title"
                class="object-cover h-64 mx-auto transition-transform group-hover:scale-105"
              />
              <div class="absolute inset-0 bg-black bg-opacity-40 transition-opacity opacity-0 group-hover:opacity-100 flex items-end">
                <div class="p-4 text-white">
                  <h3 class="font-semibold">{{ p.title }}</h3>
                  <p>&dollar;{{ p.price }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="w-full py-12 md:py-24 lg:py-32 bg-gray-100">
        <div class="container mx-auto px-4 md:px-6">
          <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl mb-8">Featured Electronics</h2>
          <div class="h-96 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
            <div v-for="p in productsElect" class="group h-96 relative overflow-hidden rounded-lg bg-white">
              <div class=" h-1/2">
                <img
                  :src="p.image"
                  :alt="p.title"
                  class=" p-3 transition-transform h-full mx-auto group-hover:scale-105"
                />
              </div>
              <div class="p-4">
                <h3 class="font-semibold">{{ p.title }}</h3>
                <p class="text-sm text-gray-500">Latest model</p>
                <p class="mt-2 font-bold">&dollar;{{ p.price }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer class="w-full py-6 bg-gray-800 text-white">
      <div class="container mx-auto px-4 md:px-6">
        <div class="grid gap-8 sm:grid-cols-2 md:grid-cols-4">
          <div class="space-y-3">
            <h3 class="text-lg font-medium">Shop</h3>
            <ul class="space-y-1">
              <li><NuxtLink to="/clothing" class="text-sm text-gray-300 hover:underline">Clothing</NuxtLink></li>
              <li><NuxtLink to="/electronics" class="text-sm text-gray-300 hover:underline">Electronics</NuxtLink></li>
              <li><NuxtLink to="/new-arrivals" class="text-sm text-gray-300 hover:underline">New Arrivals</NuxtLink></li>
              <li><NuxtLink to="/sale" class="text-sm text-gray-300 hover:underline">Sale</NuxtLink></li>
            </ul>
          </div>
          <div class="space-y-3">
            <h3 class="text-lg font-medium">Account</h3>
            <ul class="space-y-1">
              <li><NuxtLink to="" class="text-sm text-gray-300 hover:underline">My Account</NuxtLink></li>
              <li><NuxtLink to="" class="text-sm text-gray-300 hover:underline">Orders</NuxtLink></li>
              <li><NuxtLink to="" class="text-sm text-gray-300 hover:underline">Wishlist</NuxtLink></li>
            </ul>
          </div>
          <div class="space-y-3">
            <h3 class="text-lg font-medium">Help</h3>
            <ul class="space-y-1">
              <li><NuxtLink to="" class="text-sm text-gray-300 hover:underline">FAQs</NuxtLink></li>
              <li><NuxtLink to="" class="text-sm text-gray-300 hover:underline">Shipping</NuxtLink></li>
              <li><NuxtLink to="" class="text-sm text-gray-300 hover:underline">Returns</NuxtLink></li>
            </ul>
          </div>
          <div class="space-y-3">
            <h3 class="text-lg font-medium">Contact</h3>
            <ul class="space-y-1">
              <li><a href="" class="text-sm text-gray-300 hover:underline">Email</a></li>
              <li><a href="" class="text-sm text-gray-300 hover:underline">Phone</a></li>
            </ul>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>

const { data: productsElect } = await useLazyFetch('https://fakestoreapi.com/products/category/electronics?limit=4');
const { data: productsCloth } = await useLazyFetch("https://fakestoreapi.com/products/category/men's clothing?limit=4");

definePageMeta({
  layout: 'products'
});
</script>

<style scoped>
/* You can add any scoped styles here if needed */
</style>