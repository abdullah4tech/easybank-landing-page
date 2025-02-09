<script setup>
import NavBar from '@/components/NavBar.vue'
import New_Button from '@/components/New_Button.vue'
import bgHero from '@/assets/bg-intro-desktop.svg'
import bgMockup from '@/assets/image-mockups.png'
import iconOnline from '@/assets/icon-online.svg'
import iconBudgeting from '@/assets/icon-budgeting.svg'
import iconOnboarding from '@/assets/icon-onboarding.svg'
import iconApi from '@/assets/icon-api.svg'
</script>

<template>
  <header>
    <NavBar />
  </header>

  <main>
    <!-- Hero Section -->
    <section
      class="flex flex-col lg:flex-row justify-between px-6 lg:px-24 bg-light-gray overflow-hidden relative"
    >
      <!-- Text Content -->
      <div class="text-center py-32 lg:text-left max-w-lg lg:max-w-md">
        <h1 class="text-5xl text-dark-blue leading-snug">
          Next generation digital banking
        </h1>
        <p class="text-[18px] text-grayish-blue my-6 leading-relaxed">
          Take your financial life online. Your Easybank account will be a one-stop-shop for
          spending, saving, budgeting, investing, and much more.
        </p>
        <New_Button label="Request Invite" class="mt-4" />
      </div>

      <!-- Mockup Image -->
      <div class="relative w-full lg:w-auto">
        <bgHero class="absolute -top-64 -right-[600px] hidden lg:block" />
        <img :src="bgMockup" alt="Mobile Mockups" class="relative lg:-top-[120px] lg:-right-56" />
      </div>
    </section>
    <section class="bg-white">
      <div>
        <h2>Why choose Easybank?</h2>
        <p>We leverage Open Banking to turn your bank account into your financial hub. Control your finances like never before.</p>
      </div>
      <div class="grid grid-cols-4 px-20 gap-4  ">
        <div>
          <iconOnline />
          <h1>Online Banking</h1>
          <p>Our modern web and mobile application allow you to keep track of your finances wherever you are in the world</p>
        </div>
        <div>
          <iconBudgeting />
          <h1>Simple Budgeting</h1>
          <p>See exactly where your money goes each month. Receive notifications when you're close to hitting your limits</p>
        </div>
        <div>
          <iconOnboarding />
          <h1>Fast Onboarding</h1>
          <p>We don't do branches. Open your account in minutes online and start taking control of your finances right way.</p>
        </div>
        <div>
          <iconApi />
          <h1>Open API</h1>
          <p>Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.</p>
        </div>
      </div>
    </section>
    <section></section>
  </main>
</template>


<style scoped>
.bg-light-gray {
  background-color: hsl(0, 0%, 98%);
}

.text-dark-blue {
  color: hsl(233, 26%, 24%);
}

.text-grayish-blue {
  color: hsl(233, 8%, 62%);
}
</style>
