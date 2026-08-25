<script setup lang="ts">
// todo: içerikleri çekme
const { data: blogs } = useAsyncData(() => queryCollection('blog').order('date', 'DESC').all())
</script>

<template>
  <UPage>
    <UPageBody>
      <UContainer>
        <UBlogPosts>
          <UBlogPost
            v-for="blog in blogs"
            :key="blog.id"
            v-bind="blog"
            :to="blog.path"
          />
        </UBlogPosts>
      </UContainer>
    </UPageBody>
  </UPage>
</template>
