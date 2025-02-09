<script setup>
import NavBar from '@/components/NavBar.vue'
import New_Button from '@/components/New_Button.vue'
import bgHero from '@/assets/bg-intro-desktop.svg'
import bgMockup from '@/assets/image-mockups.png'
</script>


<template>
  <header>
    <NavBar />
  </header>

  <main>
    <section class="flex">
      <div>
        <h1>Next generation digital banking</h1>
        <p>Take your financial life online. Your Easybank account will be one-stop-shop for spending, saving, budgeting, investing, and much more.</p>
        <New_Button label="Request Invite" />
      </div>
      <div class="relative">
        <bgHero class="absolute" />
        <img :src="bgMockup" class="absolute left-48 top-32" />
      </div>
    </section>
    <section></section>
    <section></section>
  </main>
</template>
