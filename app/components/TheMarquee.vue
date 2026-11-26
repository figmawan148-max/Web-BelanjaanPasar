<template>
  <div class="group relative overflow-hidden bg-gradient-to-r from-[#00431a] via-[#00652c] to-[#00431a] py-6">
    <!-- Fade mask kiri-kanan -->
    <div class="pointer-events-none absolute inset-y-0 left-0 z-10 w-16 bg-gradient-to-r from-[#00431a] to-transparent md:w-32"></div>
    <div class="pointer-events-none absolute inset-y-0 right-0 z-10 w-16 bg-gradient-to-l from-[#00431a] to-transparent md:w-32"></div>

    <div class="marquee-track flex w-max items-center gap-4 group-hover:[animation-play-state:paused]">
      <div v-for="row in 2" :key="row" class="flex items-center gap-4" :aria-hidden="row === 2">
        <span
          v-for="(item, i) in items"
          :key="item"
          class="flex shrink-0 items-center gap-3 whitespace-nowrap rounded-full px-6 py-[10px] text-xl font-extrabold tracking-[-0.3px]"
          :class="i % 2 === 0
            ? 'bg-white/10 text-[#faf9f5]'
            : 'border border-[#a9e6b6]/30 text-[#a9e6b6] italic font-semibold'"
        >
          <span class="h-[6px] w-[6px] shrink-0 rounded-full bg-[#1faf38]"></span>
          {{ item }}
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
const items = [
  'Ayam Broiler',
  'Ayam Kampung',
  'Aneka Unggas',
  'Partingan Ayam',
  'Jasa Potong',
  'Kirim Toko',
  'Ngebelanjain',
]
</script>

<style scoped>
.marquee-track {
  animation: marquee-scroll 32s linear infinite;
}
@keyframes marquee-scroll {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50%);
  }
}
</style>