<template>
  <v-container>
    <PageNavigator v-if="keyValid"></PageNavigator>
    <Welcome v-else></Welcome>
  </v-container>
</template>

<script setup>
import PageNavigator from './pages/PageNavigator.vue'
import Welcome from './pages/Welcome.vue'

var keyValid = false;
console.log('👋 This message is being logged by "App.vue", included via Vite');
</script>
