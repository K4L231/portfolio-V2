<template>
  <main class="main">
    <Header />
  </main>
</template>

<script setup lang="ts">

import Header from "./components/header.vue"
</script>

<style>
  body {
    background-color: #F3F3F3;
  }
  .main {
    width: 80%;
    margin: 0 auto;
  }

  @media (max-width: 1024px) {
    .main {
      width: 95%;
    }
}
</style>
