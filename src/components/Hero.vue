<script setup>
import { computed, onMounted, onUnmounted, ref } from 'vue'

const deadline = new Date('2025-09-14T00:00:00+03:00').getTime()
const now = ref(Date.now())
let timer

const pad = (n) => String(n).padStart(2, '0')

const remaining = computed(() => {
  const diff = Math.max(0, deadline - now.value)
  return {
    days: Math.floor(diff / 86400000),
    hours: Math.floor((diff / 3600000) % 24),
    minutes: Math.floor((diff / 60000) % 60),
    seconds: Math.floor((diff / 1000) % 60),
  }
})

onMounted(() => {
  timer = setInterval(() => (now.value = Date.now()), 1000)
})
onUnmounted(() => clearInterval(timer))
</script>

<template>
  <section class="relative min-h-[720px] pt-[130px]">
    <div class="food-scene">
      <div class="food-cup"></div>
      <div class="food-burger"></div>
      <div class="food-pasta"></div>
      <div class="food-cube"></div>
    </div>

    <div class="container-gastro relative z-10">
      <div class="max-w-[1000px]">
        <h1 class="text-[clamp(30px,4.4vw,58px)] font-black uppercase leading-[.95] tracking-[-.03em]">
          Конкурс лучших брендов<br />
          гастроиндустрии Санкт-Петербурга
        </h1>

        <div class="mt-2 text-[clamp(64px,9vw,120px)] font-black leading-none tracking-[-.04em]">2025</div>

        <div class="mt-10 w-[300px] rounded-[16px] border border-gastro-lime bg-white/[.03] p-5">
          <h2 class="text-[16px] font-black uppercase leading-[1.1]">Сроки проведения<br />конкурса</h2>

          <div class="mt-10 text-[16px] font-bold leading-[1.25]">
            14 сентября 2025 –<br />
            21 октября 2025
          </div>

          <div class="mt-4 h-1.5 overflow-hidden rounded-full bg-white/20">
            <div class="h-full w-[68%] bg-gastro-lime"></div>
          </div>

          <div class="mt-2 text-[10px] text-white/60">
            До начала {{ remaining.days }} дней {{ remaining.hours }} часа
            {{ remaining.minutes }} минут {{ pad(remaining.seconds) }} секунды
          </div>
        </div>

        <a href="#nominations" class="neon-button mt-5 block w-[300px] px-6 py-4 text-center text-[14px]">
          Подать заявку
        </a>
      </div>
    </div>
  </section>
</template>