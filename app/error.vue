<script setup lang="ts">
import type { NuxtError } from '#app'

const props = defineProps<{ error: NuxtError }>()
</script>

<template>
  <UError
    :error="{
      statusCode: props.error.status,
      statusMessage: 'Page not found',
      message: props.error.message
    }"
  />
</template>
