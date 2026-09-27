<script setup>
import { ref } from 'vue'

const open = ref(0)

const questions = [
  {
    title: 'Кто может участвовать в конкурсе?',
    answer: 'Участниками могут быть субъекты малого и среднего предпринимательства (МСП), зарегистрированные в Санкт-Петербурге, работающие в сфере креативных индустрий. Компании должны быть включены в реестр МСП и не находиться в процессе ликвидации или банкротства.',
  },
  {
    title: 'Как правильно оформить презентацию бренда для заявки?',
    answer: 'Требования к презентации и документам определяются условиями участия конкурса.',
  },
  {
    title: 'Как проходит голосование?',
    answer: 'Предусмотрены открытое онлайн-голосование на официальном сайте конкурса и голосование конкурсной комиссии.',
  },
  {
    title: 'До какого числа принимаются заявки?',
    answer: 'Сбор заявок проходит с 14 сентября 2025 года по 21 октября 2025 года.',
  },
]
</script>

<template>
  <section id="faq" class="container-gastro py-16 md:py-24">
    <div class="grid grid-cols-1 gap-8 md:grid-cols-[300px_1fr]">
      <h2 class="section-title">Вопросы</h2>

      <div>
        <div
          v-for="(item, index) in questions"
          :key="item.title"
          class="border-b border-white/15"
        >
          <button
            class="flex w-full items-center justify-between gap-6 py-5 text-left text-[clamp(15px,1.5vw,20px)] font-bold"
            @click="open = open === index ? -1 : index"
          >
            <span>{{ item.title }}</span>
            <span class="shrink-0 text-white/70">{{ open === index ? '−' : '+' }}</span>
          </button>

          <div
            v-if="open === index"
            class="pb-6 text-[13px] leading-[1.6] text-white/65 md:max-w-[640px]"
          >
            {{ item.answer }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>