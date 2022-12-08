<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div class="test">
        <router-link to="/about">gg</router-link>
    </div>
</template>

<style lang="scss">

  router-link {
    width: 10vh;
    height: 10vh;
  }

  .test {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 10vh;
    height: 10vh;
    background-color: red;
  }
</style>