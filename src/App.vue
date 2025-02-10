<script setup>
import NavBar from '@/components/NavBar.vue'
import New_Button from '@/components/New_Button.vue'
import bgHero from '@/assets/bg-intro-desktop.svg'
import bgHeroMobile from '@/assets/bg-intro-mobile.svg'
import bgMockup from '@/assets/image-mockups.png'
import iconOnline from '@/assets/icon-online.svg'
import iconBudgeting from '@/assets/icon-budgeting.svg'
import iconOnboarding from '@/assets/icon-onboarding.svg'
import iconApi from '@/assets/icon-api.svg'
import imageCurrency from '@/assets/image-currency.jpg'
import imgageRes from '@/assets/image-restaurant.jpg'
import imagePlane from '@/assets/image-plane.jpg'
import imageCon from '@/assets/image-confetti.jpg'
import logo from '@/assets/logo.svg'

const articles = [
  {
    image: imageCurrency,
    title: "Receive money in any currency with no fees",
    author: "Claire Robinson",
    description:
      "The world is getting smaller and we're becoming more mobile. So why should you be forced to only receive money in a single ...",
  },
  {
    image: imgageRes,
    title: "Treat yourself without worrying about money",
    author: "Wilson Hutton",
    description:
      "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you ...",
  },
  {
    image: imagePlane,
    title: "Take your Easybank card wherever you go",
    author: "Wilson Hutton",
    description:
      "We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you ...",
  },
  {
    image: imageCon,
    title: "Our invite-only Beta accounts are now live!",
    author: "Claire Robinson",
    description:
      "After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ...",
  },
];

</script>

<template>
  <header>
    <NavBar />
  </header>

  <main class="blue-text">
    <!-- Hero Section -->
    <section
  class="flex flex-col-reverse lg:flex-row justify-between px-6 md:px-12 lg:px-24 bg-light-gray overflow-hidden min-h-[600px] relative"
>
  <!-- Text Content -->
  <div class="text-center md:text-left max-w-lg mx-auto py-16 md:py-32">
    <h1 class="text-3xl md:text-5xl lg:text-6xl text-dark-blue leading-snug">
      Next generation digital banking
    </h1>
    <p class="text-[16px] md:text-[18px] text-grayish-blue my-6 leading-relaxed">
      Take your financial life online. Your Easybank account will be a one-stop-shop for
      spending, saving, budgeting, investing, and much more.
    </p>
    <New_Button label="Request Invite" class="mt-4" />
  </div>

  <!-- Mockup Image -->
  <div class="relative flex justify-center lg:justify-end w-full lg:w-auto">
    <bgHero class="hidden lg:block absolute -top-64 -right-[600px]" />
    <bgHeroMobile class="absolute sm:block lg:hidden -top-36 -left-14 -right-40" />
    <img
      :src="bgMockup"
      alt="Mobile Mockups"
      class="relative top-14 md:top-36 lg:-top-[120px] lg:-right-56 max-w-full"
      loading="lazy"
    />
  </div>
