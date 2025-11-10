<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <div class="min-h-screen bg-white text-neutral-900 font-sans antialiased">
    <header class="sticky top-0 bg-white/80 backdrop-blur border-b border-neutral-200">
      <div class="mx-auto max-w-5xl px-4 py-4 flex items-center justify-between transition-[padding]">
        <RouterLink to="/" class="font-medium inline-flex items-center gap-2">
          <span>Abka TacimbiDoombi</span>
        </RouterLink>
        <Navbar />
      </div>
    </header>
    <!-- 统一内容容器，使所有视图宽度/左右内边距一致 -->
    <main class="mx-auto max-w-5xl px-4">
      <RouterView />
    </main>
    <Footer />
  </div>
</template>

<style scoped></style>
