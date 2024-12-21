<template>
  <div>
    <h1 class="text-2xl font-bold mb-6">Latest Perth Glory News</h1>
    <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      <article v-for="post in news" :key="post.id" class="border rounded-lg p-4 shadow-sm">
        <img :src="post.image" :alt="post.title" class="w-full h-48 object-cover rounded mb-4">
        <h2 class="text-xl font-semibold mb-2">{{ post.title }}</h2>
        <p class="text-gray-600 mb-4">{{ post.excerpt }}</p>
        <div class="flex justify-between items-center">
          <span class="text-sm text-gray-500">{{ post.date }}</span>
          <NuxtLink :to="`/news/${post.id}`" class="text-purple-800 hover:text-purple-600">
            Read More →
          </NuxtLink>
        </div>
      </article>
    </div>
  </div>
</template>

<script setup>
const news = ref([
  {
    id: 1,
    title: 'Glory Secure Crucial Victory',
    excerpt: 'Perth Glory claimed an important win in their latest A-League fixture...',
    date: '2024-03-20',
    image: '/images/placeholder-1.jpg'
  },
  // Add more news items as needed
]);
</script> 