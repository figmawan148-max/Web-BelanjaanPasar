<template>
  <section class="relative overflow-hidden bg-[#E6F8ED] px-5 py-20 md:px-10">
    <!-- Dekorasi -->
    <div class="pointer-events-none absolute left-1/2 top-0 h-[380px] w-[600px] -translate-x-1/2 rounded-full bg-[#1faf38]/15 blur-[130px]"></div>

    <div class="relative mx-auto max-w-[1280px]">
      <!-- Header -->
      <div v-reveal class="flex flex-col items-center text-center">
       <p class="mb-3 flex w-fit items-center gap-[10px] rounded-full border border-[#1faf38]/25 bg-[#1faf38]/10 px-4 py-[6px] text-sm font-bold uppercase tracking-[0.5px] text-[#131B2E]">
          <span class="h-[6px] w-[6px] rounded-full bg-[#131B2E]"></span>
          Promo Aktif
        </p>
        <h2 class="font-['Plus_Jakarta_Sans'] text-3xl font-extrabold leading-[1.1] text-[#131B2E] md:text-[48px]">
          Pantau promo dan<br />
          <span class="font-semibold italic text-[#00652c]">penawaran terbaru.</span>
        </h2>
        <p class="mt-3 max-w-[480px] text-base text-[#131B2E]/60">
          Temukan informasi penawaran produk dan layanan yang sedang aktif, lengkap dengan periode serta ketentuannya.
        </p>
      </div>

      <!-- Kartu kupon -->
      <div v-reveal="150" class="relative mt-12 flex flex-col overflow-hidden rounded-[28px] border border-[#131B2E]/20 bg-gradient-to-br from-[#123d21] to-[#071a10] md:h-[460px] md:flex-row">
        <!-- Notch kiri & kanan (gaya lubang kupon) -->
        <span class="absolute left-[42%] top-0 z-10 hidden h-7 w-7 -translate-y-1/2 rounded-full bg-[#0b1f14] md:block"></span>
        <span class="absolute left-[42%] bottom-0 z-10 hidden h-7 w-7 translate-y-1/2 rounded-full bg-[#0b1f14] md:block"></span>

        <!-- Kiri: info -->
        <div class="flex flex-1 flex-col justify-center px-8 py-10 md:px-12 md:py-0">
          <p class="flex items-center gap-3 text-base font-bold uppercase text-[#a9e6b6]">
            <img src="/icons/vector-line.svg" alt="" class="w-[31px]" />
            Penawaran Terbaru
          </p>
          <h3 class="mt-5 text-3xl font-extrabold leading-[1.15] text-white md:text-[44px]">
            Penawaran untuk<br />
            <span class="font-semibold italic text-[#a9e6b6]">kebutuhan dapur.</span>
          </h3>
          <p class="mt-3 text-base text-white/100">
            Pantau promo aktif sesuai periode dan ketersediaan produk di toko.
          </p>
          <a
            href="#produk"
            class="group mt-6 inline-flex w-fit items-center gap-[10px] rounded-full bg-[#1faf38] px-6 py-[13px] text-[15px] font-bold text-[#0b1f14] transition-all duration-300 hover:-translate-y-0.5 hover:bg-white hover:shadow-[0_10px_30px_-5px_rgba(31,175,56,0.5)]"
          >
            Jelajahi Produk
            <img src="/icons/icon-arrow-right-green.svg" alt="" class="h-[18px] w-[18px] brightness-0 transition-transform duration-300 group-hover:translate-x-1" />
          </a>
          <p class="mt-7 text-xs text-white/100">
            Syarat, periode, dan harga akhir akan dicantumkan pada promo yang sedang berlaku.
          </p>
        </div>

        <!-- Garis putus-putus pemisah -->
        <div class="relative hidden w-px md:block">
          <div class="absolute inset-y-6 left-0 border-l-2 border-dashed border-white/15"></div>
        </div>
        <div class="mx-8 block h-px border-t-2 border-dashed border-white/15 md:hidden"></div>

        <!-- Kanan: foto -->
        <div class="group relative flex-1 overflow-hidden p-4 md:p-6">
          <div class="relative h-full w-full overflow-hidden rounded-[20px]">
            <img
              src="/images/promo-ayam-broiler.png"
              alt="Ayam broiler segar di atas talenan kayu dengan rempah"
              class="h-[220px] w-full object-cover object-center transition-transform duration-700 group-hover:scale-105 md:h-full"
            />
            <div class="pointer-events-none absolute inset-0 bg-gradient-to-t from-[#0b1f14]/40 to-transparent"></div>
          </div>

          <span class="absolute right-9 top-9 rounded-full bg-white/95 px-4 py-2 text-[13px] font-extrabold text-[#0b1f14] shadow-lg">
            Harga Pasar Hari Ini
          </span>
        </div>
      </div>
    </div>
  </section>
</template>