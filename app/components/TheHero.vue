<template>
  <section class="relative overflow-hidden bg-[#E6F8ED] px-6 py-20 md:px-14 md:py-28">
    <!-- Satu-satunya elemen dekoratif: wordmark raksasa transparan -->
    <p class="pointer-events-none absolute -right-8 -top-6 select-none whitespace-nowrap font-['Plus_Jakarta_Sans'] text-[260px] font-extrabold italic leading-none text-[#2B1F14]/[0.035] md:text-[340px]">
      Pasar
    </p>

    <div class="relative mx-auto grid max-w-[1320px] grid-cols-1 items-center gap-16 lg:grid-cols-[1fr_0.92fr] lg:gap-24">
      <!-- Kolom teks -->
      <div>
        <p v-reveal class="flex items-center gap-4 text-[13px] font-bold uppercase tracking-[3px] text-[#1F6B3A]">
          <span class="h-px w-10 bg-[#A67C3D]"></span>
          Unggas Segar Pilihan
        </p>

        <h1 v-reveal="100" class="mt-7 font-['Plus_Jakarta_Sans'] text-[42px] font-semibold leading-[1.08] tracking-[-0.5px] text-[#131b2e] md:text-[68px]">
          Ayam segar,<br />
          <span class="font-bold italic text-[#1F6B3A]">dipotong</span> sesuai<br />
          kebutuhan dapur Anda.
        </h1>

        <p v-reveal="200" class="mt-8 max-w-[480px] text-[19px] leading-relaxed text-[#6B5640]">
          Belanja ayam broiler, ayam kampung, dan aneka partingan dengan pilihan potongan sesuai
          kebutuhan. Lengkap dengan layanan jasa potong, kirim toko, dan jastip ngebelanjain.
        </p>

        <div v-reveal="300" class="mt-10 flex flex-wrap items-center gap-8">
          <a
            href="#"
            class="flex items-center gap-3 rounded-full bg-[#1F6B3A] px-8 py-[18px] text-[16px] font-bold text-white shadow-[0_16px_32px_-14px_rgba(31,107,58,0.6)] transition-all duration-300 hover:-translate-y-0.5 hover:bg-[#164F2B]"
          >
            <img src="/icons/icon-download.svg" alt="" class="h-5 w-5 brightness-0 invert" />
            Pesan melalui aplikasi
          </a>
          <a href="#produk" class="group flex items-center gap-2 text-[16px] font-bold text-[#20160D]">
            Jelajahi Produk
            <span class="relative overflow-hidden">
              <span class="block transition-transform duration-300 group-hover:translate-x-1">&rarr;</span>
            </span>
            <span class="absolute mt-6 h-px w-0 bg-[#20160D] transition-all duration-300 group-hover:w-[120px]"></span>
          </a>
        </div>

        <div v-reveal="350" class="mt-12 flex items-center gap-4 border-t border-[#2B1F14]/10 pt-6 text-[14px] text-[#6B5640]">
          <img src="/icons/icon-info.svg" alt="" class="h-4 w-4 opacity-60" />
          Pesanan langsung dengan toko &middot; stok dan harga dikonfirmasi sebelum transaksi
        </div>
      </div>

      <!-- Kolom foto -->
      <div v-reveal="150" class="relative mx-auto w-full max-w-[460px] lg:mx-0">
        <div class="relative overflow-hidden rounded-[4px] shadow-[0_50px_80px_-30px_rgba(43,31,20,0.4)]">
          <div class="pointer-events-none absolute inset-3 z-10 rounded-[2px] border border-white/70"></div>
          <img
            src="/images/hero-ayam-utuh.png"
            alt="Ayam segar utuh di atas talenan kayu bersama bumbu dapur"
            class="block aspect-[819/1020] w-full object-cover"
          />
        </div>

        <!-- Satu-satunya elemen glass: kartu label mengambang -->
        <div class="absolute -left-10 bottom-16 flex items-center gap-4 rounded-sm border border-white/60 bg-white/85 py-5 pl-5 pr-7 shadow-[0_30px_60px_-20px_rgba(43,31,20,0.35)] backdrop-blur-xl md:-left-16">
          <span class="font-['Plus_Jakarta_Sans'] text-3xl italic text-[#1F6B3A]">01</span>
          <span class="h-10 w-px bg-[#2B1F14]/15"></span>
          <span class="flex flex-col">
            <strong class="text-[15px] font-semibold text-[#20160D]">Utuh &amp; Partingan</strong>
            <small class="mt-1 text-[13px] text-[#6B5640]">Dada &middot; Paha &middot; Sayap</small>
          </span>
        </div>

        <div class="absolute -right-6 -top-6 w-[42%] overflow-hidden rounded-[2px] border-4 border-[#E6F8ED] shadow-[0_30px_60px_-20px_rgba(43,31,20,0.35)]">
          <img
            src="/images/hero-dada-ayam.png"
            alt="Dada ayam segar di atas talenan kayu dengan lemon"
            class="aspect-[295/221] w-full object-cover"
          />
        </div>
      </div>
    </div>
  </section>
</template>