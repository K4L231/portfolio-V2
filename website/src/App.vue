<template>
  <main class="main">
    <Header />
    <Made />
  </main>
</template>

<script setup lang="ts">

import Header from "./components/header.vue"
import Made from "./components/made.vue"
</script>

<style>
  * {
        font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  }
  body {
    background-color: #F3F3F3;
  }
  .main {
    width: 80%;
    margin: 0 auto;
    max-width: 1136px;
  }


    @media (max-width: 650px) {
    .main {
      width: 95%;
    }
  }

  
</style>
