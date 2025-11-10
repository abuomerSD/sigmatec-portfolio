<script setup>
import Navbar from "./components/Navbar.vue";
import Slide from "./components/Slide.vue";
import About from "./components/About.vue";
import Products from "./components/Products.vue";
import HomePage from "./pages/HomePage.vue";
</script>

<template>
  <div class="flex flex-col gap-5">
    <Navbar />
    <Slide />
    <About />
    <Products />
  </div>
  <!-- <HomePage /> -->
</template>

<style scoped></style>
