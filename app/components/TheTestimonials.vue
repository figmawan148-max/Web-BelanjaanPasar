<template>
  <section class="bg-[#E6F8ED] px-6 py-24 md:px-14">
    <div class="mx-auto max-w-[1320px]">
      <!-- Header -->
      <div v-reveal class="flex flex-col gap-6 md:flex-row md:items-end md:justify-between">
        <div>
          <p class="flex items-center gap-4 text-[13px] font-bold uppercase tracking-[3px] text-[#1F6B3A]">
            <span class="h-px w-10 bg-[#A67C3D]"></span>
            Cerita Pelanggan
          </p>
          <h2 class="mt-6 font-['Plus_Jakarta_Sans'] text-[36px] font-semibold leading-[1.15] text-[#20160D] md:text-[48px]">
            Pengalaman pelanggan <span class="font-medium italic text-[#1F6B3A]">layak didengar.</span>
          </h2>
        </div>
        <p class="max-w-[360px] text-lg leading-relaxed text-[#6B5640]">
          Kami hanya menampilkan ulasan pelanggan yang sudah diverifikasi dan mendapat izin untuk dibagikan.
        </p>
      </div>

      <!-- Kartu testimoni -->
      <div class="mt-16 grid grid-cols-1 gap-px overflow-hidden rounded-[8px] bg-[#2B1F14]/10 md:grid-cols-3">
        <div
          v-for="(card, index) in cards"
          :key="card.letter"
          v-reveal="index * 100"
          class="group flex flex-col gap-7 bg-white p-9 transition-colors duration-300 hover:bg-white"
        >
          <div class="flex items-center justify-between">
            <span class="font-['Plus_Jakarta_Sans'] text-5xl italic leading-none text-[#1F6B3A]/25">&rdquo;</span>
            <div class="flex gap-[3px]">
              <img v-for="n in 5" :key="n" src="/icons/icon-star.svg" alt="" class="h-4 w-4" />
            </div>
          </div>

          <p class="flex-1 text-[17px] leading-relaxed text-[#2B1F14]">
            Tambahkan pengalaman pelanggan yang sudah diverifikasi dan disetujui untuk dipublikasikan.
          </p>

          <div class="flex items-center gap-4 border-t border-[#2B1F14]/10 pt-6">
            <span class="flex h-12 w-12 shrink-0 items-center justify-center rounded-full border border-[#1F6B3A]/30 font-['Fraunces'] text-xl italic text-[#1F6B3A]">
              {{ card.letter }}
            </span>
            <div>
              <p class="text-[15px] font-semibold text-[#20160D]">Pelanggan</p>
              <p class="text-[13px] uppercase tracking-[0.5px] text-[#A67C3D]">{{ card.badgeLabel }}</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Navigasi -->
      <div v-reveal="250" class="mt-10 flex items-center justify-center gap-6">
        <button type="button" class="flex h-11 w-11 items-center justify-center rounded-full border border-[#2B1F14]/20 text-[#20160D] transition-colors duration-300 hover:border-[#1F6B3A] hover:bg-white hover:text-white">
          <img src="/icons/icon-chevron.svg" alt="Sebelumnya" class="h-4 w-4" />
        </button>
        <div class="flex items-center gap-2">
          <span v-for="n in 7" :key="n" class="h-[5px] rounded-full transition-all duration-300" :class="n === 1 ? 'w-6 bg-[#1F6B3A]' : 'w-[5px] bg-[#2B1F14]/20'"></span>
        </div>
        <button type="button" class="flex h-11 w-11 items-center justify-center rounded-full border border-[#2B1F14]/20 text-[#20160D] transition-colors duration-300 hover:border-[#1F6B3A] hover:bg-white hover:text-white">
          <img src="/icons/icon-chevron.svg" alt="Selanjutnya" class="h-4 w-4 rotate-180" />
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const cards = [
  { letter: 'A', badgeLabel: 'Pelanggan VIP' },
  { letter: 'B', badgeLabel: 'Verified Purchase' },
  { letter: 'C', badgeLabel: 'Mitra Kuliner Bisnis' },
]
</script>