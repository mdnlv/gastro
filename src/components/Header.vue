<template>
  <header class="absolute left-0 top-0 z-50 w-full">
    <div
      class="mx-auto flex h-[72px] items-center gap-3"
      style="width: min(100% - 84px, 1560px)"
    >
      <a href="#" class="flex shrink-0 items-center gap-2.5">
        <span class="grid h-9 w-9 place-items-center rounded-full bg-white text-[11px] font-black text-gastro-bg">★</span>
        <span class="hidden text-[9px] font-bold uppercase leading-[1.15] tracking-tight sm:block">
          Конкурс лучших брендов<br />гастроиндустрии<br />Санкт-Петербурга
        </span>
      </a>

      <div class="hidden h-[52px] shrink-0 items-center gap-4 rounded-full border border-white/20 px-6 xl:flex">
        <span class="shrink-0 text-[11px] font-black uppercase leading-[1.05]">При<br />поддержке</span>
        <span class="h-8 w-px shrink-0 bg-white/20"></span>
        <span class="flex items-center gap-2 text-[8px] font-semibold uppercase leading-[1.15] text-white/80">
          <span class="grid h-7 w-7 shrink-0 place-items-center rounded-full border border-white/30 text-[10px]">◈</span>
          <span>Фонд развития субъектов малого<br />и среднего предпринимательства<br />в Санкт-Петербурге</span>
        </span>
        <span class="flex items-center gap-2 text-[8px] font-semibold uppercase leading-[1.15] text-white/80">
          <span class="grid h-7 w-7 shrink-0 place-items-center rounded-full border border-white/30 text-[10px]">✥</span>
          <span>Комитет по промышленной<br />политике, инновациям<br />и торговле Санкт-Петербурга</span>
        </span>
      </div>

      <nav class="ml-auto hidden shrink-0 items-center gap-6 text-[11px] font-semibold lg:flex">
        <a href="#about" class="transition-colors hover:text-gastro-lime">О конкурсе</a>
        <a href="#nominations" class="transition-colors hover:text-gastro-lime">Номинации</a>
        <a href="#stages" class="transition-colors hover:text-gastro-lime">Условия участия</a>
        <a href="#faq" class="transition-colors hover:text-gastro-lime">Контакты</a>
      </nav>

      <a href="#nominations" class="neon-button ml-auto shrink-0 whitespace-nowrap px-6 py-3.5 text-[12px] uppercase lg:ml-6">
        Подать заявку
      </a>
    </div>
  </header>
</template>