</section>

    <section class="md:px-6 grayish-blue flex flex-col gap-14 py-28">
      <div class="flex flex-col items-center text-center gap-5 px-4 md:px-20">
        <h2 class="md:text-5xl text-3xl text-dark-blue">Why choose Easybank?</h2>
        <p class="text-grayish-blue text-[16px] leading-relaxed">
          We leverage Open Banking to turn your bank account into your financial hub.
          Control your finances like never before.
        </p>
      </div>

      <div class="grid md:grid-cols-4 px-10 md:px-20 gap-9">
        <div class="flex flex-col md:items-start md:justify-start items-center justify-center gap-8">
          <iconOnline />
          <h1 class="text-2xl">Online Banking</h1>
          <p class="text-grayish-blue md:text-left text-center">Our modern web and mobile application allow you to keep track of your finances wherever you are in the world</p>
        </div>
        <div class="flex flex-col md:items-start md:justify-start items-center justify-center gap-8">
          <iconBudgeting />
          <h1 class="text-2xl">Simple Budgeting</h1>
          <p class="text-grayish-blue md:text-left text-center">See exactly where your money goes each month. Receive notifications when you're close to hitting your limits</p>
        </div>
        <div class="flex flex-col md:items-start md:justify-start items-center justify-center gap-8">
          <iconOnboarding />
          <h1 class="text-2xl">Fast Onboarding</h1>
          <p class="text-grayish-blue md:text-left text-center">We don't do branches. Open your account in minutes online and start taking control of your finances right way.</p>
        </div>
        <div class="flex flex-col md:items-start md:justify-start items-center justify-center gap-8">
          <iconApi />
          <h1 class="text-2xl">Open API</h1>
          <p class="text-grayish-blue md:text-left text-center">Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.</p>
        </div>
      </div>
    </section>
    <section class="md:px-24 px-5 py-16">
      <h2 class="text-4xl py-12">Latest Articles</h2>
      <div class="grid md:grid-cols-4 gap-7">
        <article class="bg-white rounded-2xl" v-for="(data, index) in articles" :key="index">
          <figure>
            <img class="w-full h-52 rounded-t" :src="data.image" loading="lazy">
          </figure>
          <div class="flex flex-col gap-3 p-7">
            <span class="text-xs text-grayish-blue">By {{ data.author }}</span>
            <h2 class="font-medium cursor-pointer hover:text-green-400">{{ data.title }}</h2>
            <p class="text-sm text-grayish-blue">{{ data.description }}</p>
          </div>
        </article>
      </div>
    </section>
  </main>
  <footer class="footer-bg text-white py-8">
    <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
      <!-- Left Section: Logo and Social Media Icons -->
      <div class="flex flex-col md:flex-row items-center gap-4">
        <!-- Logo -->
        <logo class="text-white" />
        <!-- Social Media Icons -->
        <div class="flex gap-4 text-xl">
          <a href="#" class="hover:text-green-400"><i class="fab fa-facebook"></i></a>
          <a href="#" class="hover:text-green-400"><i class="fab fa-youtube"></i></a>
          <a href="#" class="hover:text-green-400"><i class="fab fa-twitter"></i></a>
          <a href="#" class="hover:text-green-400"><i class="fab fa-pinterest"></i></a>
          <a href="#" class="hover:text-green-400"><i class="fab fa-instagram"></i></a>
        </div>
      </div>

      <!-- Middle Section: Navigation Links -->
      <div class="flex flex-col md:flex-row gap-4 mt-6 md:mt-0 text-center">
        <div>
          <a href="#" class="hover:text-green-400">About Us</a>
        </div>
        <div>
          <a href="#" class="hover:text-green-400">Contact</a>
        </div>
        <div>
          <a href="#" class="hover:text-green-400">Blog</a>
        </div>
        <div>
          <a href="#" class="hover:text-green-400">Careers</a>
        </div>
        <div>
          <a href="#" class="hover:text-green-400">Support</a>
        </div>
        <div>
          <a href="#" class="hover:text-green-400">Privacy Policy</a>
        </div>
      </div>

      <!-- Right Section: Request Invite Button -->
      <div class="mt-6 md:mt-0">
        <a
          href="#"
          class="bg-gradient-to-r from-green-400 to-blue-500 text-white font-bold py-2 px-6 rounded-full shadow-md hover:shadow-lg hover:opacity-90"
        >
          Request Invite
        </a>
      </div>
    </div>

    <!-- Footer Bottom -->
    <div class="mt-6 text-center text-sm text-gray-400">
      © Easybank. All Rights Reserved
    </div>
  </footer>

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

.grennish {
  color: hsl(136, 65%, 51%);
}

.footer-bg {
  background-color: hsl(233, 26%, 24%);
}
</style>
