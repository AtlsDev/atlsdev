<script setup lang="ts">
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    // { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'tr'
  }
})

const title = 'Atlaxt'
// const description = ''

useSeoMeta({
  title,
  // description,
  ogTitle: title,
  // ogDescription: description,
  // ogImage: 'https://ui.nuxt.com/assets/templates/nuxt/starter-light.png',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <UApp>
    <AppHeader />
    <UMain>
      <NuxtLayout>
        <NuxtPage />
      </NuxtLayout>
    </UMain>
    <AppFooter />
  </UApp>
</template>
