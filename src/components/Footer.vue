<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="bg-lightBlack">
    <div
      class="container xl:max-w-[1280px] 2xl:px-0 px-3 mx-auto xl:pb-[150px] sm:py-[104px] py-[70px] flex justify-between flex-wrap gap-10"
    >
      <div class="sm:w-auto w-full flex flex-col items-center sm:items-start">
        <a href="/"><CanalFooter /></a>
        <h3
          class="md:pt-[50px] pt-8 pb-5 text-white uppercase font-semibold text-[22px] tracking-[0.1px] sm:text-start text-center"
        >
          Follow Us
        </h3>
        <div class="flex gap-[13px]">
          <a
            v-for="(logo, index) in socialLogo"
            :key="index"
            class="w-11 h-11 rounded-full bg-green flex justify-center items-center hover:bg-yellow duration-300"
            :href="logo.link"
            ><component :is="logo.icon"
          /></a>
        </div>
      </div>
      <div v-for="(item, index) in footerLinks" :key="index">
        <h3
          class="pb-[24px] text-white font-bold md:text-2xl text-xl text-center sm:text-start"
        >
          {{ item.heading }}
        </h3>
        <ul class="flex flex-col gap-y-[14px]">
          <li
            class="text-center sm:text-start"
            v-for="(value, index) in item.links"
            :key="index"
          >
            <a
              class="font-normal md:text-lg text-base text-white tracking-[0.2px] hover:text-yellow duration-300"
              :href="value.url"
              >{{ value.title }}</a
            >
          </li>
        </ul>
      </div>
      <div class="flex flex-col items-center sm:items-start">
        <h3
          class="pb-2.5 text-white font-bold md:text-2xl text-xl text-center sm:text-start"
        >
          Subscribe to Our Newsletter
        </h3>
        <a
          class="font-normal md:text-lg text-base text-white tracking-[0.2px] hover:text-yellow duration-300 text-center sm:text-start"
          href="/"
          >Stay up to date</a
        >
        <div
          class="py-[4.5px] pe-[4.5px] bg-white sm:w-[419px] w-full max-w-[400px] mt-9 flex items-center"
        >
          <input
            class="ps-[30px] py-[18px] bg-white outline-none placeholder:text-lg text-lg placeholder:text-lightGray text-lightGray pe-3 w-full"
            type="text"
            placeholder="Your email "
          />
          <button
            class="bg-green px-[30px] py-[18px] text-lg text-white font-normal tracking-[.2px] duration-500 hover:shadow-[0px_150px_0px_-67px_rgba(255,211,0,1)_inset] "
          >
            Subscribe
          </button>
        </div>
      </div>
    </div>
    <p
      class="text-center py-5 border-t border-white font-normal md:text-lg text-base text-white px-3"
    >
      Copyright 2024 uifry.com all rights reserved
    </p>
  </div>
</template>
<script setup>
import { ref } from "vue";
import CanalFooter from "./icons/CanalFooter.vue";
import FaceBook from "./icons/FaceBook.vue";
import InstaGram from "./icons/InstaGram.vue";
import LinkedIn from "./icons/LinkedIn.vue";
import TwiiterX from "./icons/TwiiterX.vue";
const socialLogo = ref([
  { icon: FaceBook, link: "/" },
  { icon: TwiiterX, link: "/" },
  { icon: InstaGram, link: "/" },
  { icon: LinkedIn, link: "/" },
]);
const footerLinks = ref([
  {
    heading: "Links",
    links: [
      { title: "Home", url: "/" },
      { title: "About us", url: "/" },
      { title: "Bookings", url: "/" },
      { title: "Blog", url: "/" },
    ],
  },
  {
    heading: "Legal",
    links: [
      { title: "Terms of use", url: "/" },
      { title: "Privacy policy", url: "/" },
      { title: "Cookie policy", url: "/" },
    ],
  },
  {
    heading: "Product",
    links: [
      { title: "Take tour", url: "/" },
      { title: "Live chat", url: "/" },
      { title: "Reveiws", url: "/" },
    ],
  },
]);
</script>
