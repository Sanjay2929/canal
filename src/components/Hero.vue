<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="lg:min-h-[calc(100vh-115px)] flex items-center">
    <div
      class="container mx-auto xl:max-w-[1320px] 2xl:px-0 px-3 flex items-center justify-between py-16 flex-col-reverse md:flex-row"
    >
      <div class="md:w-[52%]">
        <h1
          class="xl:text-[64px] lg:text-[50px] sm:text-[42px] text-[36px] relative z-[1] text-lightBlack font-bold leading-[120%] md:text-start text-center"
        >
          The Route to Upward Financial Mobility is Open
        </h1>
        <p
          class="pt-[30px] font-bold lg:text-2xl sm:text-xl text-lg text-greyscale lg:pb-[50px] pb-6 max-w-[550px] md:text-start text-center"
        >
          Turn fees of check cashing and remittances into increased saving and
          spending.
        </p>
        <h2
          class="font-bold lg:text-2xl sm:text-xl text-lg text-green pb-4 md:text-start text-center"
        >
          Join the Waitlist
        </h2>
        <div class="flex gap-5 max-w-[530px] mx-auto md:ms-0 sm:flex-row flex-col  items-center">
          <label
            for="email"
            class="flex gap-2.5 items-center px-5 sm:py-[18px] py-3 border w-full bg-gray-200"
          >
            <EmailLetter />
            <input
              type="email"
              class="w-full placeholder:text-greyscale placeholder:text-[18px] bg-transparent"
              placeholder="Enter Your Email Address"
            />
          </label>
          <button
            class="sm:py-[17px] py-3 px-[25px] bg-green text-white font-normal text-lg w-[122px] text-nowrap duration-500 hover:shadow-[0px_150px_0px_-67px_rgba(255,211,0,1)_inset] "
          >
            Join Now
          </button>
        </div>
      </div>
      <div
        class="md:w-[45%] md:max-w-[546px] w-[80%] max-w-[400px] relative sm:mb-32 mb-16 sm:mt-14 mt-8 md:my-0"
      >
        <img
          class="w-full"
          src="/assets/images/hero/iphone-bg-blur.png"
          alt="blur"
        />
        <img
          class="w-full absolute z-0 top-[53%] left-1/2 -translate-x-1/2 -translate-y-1/2 lg:px-7 mobile_animate"
          src="/assets/images/hero/mobile.png"
          alt="blur"
        />
      </div>
    </div>
  </div>
</template>
<script setup>
import EmailLetter from "./icons/EmailLetter.vue";
</script>
