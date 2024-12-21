<template>
  <div>
    <nav class="bg-purple-800 text-white p-4">
      <div class="container mx-auto flex justify-between items-center">
        <NuxtLink to="/" class="text-xl font-bold">Perth Glory News</NuxtLink>
        <div class="space-x-4">
          <NuxtLink to="/" class="hover:text-purple-200">Home</NuxtLink>
          <NuxtLink to="/news" class="hover:text-purple-200">Latest News</NuxtLink>
        </div>
      </div>
    </nav>
    <main class="container mx-auto p-4">
      <NuxtPage />
    </main>
  </div>
</template>
