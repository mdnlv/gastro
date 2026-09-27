<script setup>
const items = [
  {
    title: 'Лучший кондитерский бренд',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    title: 'Лучшая кофейня',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    title: 'Лучший стрит-фуд',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    title: 'Открытие года',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut',
  },
  {
    title: 'Молодой ресторатор',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut',
  },
]
</script>

<template>
  <section class="container-gastro py-16 md:py-24">
    <div class="grid grid-cols-1 gap-8 md:grid-cols-[300px_1fr]">
      <h2 class="section-title">Номинации</h2>

      <div>
        <div
          v-for="item in items"
          :key="item.title"
          class="grid grid-cols-1 items-center gap-4 border-b border-white/15 py-6 md:grid-cols-[1fr_1fr_auto] md:gap-8"
        >
          <h3 class="text-[clamp(20px,2.2vw,30px)] font-black uppercase leading-[1.05] tracking-[-.02em]">
            {{ item.title }}
          </h3>
          <p class="text-[12px] leading-[1.5] text-white/60">{{ item.text }}</p>
          <a
            href="#"
            class="neon-button whitespace-nowrap px-8 py-4 text-center text-[14px] md:justify-self-end"
          >
            Подать заявку
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
