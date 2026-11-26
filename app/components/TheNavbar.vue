<template>
  <header class="sticky top-4 z-50 w-full px-4 md:top-5 md:px-8">
    <div class="mx-auto flex h-[64px] max-w-[1200px] items-center justify-between rounded-full border border-white/60 bg-white/80 px-5 shadow-[0_8px_30px_-10px_rgba(19,27,46,0.15)] backdrop-blur-xl md:px-6">
      <a href="/" class="group flex items-center gap-[8px]" aria-label="Belanjaan Pasar, ke awal halaman">
        <span class="flex h-9 w-9 items-center justify-center rounded-full from-[#E6F8ED] transition-transform duration-300 group-hover:scale-110">
          <img src="/icons/logo.svg" alt="" class="h-5 w-6" />
        </span>
        <span class="font-['Nunito'] text-[16px] font-extrabold text-[#131b2e]">Belanjaan Pasar</span>
      </a>

      <nav class="hidden items-center gap-1 lg:flex">
        <a
          v-for="link in links"
          :key="link.label"
          :href="link.href"
          class="group relative rounded-full px-4 py-2 text-[14px] font-semibold text-[#131b2e]/75 transition-colors duration-200 hover:text-[#131b2e]"
        >
          {{ link.label }}
          <span class="absolute bottom-1 left-4 right-4 h-[2px] origin-left scale-x-0 rounded-full bg-[#1faf38] transition-transform duration-300 group-hover:scale-x-100"></span>
        </a>
      </nav>

      <a
        href="#"
        class="group flex items-center gap-2 whitespace-nowrap rounded-full bg-gradient-to-r from-[#137a32] to-[#00652c] px-5 py-[10px] text-[13.5px] font-bold text-white shadow-[0_8px_20px_-6px_rgba(19,122,50,0.5)] transition-all duration-300 hover:-translate-y-0.5 hover:shadow-[0_10px_25px_-6px_rgba(19,122,50,0.6)]"
      >
        <img src="/icons/icon-download.svg" alt="" class="h-[18px] w-[18px] brightness-0 invert" />
        <span class="hidden sm:inline">Download Aplikasi Segera</span>
        <span class="sm:hidden">Download</span>
      </a>
    </div>
  </header>
</template>

<script setup>
const links = [
  { label: 'Produk', href: '#produk' },
  { label: 'Keunggulan', href: '#keunggulan' },
  { label: 'Layanan', href: '#layanan' },
  { label: 'Cara Pesan', href: '#cara-pesan' },
  { label: 'Tentang Kami', href: '#tentang-kami' },
  { label: 'Lokasi & Kontak', href: '#kontak' },
]
</script>