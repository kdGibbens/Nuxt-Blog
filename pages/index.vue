<script setup>
useSeoMeta({
  title: 'Main Page',
  description: 'Main Page for KDG',
  ogTitle: 'Main Page',
  ogDescription: 'Main Page for KDG',
  ogImage: '[og:image]',
  ogUrl: '[og:url]',
  twitterTitle: '[twitter:title]',
  twitterDescription: '[twitter:description]',
  twitterImage: '[twitter:image]',
  twitterCard: 'summary',
});
useHead({
  htmlAttrs: { lang: 'en' },
  link: [{ rel: 'icon', type: 'image/png', href: '/favicon.ico' }],
});
</script>

<template>Hello from Nuxt</template>
