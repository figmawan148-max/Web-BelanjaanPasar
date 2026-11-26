<template>
  <section class="relative overflow-hidden bg-[#E6F8ED] px-5 py-14 md:px-10">
    <div class="pointer-events-none absolute left-1/2 top-0 h-[260px] w-[500px] -translate-x-1/2 rounded-full bg-[#1faf38]/10 blur-[110px]"></div>

    <div class="relative mx-auto grid max-w-[1280px] grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-4">
      <div
        v-for="(item, i) in items"
        :key="i"
        v-reveal="i * 60"
        class="group flex items-start gap-4 rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition-all duration-300 hover:-translate-y-1 hover:border-[#1faf38]/30 hover:bg-white/[0.06]"
      >
        <span class="flex h-11 w-11 shrink-0 items-center justify-center rounded-xl bg-gradient-to-br from-[#1faf38] to-[#00652c] shadow-[0_6px_16px_-4px_rgba(31,175,56,0.4)] transition-transform duration-300 group-hover:scale-110">
          <img :src="item.icon" alt="" class="h-5 w-5 brightness-0 invert" />
        </span>
        <div>
          <h3 class="text-[15px] font-bold text-[#131B2E]">{{ item.title }}</h3>
          <p class="mt-1 text-[13.5px] text-[#131B2E]/70">{{ item.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const items = [
  { icon: '/icons/icon-trust-1.svg', title: 'Ayam Potong Segar', desc: 'Disiapkan untuk kebutuhan masak harian.' },
  { icon: '/icons/icon-trust-2.svg', title: 'Pilihan Produk', desc: 'Ayam broiler, kampung, dan aneka unggas.' },
  { icon: '/icons/icon-trust-3.svg', title: 'Layanan Fleksibel', desc: 'Potongan sesuai kebutuhan pelanggan.' },
  { icon: '/icons/icon-trust-4.svg', title: 'Praktis Memesan', desc: 'Konfirmasi langsung dengan toko.' },
]
</script>