<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div class="header">
        <h1>datashoppen&nbsp;</h1>
        <router-link class="links" to="/">> produkter&nbsp;</router-link>
        <a class="links" target="_blank" href="https://www.inet.se/">> hem</a>
    </div>
</template>

<style lang="scss">

  .header:router {
    color: black;
    background-color: blue;
  }

  a {
    color: black;
  }

  .header {
    position: fixed;
    top: 0%;
    width: 100%;
    height: 10vh;
    background-color: rgb(160,160,160);
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>