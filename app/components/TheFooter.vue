<template>
  <footer class="relative overflow-hidden bg-[#071a10] px-5 pt-24 md:px-10">
    <!-- Dekorasi blur warna-warni -->
    <div class="pointer-events-none absolute left-[-10%] top-0 h-[420px] w-[420px] rounded-full bg-[#1faf38]/25 blur-[120px]"></div>
    <div class="pointer-events-none absolute right-[-5%] top-[30%] h-[360px] w-[360px] rounded-full bg-[#a9e6b6]/15 blur-[110px]"></div>
    <div class="pointer-events-none absolute inset-0 bg-[radial-gradient(circle_at_1px_1px,rgba(255,255,255,0.07)_1px,transparent_0)] [background-size:28px_28px]"></div>

    <div class="relative mx-auto max-w-[1280px]">
      <!-- CTA besar -->
      <div v-reveal class="relative overflow-hidden rounded-[32px] border border-white/10 bg-gradient-to-br from-[#137a32] to-[#00431a] p-10 md:p-16">
        <div class="pointer-events-none absolute -right-16 -top-16 h-56 w-56 rounded-full bg-white/10 blur-3xl"></div>
        <p class="flex items-center gap-2 text-xs font-bold uppercase tracking-[2px] text-[#a9e6b6]">
          <span class="h-[6px] w-[6px] animate-pulse rounded-full bg-[#a9e6b6]"></span>
          Siap Belanja?
        </p>
        <h3 class="mt-4 max-w-[640px] text-3xl font-extrabold leading-[1.1] text-white md:text-4xl">
          Pesan ayam segar <span class="font-semibold italic text-[#a9e6b6]">hari ini juga.</span>
        </h3>
        <div class="mt-8 flex flex-col items-start gap-4 sm:flex-row sm:items-center">
          <a
            href="#"
            class="group inline-flex h-14 items-center rounded-full bg-white px-7 text-[15px] font-bold text-[#131b2e] transition-all duration-300 hover:-translate-y-0.5 hover:bg-[#a9e6b6] hover:shadow-[0_10px_30px_-5px_rgba(169,230,182,0.5)]"
          >
            <span class="flex max-w-0 items-center gap-0 overflow-hidden opacity-0 transition-all duration-300 ease-out group-hover:mr-[10px] group-hover:max-w-[24px] group-hover:gap-[10px] group-hover:opacity-100">
              <img src="/icons/icon-download.svg" alt="" class="h-5 w-5 shrink-0" />
            </span>
            Segera Hadir
          </a>
          <p class="text-sm text-[#faf9f5]/60">Stok dan harga dikonfirmasi langsung oleh toko.</p>
        </div>
      </div>

      <!-- Kolom konten: kartu kaca -->
      <div v-reveal class="mt-14 grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-5">
        <!-- Logo & deskripsi -->
        <div class="rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition-colors duration-300 hover:bg-white/[0.06] lg:col-span-2">
          <a href="/" class="group flex items-center gap-[5px]">
            <span class="flex items-center rounded-full px-4 py-[10px] transition-transform duration-300 group-hover:scale-105">
              <img src="/icons/logo.svg" alt="" class="h-9 w-[46px] object-contain" />
            </span>
            <span class="font-['Nunito'] text-2xl font-extrabold text-white">Belanjaan Pasar</span>
          </a>
          <p class="mt-5 max-w-[300px] text-[14.5px] leading-relaxed text-white/60">
            Wajah digital Surya Mandiri Sejahtera. Dari ayam segar hingga kebutuhan pasar.
          </p>
        </div>

        <!-- Navigasi -->
        <div class="rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition-colors duration-300 hover:bg-white/[0.06]">
          <h3 class="text-xs font-extrabold uppercase tracking-[1.2px] text-[#a9e6b6]">Navigasi</h3>
          <ul class="mt-4 flex flex-col gap-1">
            <li v-for="item in navLinks" :key="item">
              <a href="#" class="group relative inline-block py-[7px] text-[14px] text-white/70 transition-colors duration-200 hover:text-white">
                {{ item }}
                <span class="absolute bottom-[5px] left-0 h-px w-0 bg-[#a9e6b6] transition-all duration-300 group-hover:w-full"></span>
              </a>
            </li>
          </ul>
        </div>

        <!-- Produk & Layanan digabung satu kartu -->
        <div class="rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition-colors duration-300 hover:bg-white/[0.06]">
          <h3 class="text-xs font-extrabold uppercase tracking-[1.2px] text-[#a9e6b6]">Produk</h3>
          <ul class="mt-4 flex flex-col gap-1">
            <li v-for="item in productLinks" :key="item">
              <a href="#" class="group relative inline-block py-[7px] text-[14px] text-white/70 transition-colors duration-200 hover:text-white">
                {{ item }}
                <span class="absolute bottom-[5px] left-0 h-px w-0 bg-[#a9e6b6] transition-all duration-300 group-hover:w-full"></span>
              </a>
            </li>
          </ul>

          <h3 class="mt-6 text-xs font-extrabold uppercase tracking-[1.2px] text-[#a9e6b6]">Layanan</h3>
          <ul class="mt-4 flex flex-col gap-1">
            <li v-for="item in serviceLinks" :key="item">
              <a href="#" class="group relative inline-block py-[7px] text-[14px] text-white/70 transition-colors duration-200 hover:text-white">
                {{ item }}
                <span class="absolute bottom-[5px] left-0 h-px w-0 bg-[#a9e6b6] transition-all duration-300 group-hover:w-full"></span>
              </a>
            </li>
          </ul>
        </div>

        <!-- Kontak & Lokasi -->
        <div class="rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition-colors duration-300 hover:bg-white/[0.06]">
          <h3 class="text-xs font-extrabold uppercase tracking-[1.2px] text-[#a9e6b6]">Kontak &amp; Lokasi</h3>
          <div class="mt-4 flex flex-col gap-3 text-[13px] leading-relaxed text-white/60">
            <p>admin@</p>
            <p>WA: 0813 10 11 12 74<br />Telepon: 0858 10 11 12 74</p>
            <p>Pasar Alfa Indah, Jl. Palem V, Petukangan Utara, Pesanggrahan, Jakarta Selatan 12660.</p>
            <p>Jam kios: Setiap hari, 06.00&ndash;10.00 WIB</p>
          </div>
        </div>
      </div>

      <!-- Copyright -->
      <div class="flex flex-col items-start gap-3 py-7 text-[13px] text-white/50 sm:flex-row sm:items-center sm:justify-between">
        <p>&copy; 2026 Belanjaan Pasar. Hak cipta dilindungi.</p>
        <p>Dari Surya Mandiri Sejahtera</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const navLinks = ['Produk', 'Keunggulan', 'Layanan', 'Cara Pesan', 'Promo & Penawaran', 'Tentang Kami', 'Cerita Pelanggan', 'Lokasi & Kontak']
const productLinks = ['Ayam Broiler', 'Ayam Kampung & Unggas', 'Partingan Ayam']
const serviceLinks = ['Ngebelanjain', 'Jasa Kirim Toko', 'Jasa Potong Unggas']
</script>

<style scoped>
.footer-marquee-track {
  animation: footer-marquee 25s linear infinite;
}
@keyframes footer-marquee {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50%);
  }
}
</style>