<script setup>
import New_Button from '@/components/New_Button.vue'
import logo from '@/assets/logo.svg'
</script>

<template>
  <nav class="flex items-center justify-around py-5 bg-white">
    <logo />
    <ul class="flex space-x-8 text-gray-500 transition-colors ease-out">
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Home</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[5px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">About</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[5px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Contact</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[5px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Blog</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[5px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
      <li class="relative cursor-pointer group hover:text-black">
        <a href="#">Careers</a>
        <span
          class="absolute top-[51px] left-0 w-full h-[5px] bg-gradient-to-r from-lime-200 to-blue-500 scale-x-0 group-hover:scale-x-100 transition-transform duration-500"
        ></span>
      </li>
    </ul>
    <New_Button label="Request Invite" />
  </nav>
</template>
