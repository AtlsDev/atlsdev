<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const route = useRoute()

const items = computed<NavigationMenuItem[]>(() => [
  {
    label: 'Blog',
    to: '/blog',
    active: route.path.startsWith('/blog')
  }
])
</script>

<template>
  <UHeader>
    <template #title>
      <AppLogo class="h-8 w-auto" />
    </template>

    <UNavigationMenu :items="items" />

    <template #body>
      <UNavigationMenu
        orientation="vertical"
        :items="items"
      />
    </template>

    <template #right>
      <UColorModeButton />

      <UTooltip
        text="Open on GitHub"
        :kbds="['meta', 'G']"
      >
        <UButton
          color="neutral"
          variant="ghost"
          to="https://github.com/nuxt/ui"
          target="_blank"
          icon="i-simple-icons-github"
          aria-label="GitHub"
        />
      </UTooltip>
    </template>
  </UHeader>
</template>
