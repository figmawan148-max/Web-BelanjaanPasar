<template>
  <section class="relative overflow-hidden bg-[#0b1f14] px-5 py-20 md:px-10">
    <!-- Dekorasi -->
    <div class="pointer-events-none absolute -left-24 top-20 h-[400px] w-[400px] rounded-full bg-[#1faf38]/15 blur-[130px]"></div>
    <div class="pointer-events-none absolute right-0 bottom-10 h-[300px] w-[300px] rounded-full bg-[#a9e6b6]/10 blur-[110px]"></div>

    <div class="relative mx-auto grid max-w-[1280px] grid-cols-1 items-center gap-16 lg:grid-cols-[0.95fr_1fr]">
      <!-- Teks -->
      <div>
        <p v-reveal class="mb-3 flex items-center gap-3 text-base font-bold uppercase text-[#a9e6b6]">
          <img src="/icons/vector-line.svg" alt="" class="w-[31px]" />
          Dari Surya Mandiri Sejahtera
        </p>

        <h2 v-reveal="100" class="max-w-[480px] font-['Plus_Jakarta_Sans'] text-3xl font-extrabold leading-[1.15] text-white md:text-[52px]">
          Kenali <span class="font-semibold italic text-[#a9e6b6]">Belanjaan Pasar</span> lebih dekat.
        </h2>

        <p v-reveal="200" class="mt-8 max-w-[477px] text-lg font-medium text-white/80">
          Belanjaan Pasar adalah wajah digital baru Surya Mandiri Sejahtera, penyedia ayam potong
          segar dan aneka partingan unggas untuk kebutuhan rumah tangga maupun pelaku usaha.
        </p>

        <div v-reveal="250" class="relative mt-6 max-w-[477px] overflow-hidden rounded-2xl border border-white/10 bg-white/[0.04] p-5">
          <span class="pointer-events-none absolute -left-1 -top-3 font-['Plus_Jakarta_Sans'] text-[64px] font-extrabold leading-none text-[#1faf38]/15">&ldquo;</span>
          <p class="relative text-[15px] leading-relaxed text-white/70">
            Selain produk unggas, pelanggan dapat memanfaatkan Ngebelanjain untuk titip belanja
            kebutuhan pasar, serta layanan jasa kirim toko dan potong unggas.
          </p>
        </div>

        <div v-reveal="300" class="mt-12 max-w-[477px]">
          <p class="flex items-center gap-2 text-xs font-bold uppercase tracking-[1.2px] text-white/50">
            <span class="h-[3px] w-4 rounded-full bg-[#a9e6b6]"></span>
            Kami Melayani
          </p>
          <div class="mt-4 flex flex-wrap gap-3">
            <span
              v-for="item in services"
              :key="item"
              class="group flex items-center gap-2 rounded-full border border-white/10 bg-white/[0.04] px-4 py-[10px] text-[14px] font-semibold text-white/85 transition-all duration-300 hover:-translate-y-0.5 hover:border-[#1faf38]/50 hover:bg-[#1faf38]/10"
            >
              <span class="h-[6px] w-[6px] rounded-full bg-[#1faf38] transition-transform duration-300 group-hover:scale-150"></span>
              {{ item }}
            </span>
          </div>
        </div>
      </div>

      <!-- Foto collage -->
      <div v-reveal="150" class="relative mx-auto w-full max-w-[560px] lg:pl-8">
        <div class="group relative overflow-hidden rounded-[28px] border border-white/10 bg-white/[0.04] p-2">
          <div class="overflow-hidden rounded-[22px]">
            <img
              src="/images/about-suasana-pasar.png"
              alt="Suasana pasar tradisional dengan para pembeli berbelanja"
              class="aspect-[651/505] w-full object-cover transition-transform duration-700 group-hover:scale-105"
            />
          </div>
          <span class="absolute right-5 top-5 rounded-full bg-[#0b1f14]/70 px-3 py-[6px] text-[10.5px] font-semibold text-white backdrop-blur-sm">
            Foto ilustrasi
          </span>
        </div>

        <div class="absolute bottom-[-10%] right-[2%] w-[42%] overflow-hidden rounded-2xl border-[3px] border-[#0b1f14] bg-gradient-to-br from-[#1faf38] to-[#00431a] p-[3px] shadow-[0_20px_50px_-15px_rgba(0,0,0,0.6)] transition-transform duration-500 hover:-translate-y-1">
          <img
            src="/images/about-penjual-pasar.png"
            alt="Penjual di lapak pasar tradisional saat matahari terbit"
            class="aspect-[236/174] w-full rounded-[14px] object-cover"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = ['Rumah tangga', 'Usaha makanan kecil', 'Restoran & kuliner', 'Katering']
</script>