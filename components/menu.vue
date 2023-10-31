<template>
  <nav>
    <ul class="flex space-x-4 font-mono">
      <li><NuxtLink to="/" class="link">Home</NuxtLink></li>
      <li><NuxtLink to="/about" class="link">About</NuxtLink></li>
      <li><NuxtLink to="/projects" class="link">Projects</NuxtLink></li>
    </ul>
  </nav>
</template>

<style scoped>
.link {
  @apply p-2 hover:bg-red-200;
}
</style>
