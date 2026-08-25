<script setup lang="ts">
import LogoDark from '/sign_black.png'
import LogoLight from '/sign_white.png'
</script>

<template>
  <UColorModeImage
    :light="LogoDark"
    :dark="LogoLight"
  />
</template>
