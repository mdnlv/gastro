<script setup>
const stages = [
  ['ОНЛАЙН', '14 сентября 2025 – 21 октября 2025', 'Сбор заявок'],
  ['ОНЛАЙН', '26 октября 2025 – 3 ноября 2025', 'Открытое голосование на официальном сайте конкурса'],
  ['ОНЛАЙН', '26 октября 2025 – 3 ноября 2025', 'Голосование конкурсной комиссии'],
  ['ОЧНО', '11 ноября 2025', 'Объявление победителей'],
]
</script>

<template>
  <section id="stages" class="container-gastro py-16 md:py-24">
    <div class="grid grid-cols-1 gap-8 md:grid-cols-[300px_1fr]">
      <h2 class="section-title">Этапы</h2>

      <div>
        <div
          v-for="([mode, date, title], index) in stages"
          :key="title"
          class="grid grid-cols-1 items-center gap-4 border-b border-white/15 py-6 md:grid-cols-[130px_1fr_1fr] md:gap-8"
        >
          <span
            class="w-fit rounded-full border border-gastro-lime px-5 py-2 text-center text-[11px] font-bold uppercase"
          >
            {{ mode }}
          </span>
          <span class="text-[12px] text-white/60">{{ date }}</span>
          <strong class="text-[clamp(16px,1.6vw,22px)] font-black uppercase leading-[1.1]">{{ title }}</strong>
        </div>
      </div>
    </div>
  </section>
</template>