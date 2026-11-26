<template>
  <section class="relative overflow-hidden bg-[#0b1f14] px-5 py-20 md:px-10">
    <!-- Dekorasi -->
    <div class="pointer-events-none absolute -right-24 -top-24 h-[420px] w-[420px] rounded-full bg-[#1faf38]/15 blur-[130px]"></div>
    <div class="pointer-events-none absolute -left-16 bottom-0 h-[320px] w-[320px] rounded-full bg-[#a9e6b6]/10 blur-[110px]"></div>
    <div class="pointer-events-none absolute inset-0 bg-[radial-gradient(circle_at_1px_1px,rgba(255,255,255,0.05)_1px,transparent_0)] [background-size:26px_26px]"></div>

    <div class="relative mx-auto grid max-w-[1280px] grid-cols-1 items-center gap-12 lg:grid-cols-[0.82fr_1fr] lg:gap-x-[100px]">
      <!-- Foto + tag -->
      <div v-reveal class="relative mx-auto w-full max-w-[460px] lg:mx-0">
        <div class="relative overflow-hidden rounded-[28px] border border-white/10 bg-gradient-to-br from-[#1faf38] to-[#00431a] p-[3px]">
          <div class="group overflow-hidden rounded-[25px]">
            <img
              src="/images/feature-penjual-pasar.png"
              alt="Penjual melayani pembeli di lapak pasar dengan timbangan"
              class="aspect-[477/871] w-full bg-[#f2ece2] object-cover transition-transform duration-700 group-hover:scale-105"
            />
          </div>
        </div>

        <div class="absolute bottom-[8%] left-1/2 w-[85%] max-w-[300px] -translate-x-1/2 rounded-2xl border border-white/10 bg-[#0e2518]/95 p-5 shadow-[0_20px_50px_-15px_rgba(0,0,0,0.5)] backdrop-blur-md transition-transform duration-500 hover:-translate-y-1 md:left-[48%]">
          <p class="flex items-center gap-2 text-xs font-bold uppercase tracking-[1.5px] text-[#a9e6b6]">
            <span class="h-[6px] w-[6px] animate-pulse rounded-full bg-[#1faf38]"></span>
            Tanpa Ribet
          </p>
          <p class="mt-3 max-w-[250px] text-[15px] font-semibold text-white">
            Tanpa registrasi dan checkout rumit. Cukup kirim kebutuhan Anda lewat WhatsApp.
          </p>
        </div>
      </div>

      <!-- Teks + daftar bernomor -->
      <div>
        <p v-reveal class="mb-3 flex items-center gap-3 text-base font-bold uppercase text-[#a9e6b6]">
          <img src="/icons/vector-line.svg" alt="" class="w-[31px]" />
          Keunggulan Kami
        </p>
        <h2 v-reveal="100" class="font-['Plus_Jakarta_Sans'] text-3xl font-extrabold leading-[1.15] text-white md:text-[48px]">
          Belanja lebih mudah,<br />
          kebutuhan dapur<br />
          <span class="font-semibold italic text-[#a9e6b6]">kebutuhan lebih terarah.</span>
        </h2>

        <div class="mt-12 grid grid-cols-1 gap-4 sm:grid-cols-2">
          <div
            v-for="(item, index) in items"
            :key="item.number"
            v-reveal="index * 80"
            class="group rounded-2xl border border-white/10 bg-white/[0.04] p-6 transition-all duration-300 hover:-translate-y-1 hover:border-[#1faf38]/30 hover:bg-white/[0.08]"
          >
            <span class="flex h-11 w-11 items-center justify-center rounded-xl bg-white/[0.06] text-base font-extrabold text-[#a9e6b6] transition-colors duration-300 group-hover:bg-[#1faf38] group-hover:text-[#0b1f14]">
              {{ item.number }}
            </span>
            <h3 class="mt-4 text-lg font-extrabold text-white">{{ item.title }}</h3>
            <p class="mt-2 text-sm text-white/55">{{ item.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const items = [
  { number: '01', title: 'Fokus pada Kesegaran', desc: 'Produk disiapkan untuk memenuhi kebutuhan belanja harian Anda.' },
  { number: '02', title: 'Pilihan Sesuai Kebutuhan', desc: 'Mulai dari ayam utuh hingga potongan bagian tertentu.' },
  { number: '03', title: 'Untuk Rumah dan Usaha', desc: 'Mendukung kebutuhan rumah tangga maupun bisnis kuliner.' },
  { number: '04', title: 'Layanan Lebih Praktis', desc: 'Lengkap dengan jasa potong, pengiriman toko, dan jastip belanja.' },
]
</script>