<template>
  <section class="relative overflow-hidden bg-[#0b1f14] px-5 py-20 md:px-10">
    <!-- Dekorasi -->
    <div class="pointer-events-none absolute -right-20 top-0 h-[380px] w-[380px] rounded-full bg-[#1faf38]/15 blur-[130px]"></div>

    <div class="relative mx-auto max-w-[1280px]">
      <!-- Header -->
      <p v-reveal class="mb-3 flex items-center gap-[10px] text-base font-bold uppercase text-[#a9e6b6]">
        <img src="/icons/vector-line.svg" alt="" class="w-[31px]" />
        Pesan Ayam &amp; Unggas
      </p>
      <h2 v-reveal="100" class="font-['Plus_Jakarta_Sans'] text-3xl font-extrabold leading-[1.1] text-white md:text-[48px]">
        Pilih cara belanja <span class="font-semibold italic text-[#a9e6b6]">sesuai kebutuhan.</span>
      </h2>

      <!-- Timeline langkah 1-4 -->
      <div class="relative mt-16">
        <div class="absolute left-0 right-0 top-[27px] hidden h-px bg-white/10 lg:block"></div>
        <div class="grid grid-cols-1 gap-10 sm:grid-cols-2 lg:grid-cols-4">
          <div
            v-for="(step, index) in steps"
            :key="step.number"
            v-reveal="index * 80"
            class="group relative"
          >
            <span class="relative z-10 flex h-14 w-14 items-center justify-center rounded-2xl border border-white/10 bg-[#132e1e] text-lg font-extrabold text-[#a9e6b6] transition-all duration-300 group-hover:border-[#1faf38]/50 group-hover:bg-[#1faf38] group-hover:text-[#0b1f14]">
              {{ step.number }}
            </span>
            <p class="mt-6 text-xs font-bold uppercase tracking-[0.8px] text-[#a9e6b6]/70">Langkah {{ step.number }}</p>
            <h3 class="mt-2 text-xl font-extrabold text-white">{{ step.title }}</h3>
            <p class="mt-2 text-[15px] text-white/55">{{ step.desc }}</p>
          </div>
        </div>
      </div>

      <!-- Jastip belanja pasar -->
      <div class="mt-20 grid grid-cols-1 gap-12 border-t border-white/10 pt-16 lg:grid-cols-2 lg:items-center">
        <div v-reveal>
          <h3 class="max-w-[480px] text-2xl font-extrabold text-white md:text-[32px]">
            Butuh sayur, bumbu, atau kebutuhan pasar lain?
          </h3>

          <div class="mt-8 flex flex-col gap-5">
            <div
              v-for="item in jastipSteps"
              :key="item.number"
              class="flex gap-4 rounded-2xl border border-white/10 bg-white/[0.03] p-4 transition-colors duration-300 hover:bg-white/[0.06]"
            >
              <span class="flex h-8 w-8 shrink-0 items-center justify-center rounded-full bg-[#1faf38]/15 text-xs font-bold text-[#a9e6b6]">
                {{ item.number }}
              </span>
              <div>
                <p class="text-sm font-bold text-white">{{ item.title }}</p>
                <p class="mt-1 text-sm text-white/55">{{ item.desc }}</p>
              </div>
            </div>
          </div>

          <a
            href="#"
            class="group mt-8 inline-flex h-12 items-center justify-center gap-[10px] rounded-full bg-[#1faf38] px-6 text-[15px] font-bold text-[#0b1f14] transition-all duration-300 hover:-translate-y-0.5 hover:bg-white hover:shadow-[0_10px_30px_-5px_rgba(31,175,56,0.5)]"
          >
            <img src="/icons/icon-whatsapp.svg" alt="" class="h-[18px] w-[18px] brightness-0" />
            Mulai Ngebelanjain
            <img src="/icons/icon-arrow-white.svg" alt="" class="h-[18px] w-[18px] brightness-0 transition-transform duration-300 group-hover:translate-x-1" />
          </a>

          <div class="mt-6 flex items-start gap-[10px] text-xs text-white/40">
            <img src="/icons/icon-info.svg" alt="" class="mt-[2px] h-4 w-4 brightness-0 invert opacity-60" />
            <p>Tagihan final mengikuti barang yang berhasil dibeli dan hasil penimbangan.</p>
          </div>
        </div>

        <!-- Mockup chat: device frame -->
        <div v-reveal="150" class="relative mx-auto w-full max-w-[460px]">
          <div class="pointer-events-none absolute -inset-4 rounded-[36px] bg-gradient-to-br from-[#1faf38]/20 to-transparent blur-xl"></div>
          <div class="relative overflow-hidden rounded-[28px] border border-white/10 bg-[#0e2518] shadow-[0_30px_60px_-20px_rgba(0,0,0,0.6)] transition-transform duration-500 hover:-translate-y-1">
            <div class="flex items-center gap-3 border-b border-white/10 bg-white/[0.03] px-5 py-4">
              <span class="flex h-10 w-10 items-center justify-center rounded-full bg-gradient-to-br from-[#1faf38] to-[#00431a] text-[13px] font-extrabold text-white">BP</span>
              <div>
                <p class="text-[15px] font-bold text-white">Belanjaan Pasar</p>
                <p class="flex items-center gap-1 text-xs text-white/40">
                  <span class="h-[6px] w-[6px] rounded-full bg-[#1faf38]"></span>
                  Daftar belanja
                </p>
              </div>
            </div>

            <div class="p-6">
              <div class="ml-auto w-fit max-w-[90%] rounded-2xl rounded-tr-[4px] bg-[#1faf38]/15 px-4 pb-6 pt-[14px]">
                <p class="text-[14.5px] text-white/90">Daftar belanja:</p>
                <p class="text-[14.5px] text-white/90">Cabai merah 500 g, bawang merah 1 kg, tomat 1 kg.</p>
                <p class="text-[14.5px] text-white/90">Catatan: pilih yang segar.</p>
              </div>
              <div class="mt-4 flex justify-center">
                <span class="rounded-full bg-white/[0.06] px-[14px] py-[6px] text-[11.5px] font-medium text-white/50">
                  Tim memproses daftar belanja
                </span>
              </div>
            </div>

            <div class="flex items-center justify-between border-t border-white/10 bg-white/[0.03] p-4">
              <p class="px-1 text-[12.5px] text-white/50">Pilih antar atau ambil di toko.</p>
              <span class="flex items-center gap-[10px] rounded-xl border border-white/15 px-4 py-3 text-sm font-bold text-white">
                <img src="/icons/icon-info-outline.svg" alt="" class="h-[17px] w-[17px] brightness-0 invert" />
                Buka Aplikasi
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  { number: '01', title: 'Pilih Produk & Potongan', desc: 'Tentukan jenis ayam, bagian, jumlah, dan layanan tambahan yang dibutuhkan.' },
  { number: '02', title: 'Hubungi Toko', desc: 'Kirim detail pesanan produk ayam dan unggas melalui WhatsApp toko.' },
  { number: '03', title: 'Konfirmasi Stok & Harga', desc: 'Toko memastikan ketersediaan, harga terbaru, serta pilihan ambil atau kirim.' },
  { number: '04', title: 'Bayar & Terima Pesanan', desc: 'Lakukan pembayaran sesuai konfirmasi. Pesanan disiapkan untuk diambil atau dikirim.' },
]

const jastipSteps = [
  { number: '01', title: 'Isi Daftar Belanja', desc: 'Tuliskan barang, jumlah, dan satuan yang dibutuhkan.' },
  { number: '02', title: 'Pilih Cara Menerima', desc: 'Tentukan antar ke rumah atau ambil di toko.' },
  { number: '03', title: 'Tim Membelanjakan', desc: 'Tim berbelanja sesuai daftar dan ketersediaan barang.' },
  { number: '04', title: 'Konfirmasi Total & Bayar', desc: 'Periksa tagihan final setelah barang dibeli dan ditimbang, lalu ikuti instruksi pembayaran di aplikasi.' },
]
</script>