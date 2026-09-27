<script setup>
const nominations = [
  { title: 'Лучший кондитерский бренд', class: 'bg-gastro-purple' },
  { title: 'Лучшая кофейня', class: 'bg-gastro-lime justify-end' },
  { title: 'Лучший стрит-фуд', class: 'bg-gastro-cyan' },
  { title: 'Открытие года', class: 'bg-gastro-orange justify-end' },
  { title: 'Молодой ресторатор', class: 'bg-gastro-yellow' },
]
</script>

<template>
  <section id="nominations" class="relative z-20 -mt-6">
    <div class="container-gastro !w-full">
      <div
        v-for="item in nominations"
        :key="item.title"
        class="nomination-bar mx-0 mb-2.5"
        :class="item.class"
      >
        {{ item.title }}
      </div>
    </div>
  </section>
</template>