<script setup>
const organizers = [
  {
    title: 'Фонд развития субъектов малого и среднего предпринимательства в Санкт-Петербурге',
    icon: '↗',
  },
  {
    title: 'Комитет по промышленной политике, инновациям и торговле Санкт-Петербурга',
    icon: '✥',
  },
]
</script>

<template>
  <section class="container-gastro py-16 md:py-24">
    <h2 class="section-title text-center">Организаторы</h2>

    <div class="mx-auto mt-12 grid max-w-[1100px] grid-cols-1 gap-4 md:grid-cols-2">
      <div
        v-for="item in organizers"
        :key="item.title"
        class="glass-card flex min-h-[110px] items-center gap-5 rounded-[16px] px-6"
      >
        <div class="grid h-14 w-14 shrink-0 place-items-center rounded-full border border-cyan-400 text-2xl">
          {{ item.icon }}
        </div>
        <div class="text-[14px] font-semibold leading-[1.35]">{{ item.title }}</div>
      </div>
    </div>
  </section>
</template>