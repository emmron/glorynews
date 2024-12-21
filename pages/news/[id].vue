<template>
  <div>
    <NuxtLink to="/news" class="text-purple-800 hover:text-purple-600 mb-4 inline-block">
      ← Back to News
    </NuxtLink>
    <article v-if="post" class="max-w-3xl mx-auto">
      <img :src="post.image" :alt="post.title" class="w-full h-64 object-cover rounded-lg mb-6">
      <h1 class="text-3xl font-bold mb-4">{{ post.title }}</h1>
      <div class="text-gray-500 mb-6">{{ post.date }}</div>
      <div class="prose max-w-none">
        {{ post.content }}
      </div>
    </article>
  </div>
</template>

<script setup>
const route = useRoute();
const id = parseInt(route.params.id);

// This would typically come from an API
const post = ref({
  id: 1,
  title: 'Glory Secure Crucial Victory',
  content: 'Full article content here...',
  date: '2024-03-20',
  image: '/images/placeholder-1.jpg'
});
</script> 