<script setup lang="ts">
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import TrendsComponent from './components/TrendsComponent.vue'
</script>

<template>
  <header>
    <HeaderComponent />
  </header>
  <main>
    <MainComponent />
  </main>
  <section class="trends" id="trends">
    <TrendsComponent />
  </section>
</template>

<style>
@import './assets/css/base.css';
</style>

<style scoped>
header {
  display: flex;
  position: sticky;
  padding: 2rem;
  top: 0;
  flex-direction: column;
  justify-content: space-between;
  height: 80vh;
  border-right: 1px solid grey;
}


</style>
