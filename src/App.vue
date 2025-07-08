<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div class="container">

    </div>
    <div class="nav">
        <RouterLink to="/">Home</RouterLink> |
        <RouterLink to="/about">About</RouterLink> |
         <RouterLink to="/login">Login</RouterLink> |
    </div>

      <RouterView />
</template>

<style lang="scss">
    @import "@/assets/all.scss";
</style>
