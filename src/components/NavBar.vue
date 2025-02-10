<script setup>
import New_Button from '@/components/New_Button.vue'
import logo from '@/assets/logo.svg'
import iconHamburger from '@/assets/icon-hamburger.svg'
import iconClose from '@/assets/icon-close.svg'
import { ref } from 'vue';


const isOpen = ref(false)
</script>

<template>
  <nav class="relative flex items-center justify-around py-5 bg-white">
    <logo />

    <!-- Desktop/Laptop -->
    <ul class="md:flex hidden space-x-8 text-gray-500 transition-colors ease-out">
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Home</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[3px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">About</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[3px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Contact</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[3px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Blog</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[3px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Careers</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[3px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
    </ul>

    <div class="w-10 h-10 flex items-center justify-center">
      <iconHamburger v-show="!isOpen" @click.prevent="isOpen = !isOpen" class="md:hidden" />
      <iconClose v-show="isOpen" @click.prevent="isOpen = !isOpen" />
    </div>

    <transition
      enter-active-class="duration-300 ease-out"
      enter-from-class="opacity-0 scale-90"
      enter-to-class="opacity-100 scale-100"
      leave-active-class="duration-300 ease-in"
      leave-from-class="opacity-100 scale-100"
      leave-to-class="opacity-0 scale-90"
    >
      <!-- Mobile menu -->
      <div v-show="isOpen" class="absolute md:hidden bg-white shadow-2xl py-14 px-32 top-24 z-10 rounded">
        <ul class="flex flex-col gap-5">
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
          <li><a href="#">Blog</a></li>
          <li><a href="#">Careers</a></li>
        </ul>
      </div>
    </transition>
    <New_Button class="md:block hidden" label="Request Invite" />
  </nav>
</template>
