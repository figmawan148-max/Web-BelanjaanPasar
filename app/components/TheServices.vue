<template>
  <section class="relative overflow-hidden bg-[#E6F8ED] px-5 py-20 md:px-10">
    <!-- Dekorasi -->
    <div class="pointer-events-none absolute -left-20 top-10 h-[380px] w-[380px] rounded-full bg-[#1faf38]/15 blur-[130px]"></div>
    <div class="pointer-events-none absolute right-0 bottom-0 h-[320px] w-[320px] rounded-full bg-[#a9e6b6]/10 blur-[110px]"></div>

    <div class="relative mx-auto max-w-[1280px]">
      <!-- Header -->
      <div v-reveal class="mb-14 flex flex-col gap-6 md:flex-row md:items-end md:justify-between">
        <div>
          <p class="mb-3 flex items-center gap-[10px] text-base font-bold uppercase text-[#00652c]">
            <img src="/icons/vector-line.svg" alt="" class="w-[31px]" />
            Layanan Kami
          </p>
          <h2 class="max-w-[690px] font-['Plus_Jakarta_Sans'] text-3xl font-extrabold leading-[1.1] text-[#131B2E] md:text-[48px]">
            Bukan <span class="font-semibold italic text-[#00652c]">sekedar</span> belanja ayam.
          </h2>
        </div>
        <p class="max-w-[385px] text-base text-[#131B2E]/80">
          Berbagai layanan tambahan untuk membantu kebutuhan belanja pasar Anda.
        </p>
      </div>

      <!-- Grid bento -->
      <div class="grid grid-cols-1 gap-6 lg:grid-cols-2">
        <!-- Layanan 01: Jastip Belanja -->
        <div v-reveal class="group relative overflow-hidden rounded-[28px] border border-white/10">
          <img
            src="/images/service-jastip.png"
            alt="Keranjang anyaman dan aneka sayuran segar di lapak pasar"
            class="aspect-[688/574] w-full bg-[#0e2518] object-cover transition-transform duration-700 group-hover:scale-105"
          />
          <div class="absolute inset-0 bg-gradient-to-t from-[#061209] via-[#061209]/60 via-45% to-transparent to-80%"></div>
          <span class="absolute right-6 top-6 font-['Plus_Jakarta_Sans']"></span>
          <div class="absolute inset-x-0 bottom-0 p-9">
            <span class="inline-flex items-center gap-2 rounded-full border border-white/15 bg-white/10 px-[14px] py-2 text-[13px] font-bold uppercase text-white backdrop-blur-sm">
              <img src="/icons/icon-basket.svg" alt="" class="h-[14px] w-[14px] brightness-0 invert" />
              Layanan 01
            </span>
            <h3 class="mt-4 text-3xl font-extrabold text-white md:text-4xl">Ngebelanjain</h3>
            <p class="mt-3 max-w-[448px] text-base text-white/70">
              Titip belanja kebutuhan pasar lainnya bersamaan dengan pesanan ayam Anda.
            </p>
            <a
              href="#"
              class="group/btn mt-6 inline-flex h-12 items-center justify-center gap-[10px] rounded-full bg-white px-6 text-[15px] font-bold text-[#0b1f14] transition-all duration-300 hover:-translate-y-0.5 hover:bg-[#1faf38] hover:text-white hover:shadow-lg"
            >
              Jelajahi Layanan              
              <img src="/icons/icon-arrow-jastip.svg" alt="" class="h-[18px] w-[18px] transition-transform duration-300 group-hover/btn:translate-x-1" />
            </a>
          </div>
        </div>

        <!-- Layanan 02: Jasa Kirim Toko -->
        <div v-reveal="100" class="group overflow-hidden rounded-[24px] border border-white/100 shadow-[0_20px_45px_-20px_rgba(43,31,20,0.25)] transition-all duration-300 hover:-translate-y-1 hover:shadow-[0_28px_60px_-20px_rgba(43,31,20,0.35)]">
          <div class="relative overflow-hidden">
            <img
              src="/images/service-kirim-toko.png"
              alt="Kurir mengantar pesanan dengan sepeda motor"
              class="h-[260px] w-full bg-[#0e2518] object-cover transition-transform duration-700 group-hover:scale-105 md:h-[301px]"
            />
            <div class="pointer-events-none absolute inset-0 bg-gradient-to-t from-[#0b1f14] to-transparent"></div>
          </div>
          <div class="p-8">
            <p class="text-[13px] font-bold uppercase tracking-[0.8px] text-[#00652c]">Layanan 02</p>
            <h3 class="mt-2 text-2xl font-extrabold text-[#131B2E] md:text-[32px]">Jasa Kirim Toko</h3>
            <p class="mt-3 max-w-[418px] text-[15px] text-[#131B2E]/80">
              Pesanan dapat diantar dari toko ke alamat Anda sesuai area dan jadwal yang tersedia.
            </p>
            <a 
               href="#"
              class="group/btn mt-7 inline-flex h-12 w-fit items-center justify-center gap-[10px] rounded-full  px-6 text-[15px] font-bold text-[#131b2e] transition-all duration-300 hover:-translate-y-0.5 hover:bg-white hover:shadow-[0_10px_30px_-5px_rgba(31,175,56,0.5)]"
            >
              Jelajahi Layanan
              <img src="/icons/icon-arrow-potong.svg" alt="" class="h-[18px] w-[18px] brightness-0 transition-transform duration-300 group-hover/btn:translate-x-1" />
            </a>
          </div>
        </div>

        <!-- Layanan 03: Jasa Potong Unggas -->
        <div v-reveal="200" class="group flex flex-col overflow-hidden rounded-[24px] border border-white/100 shadow-[0_20px_45px_-20px_rgba(43,31,20,0.25)] transition-all duration-300 hover:-translate-y-1 hover:shadow-[0_28px_60px_-20px_rgba(43,31,20,0.35)] md:flex-row lg:col-span-2">
          <div class="relative overflow-hidden md:w-[50%]">
            <img
              src="/images/service-potong-unggas.png"
              alt="Tangan memegang ayam utuh segar di atas talenan kayu dengan pisau"
              class="h-[260px] w-full bg-[#0e2518] object-cover transition-transform duration-700 group-hover:scale-105 md:h-full"
            />
            <div class="pointer-events-none absolute inset-0 bg-gradient-to-r from-transparent to-[#0b1f14]/40 md:bg-gradient-to-t md:from-[#0b1f14]/30 md:to-transparent"></div>
          </div>
          <div class="flex flex-1 flex-col justify-center p-8 md:p-14">
            <span class="flex items-center gap-2 text-[13px] font-bold uppercase tracking-[0.8px] text-[#00652c]">
              Layanan 03
            </span>
            <h3 class="mt-4 text-2xl font-extrabold text-[#131B2E] md:text-[32px]">Jasa Potong Unggas</h3>
            <p class="mt-3 max-w-[388px] text-base text-[#131B2E]/80">
              Potongan ayam dapat disesuaikan dengan jumlah dan bagian yang Anda butuhkan.
            </p>
            <a
              href="#"
              class="group/btn mt-7 inline-flex h-12 w-fit items-center justify-center gap-[10px] rounded-full  px-6 text-[15px] font-bold text-[#131b2e] transition-all duration-300 hover:-translate-y-0.5 hover:bg-white hover:shadow-[0_10px_30px_-5px_rgba(31,175,56,0.5)]"
            >
              Jelajahi Layanan
              <img src="/icons/icon-arrow-potong.svg" alt="" class="h-[18px] w-[18px] brightness-0 transition-transform duration-300 group-hover/btn:translate-x-1" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>