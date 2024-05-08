<template>
  <div class="bg-lightBlue">
    <div
      class="container xl:max-w-[1280px] 2xl:px-0 px-3 mx-auto flex justify-between items-center md:flex-row flex-col-reverse gap-y-10 py-[162px]"
    >
      <div class="md:w-1/2 md:max-w-[582px] xl:pe-0 lg:pe-10 md:pe-6">
        <h2
          class="text-lightBlack xl:text-[50px] lg:text-[40px] sm:text-[32px] text-[30px] font-bold lg:pb-[30px] pb-3 leading-[120%] md:text-start text-center"
        >
          Fighting the Current with your Finances?
        </h2>
        <p
          class="font-normal lg:text-lg text-base text-lightBlack tracking-[0.2px] leading-[130%] md:text-start text-center lg:pb-[50px] pb-3"
        >
          You could be paying separate fees for each financial product you use.
        </p>
        <div class="flex flex-col lg:gap-[30px] gap-3">
          <div
            v-for="(item, index) in productFee"
            :key="index"
            class="flex items-center justify-between lg:px-[30px] lg:py-[25px] p-3.5 bg-white border border-[#EEEEEE]"
          >
            <div class="flex items-center gap-5">
              <component :is="item.icon" />
              <!-- Render the component using :is directive -->
              <p class="font-bold lg:text-2xl text-xl text-black">{{ item.label }}</p>
            </div>
            <p class="font-bold lg:text-2xl text-xl text-darkPink">{{ item.fees }}</p>
          </div>
        </div>
      </div>
      <div class="md:w-1/2 md:max-w-[600px] max-w-[400px]">
        <img
          class="w-full"
          src="/assets/images/fighting/finances.png"
          alt="finances"
        />
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
import Cash from "./icons/Cash.vue";
import DollorSign from "./icons/DollorSign.vue";
import PrepaidCard from "./icons/PrepaidCard.vue";

// Ensure correct import paths and component registration

const productFee = ref([
  { icon: Cash, label: "Product", fees: "4.5-9.9% Fee" },
  { icon: DollorSign, label: "Remittance", fees: "4.-11.5% Fee" },
  { icon: PrepaidCard, label: "Remittance", fees: "4.-11.5% Fee" },
]);
</script>
