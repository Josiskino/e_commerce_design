<script setup>
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue';
import Navbar02 from './components/Navbar02.vue';
import MapView from './views/MapView.vue'
</script>

<template>
<Navbar />
<Navbar02 />
  <RouterView />
</template>

<style>
/* Global styles will be handled in src/assets/main.css or similar */
</style>
