<script setup lang="ts">
import { withoutTrailingSlash } from 'ufo'

const route = useRoute()
const routePath = computed(() => withoutTrailingSlash(route.path))

const { data: blog } = await useAsyncData(routePath.value, () =>
  queryCollection('blog').path(routePath.value).first()
)
</script>

<template>
  <UPage v-if="blog">
    <UContainer>
      <UPageHeader v-bind="blog" />

      <ContentRenderer :value="blog" />
    </UContainer>
  </UPage>
</template>
