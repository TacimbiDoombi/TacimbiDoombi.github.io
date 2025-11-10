<script setup lang="ts">
// 导航栏无需 props
</script>

<template>
  <nav class="hidden sm:flex gap-6 text-sm text-neutral-600">
    <router-link to="/bookmarks" class="hover:text-neutral-900">Bookmarks</router-link>
    <router-link to="/about" class="hover:text-neutral-900">About</router-link>
  </nav>
</template>
