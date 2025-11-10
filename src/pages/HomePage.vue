<template>
  <Navbar class="block" />

  <div class="mt-5">
    <swiper
      :modules="[Navigation, Pagination, Autoplay]"
      :slides-per-view="1"
      :loop="true"
      :autoplay="{ delay: 3000 }"
      navigation
      pagination
      class="w-11/12 h-[400px] rounded-2xl"
    >
      <swiper-slide v-for="(img, i) in images" :key="i">
        <img :src="img" class="w-full h-full object-cover rounded-2xl" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup>
import Navbar from "../components/Navbar.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import { Navigation, Pagination, Autoplay } from "swiper/modules";

const images = [
  "src/assets/images/slider/slide-3.jpg",
  "src/assets/images/slider/slide-4.jpg",
  "src/assets/images/slider/slide-5.jpg",
];
</script>

<style></style>
