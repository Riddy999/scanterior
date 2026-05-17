<script setup lang="ts">
import { RouterView } from 'vue-router'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
</script>

<template>
    <Header />

      <RouterView />

    <Footer />
</template>

<style scoped>
.app-shell {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.page-view {
  flex: 1;
  min-height: 0;
  display: flex;
  flex-direction: column;
}

header {
  line-height: 1.5;
}
</style>
