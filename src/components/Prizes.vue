<script setup>
const prizes = [
  'Сюжет о бренде на одном из ведущих телеканалов Санкт-Петербурга',
  'Упоминание бренда в социальных сетях профильного блогера и/или крупном тематическом паблике',
  'Настройка и ведение рекламной кампании в сети Интернет',
  'Подготовка и размещение рекламного ролика на российском онлайн-сервисе для хостинга и просмотра видео',
]
</script>

<template>
  <section class="container-gastro py-16 md:py-24">
    <div class="grid grid-cols-1 gap-8 md:grid-cols-[300px_1fr]">
      <h2 class="section-title">Призы</h2>

      <div class="glass-card rounded-[20px] p-6 md:p-8">
        <h3 class="text-[clamp(20px,2vw,28px)] font-black uppercase">1 место</h3>

        <div class="mt-6 grid gap-3">
          <div
            v-for="prize in prizes"
            :key="prize"
            class="rounded-[14px] bg-white/10 px-5 py-4 text-[13px] leading-[1.45] text-white/90"
          >
            {{ prize }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>