<script setup>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Nominations from './components/Nominations.vue'
import Stages from './components/Stages.vue'
import AboutContest from './components/AboutContest.vue'
import NominationsList from './components/NominationsList.vue'
import Prizes from './components/Prizes.vue'
import FAQ from './components/FAQ.vue'
import Organizers from './components/Organizers.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="min-h-screen overflow-x-clip bg-gastro-bg text-white">
    <Header />

    <main>
      <Hero />
      <Nominations />
      <Stages />
      <AboutContest />
      <NominationsList />
      <Prizes />
      <FAQ />
      <Organizers />
    </main>

    <Footer />
  </div>
</template>