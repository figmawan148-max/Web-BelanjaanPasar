<template>
  <section class="relative overflow-hidden bg-[#E6F8ED] px-5 py-20 md:px-10">
    <!-- Dekorasi -->
    <div class="pointer-events-none absolute -right-24 top-20 h-[380px] w-[380px] rounded-full bg-[#1faf38]/15 blur-[130px]"></div>
    <div class="pointer-events-none absolute -left-16 bottom-0 h-[300px] w-[300px] rounded-full bg-[#a9e6b6]/10 blur-[110px]"></div>

    <div class="relative mx-auto max-w-[1280px]">
      <!-- Header -->
      <div v-reveal class="mb-12 flex flex-col gap-8 md:flex-row md:items-end md:justify-between">
        <div>
          <p class="mb-3 flex w-fit items-center gap-[10px] rounded-full border border-[#1faf38]/25 bg-[#1faf38]/10 px-4 py-[6px] text-sm font-bold uppercase tracking-[0.5px] text-[#131B2E]">
            <span class="h-[6px] w-[6px] rounded-full bg-[#131B2E]"></span>
            Pilihan Produk
          </p>
          <h2 class="max-w-[690px] font-['Plus_Jakarta_Sans'] text-3xl font-extrabold leading-[1.1] tracking-[-1px] text-[#131B2E] md:text-[48px]">
            Temukan pilihan unggas untuk
            <span class="font-semibold italic text-[#1F6B3A]">kebutuhan</span>
            Anda.
          </h2>
        </div>

        <div class="flex flex-col gap-[25px] md:max-w-[380px]">
          <p class="text-base text-[#131B2E]/100">
            Mulai dari ayam utuh hingga potongan favorit, pilih produk yang sesuai dengan kebutuhan dapur Anda.
          </p>
          <p class="rounded-xl border-l-[3px] border-[#1faf38] bg-white/[0.04] py-3 pl-4 text-[14px] text-[#131B2E]/80">
            Harga mengikuti kondisi pasar harian dan dikonfirmasi langsung oleh toko.
          </p>
        </div>
      </div>

      <!-- Grid -->
      <div class="grid grid-cols-1 gap-6 lg:grid-cols-[1.45fr_1fr]">
        <!-- Kartu besar: Ayam Broiler -->
        <div v-reveal class="group overflow-hidden rounded-[24px] border border-white/10 bg-white/[0.04] transition-all duration-400 hover:-translate-y-1 hover:border-[#1faf38]/30 hover:bg-white/[0.06]">
          <div class="relative h-[300px] overflow-hidden bg-[#0e2518] md:h-[440px]">
            <img
              src="/images/product-ayam-broiler.png"
              alt="Ayam broiler utuh segar di atas talenan kayu"
              class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-105"
            />
            <div class="pointer-events-none absolute inset-0 bg-gradient-to-t from-[#0b1f14]/50 to-transparent"></div>
            <span class="absolute left-5 top-5 rounded-full bg-white/90 px-4 py-2 text-[11px] font-bold uppercase tracking-[1.2px] text-[#00652c] backdrop-blur-sm">
              Ayam Negeri
            </span>
            <span class="absolute right-5 top-5 flex h-11 w-11 items-center justify-center rounded-2xl bg-gradient-to-br from-[#131B2E] to-[#00652c] text-base font-extrabold text-white shadow-lg">
              01
            </span>
          </div>
          <div class="px-6 pb-3 pt-8 md:px-10">
            <h3 class="text-2xl font-extrabold text-[#131B2E] md:text-[32px]">Ayam Broiler</h3>
            <p class="mt-3 max-w-[448px] text-base text-[#131B2E]/80">
              Ayam potong segar utuh untuk kebutuhan memasak keluarga maupun stok usaha kuliner.
            </p>
          </div>
          <div class="px-6 md:px-10">
            <div class="flex h-16 items-center justify-between border-t border-white/10">
              <span class="text-[15px] font-bold text-[#00652c]">Tanya Ayam Broiler</span>
              <span class="flex h-10 w-10 items-center justify-center rounded-full bg-white/[0.06] transition-all duration-300 group-hover:bg-[#1faf38]">
                <img
                  src="/icons/icon-whatsapp-arrow.svg"
                  alt=""
                  class="h-[18px] w-[18px] brightness-0 invert transition-all duration-300 group-hover:translate-x-0.5 group-hover:-translate-y-0.5 group-hover:invert-0"
                />
              </span>
            </div>
          </div>
        </div>

        <!-- Kolom kanan: 2 kartu kecil -->
        <div class="flex flex-col gap-6">
          <!-- Ayam Kampung -->
          <div v-reveal="100" class="group flex overflow-hidden rounded-[24px] border border-white/10 bg-white/[0.04] transition-all duration-400 hover:-translate-y-1 hover:border-[#1faf38]/30 hover:bg-white/[0.06]">
            <div class="relative w-[35%] shrink-0 overflow-hidden bg-[#0e2518]">
              <img
                src="/images/product-ayam-kampung.png"
                alt="Ayam kampung berbulu cokelat"
                class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-105"
              />
              <span class="absolute left-2 top-2 flex h-7 w-7 items-center justify-center rounded-lg bg-gradient-to-br from-[#131B2E] to-[#00652c] text-[11px] font-extrabold text-white">
                02
              </span>
            </div>
            <div class="flex flex-1 flex-col px-6 pt-6">
              <span class="w-fit rounded-full bg-white/[0.06] px-3 py-1 text-[9px] font-bold uppercase tracking-[1px] text-[#131B2E]">Aneka Unggas</span>
              <h3 class="mt-3 text-xl font-extrabold text-[#131B2E]">Ayam Kampung &amp; Unggas Lainnya</h3>
              <p class="mt-1 pb-5 text-sm text-[#131B2E]/80">
                Pilihan ayam kampung dan aneka unggas sesuai ketersediaan di toko.
              </p>
              <div class="mt-auto flex items-center justify-between border-t border-white/10 py-4">
                <span class="text-[15px] font-bold text-[#00652c]">Tanya Ketersediaan</span>
                <span class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-white/[0.06] transition-all duration-300 group-hover:bg-[#1faf38]">
                  <img
                    src="/icons/icon-whatsapp-arrow.svg"
                    alt=""
                    class="h-[18px] w-[18px] brightness-0 invert transition-all duration-300 group-hover:translate-x-0.5 group-hover:-translate-y-0.5 group-hover:invert-0"
                  />
                </span>
              </div>
            </div>
          </div>

          <!-- Partingan Ayam -->
          <div v-reveal="200" class="group flex overflow-hidden rounded-[24px] border border-white/10 bg-white/[0.04] transition-all duration-400 hover:-translate-y-1 hover:border-[#1faf38]/30 hover:bg-white/[0.06]">
            <div class="relative w-[35%] shrink-0 overflow-hidden bg-[#0e2518]">
              <img
                src="/images/product-partingan.png"
                alt="Potongan ayam segar tertata di atas talenan kayu"
                class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-105"
              />
              <span class="absolute left-2 top-2 flex h-7 w-7 items-center justify-center rounded-lg bg-gradient-to-br from-[#131B2E] to-[#00652c] text-[11px] font-extrabold text-white">
                03
              </span>
            </div>
            <div class="flex flex-1 flex-col px-6 pt-6">
              <span class="w-fit rounded-full bg-white/[0.06] px-3 py-1 text-[9px] font-bold uppercase tracking-[1px] text-[#131B2E]">Bagian Pilihan</span>
              <h3 class="mt-3 text-xl font-extrabold text-[#131B2E]">Partingan Ayam</h3>
              <p class="mt-1 text-sm text-[#131B2E]/80">
                Berbagai bagian ayam agar Anda dapat memilih sesuai menu dan kebutuhan memasak.
              </p>
              <div class="flex flex-wrap gap-2 py-4">
                <span
                  v-for="part in ['Dada', 'Paha', 'Sayap', 'Bagian lain']"
                  :key="part"
                  class="rounded-full border border-[#131B2E]/25 px-3 py-1 text-xs font-semibold text-[#131B2E]"
                >
                  {{ part }}
                </span>
              </div>
              <div class="mt-auto flex items-center justify-between border-t border-white/10 py-4">
                <span class="text-[15px] font-bold text-[#00652c]">Tanya Partingan</span>
                <span class="flex h-10 w-10 shrink-0 items-center justify-center rounded-full bg-white/[0.06] transition-all duration-300 group-hover:bg-[#1faf38]">
                  <img
                    src="/icons/icon-whatsapp-arrow.svg"
                    alt=""
                    class="h-[18px] w-[18px] brightness-0 invert transition-all duration-300 group-hover:translate-x-0.5 group-hover:-translate-y-0.5 group-hover:invert-0"
                  />
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>