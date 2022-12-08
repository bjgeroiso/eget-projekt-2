<script setup lang="ts">
import AppHeader from '@/components/Header.vue'
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Box from '@/components/Box.vue' 
// import AppFooter from '@/components/Footer.vue'
</script>

<template>
  <div class="hhh">
    <app-header />
    <router-view />
  </div>
</template>

<style lang="scss">

  .hhh {
    position: fixed;
    top: 0%;
    left: 0%;
    width: 100%;
    height: 100%;
    background-color: grey;
    color: black;
  }

  .links {
    color: black;
  }

</style>