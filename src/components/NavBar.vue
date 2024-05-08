<template>
  <div
    class="container mx-auto flex justify-between items-center py-[30px] xl:max-w-[1320px] 2xl:px-0 px-3"
  >
    <a href="/"><CanalLogo /></a>
    <div class="flex lg:gap-[100px] gap-10 items-center">
      <div class="sm:flex hidden gap-[30px] items-center">
        <a class="text-[18px] font-semibold text-lightBlack" href="/"
          >Product</a
        >
        <a class="text-[18px] font-semibold text-lightBlack" href="/"
          >Mission</a
        >
      </div>
      <div class="flex items-center sm:gap-8 gap-5">
        <GlobeStroke />
        <button
          class="sm:flex hidden items-center py-[13px] px-5 border border-green text-green gap-[5px] font-semibold text-[18px] hover:shadow-[0px_150px_0px_-67px_rgba(255,211,0,1)_inset] duration-500 hover:text-white group hover:border-yellow"
        >
          <PluseGreen /> Join
        </button>
        <button @click="togglePosition" class="sm:hidden relative z-[101]">
          <MenuIcon />
        </button>
      </div>
    </div>
    <div
      :class="[
        { 'left-0': !isLeft0, '-left-full': isLeft0 },
        'min-h-screen w-full top-0 fixed flex sm:hidden justify-center items-center flex-col gap-4 z-50 duration-300 bg-white',
      ]"
    >
      <a class="text-[18px] font-semibold text-lightBlack" href="/">Product</a>
      <a class="text-[18px] font-semibold text-lightBlack" href="/">Mission</a>
      <button
        class="flex items-center py-[13px] px-5 border border-green text-green gap-[5px] font-semibold text-[18px] hover:shadow-[0px_150px_0px_-67px_rgba(255,211,0,1)_inset] duration-500 hover:text-white group hover:border-yellow"
      >
        <PluseGreen /> Join
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import CanalLogo from "./icons/CanalLogo.vue";
import GlobeStroke from "./icons/GlobeStroke.vue";
import MenuIcon from "./icons/MenuIcon.vue";
import PluseGreen from "./icons/PluseGreen.vue";

const isLeft0 = ref(true);

const togglePosition = () => {
  isLeft0.value = !isLeft0.value;
};
</script>

<style scoped>
/* Add any scoped styles here */
</style>
