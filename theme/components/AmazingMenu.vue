<script lang="ts" setup>
import type { AmazingTheme } from 'valaxy-theme-amazing'
import { useThemeConfig } from 'valaxy'
import { computed } from 'vue'
const themeConfig = useThemeConfig<AmazingTheme>()
const nav = computed(() => themeConfig.value.nav || [])
</script>

<template>
  <div class="flex items-center h-12.5">
    <AmazingMenuItem v-for="(item, index) in nav" :key="index" :item="item" />
  </div>
</template>

<style lang="scss" scoped></style>
