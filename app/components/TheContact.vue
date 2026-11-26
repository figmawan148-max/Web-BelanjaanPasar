<template>
  <section class="relative overflow-hidden bg-[#0b1f14] px-5 py-20 md:px-10">
    <!-- Dekorasi -->
    <div
      class="pointer-events-none absolute -left-20 top-10 h-[380px] w-[380px] rounded-full bg-[#1faf38]/20 blur-[120px]"
    ></div>
    <div
      class="pointer-events-none absolute right-0 bottom-0 h-[320px] w-[320px] rounded-full bg-[#a9e6b6]/10 blur-[110px]"
    ></div>

    <div class="relative mx-auto max-w-[1280px]">
      <!-- Header -->
      <div
        v-reveal
        class="flex flex-col gap-6 md:flex-row md:items-end md:justify-between"
      >
        <div>
          <p
            class="mb-3 flex items-center gap-[10px] text-base font-bold uppercase text-[#a9e6b6]"
          >
            <img src="/icons/vector-line.svg" alt="" class="w-[31px]" />
            Lokasi &amp; Kontak
          </p>
          <h2
            class="max-w-[600px] font-['Plus_Jakarta_Sans'] text-3xl font-extrabold leading-[1.1] text-white md:text-[48px]"
          >
            Kunjungi toko kami di
            <span class="font-semibold italic text-[#a9e6b6]"
              >Pasar Alfa Indah.</span
            >
          </h2>
        </div>

        <a
          href="#"
          class="group inline-flex h-14 w-fit shrink-0 items-center gap-[10px] rounded-full bg-[#1faf38] px-7 text-[15px] font-bold text-white transition-all duration-300 hover:-translate-y-0.5 hover:bg-white hover:text-[#0b1f14] hover:shadow-[0_10px_30px_-5px_rgba(31,175,56,0.5)]"
        >
          <img
            src="/icons/icon-whatsapp-filled.svg"
            alt=""
            class="h-[18px] w-[18px] brightness-0 invert transition-all duration-300 group-hover:invert-0"
          />
          Hubungi Kami
          <img
            src="/icons/icon-arrow-small.svg"
            alt=""
            class="h-[18px] w-[18px] brightness-0 invert transition-all duration-300 group-hover:translate-x-1 group-hover:invert-0"
          />
        </a>
      </div>

      <!-- Grid utama -->
      <div class="mt-12 grid grid-cols-1 gap-5 lg:grid-cols-[0.85fr_1.15fr]">
        <!-- Kiri: info kontak sebagai kartu metrik -->
        <div v-reveal="100" class="flex flex-col gap-5">
          <div
            class="rounded-[24px] border border-white/10 bg-white/[0.04] p-7"
          >
            <p class="text-sm text-white/60">Hubungi toko langsung melalui</p>
            <p class="mt-2 text-xl font-bold text-white">0813 10 11 12 74</p>
            <p class="text-sm text-white/50">
              WhatsApp &amp; Telepon &middot; admin
            </p>
          </div>

          <div class="grid grid-cols-2 gap-5">
            <div
              v-for="item in infoItems"
              :key="item.label"
              class="group rounded-[24px] border border-white/10 bg-white/[0.04] p-6 transition-all duration-300 hover:-translate-y-1 hover:bg-white/[0.08]"
            >
              <p
                class="text-xs font-bold uppercase tracking-[0.8px] text-white/50"
              >
                {{ item.label }}
              </p>
              <p class="mt-1 text-[15px] font-bold text-white">
                {{ item.value }}
              </p>
            </div>
          </div>
        </div>

        <!-- Kanan: peta dengan pin berdenyut -->
        <div
          v-reveal="200"
          class="relative min-h-[420px] overflow-hidden rounded-[28px] border border-white/10 bg-[#0e2518]"
        >
          <img
            src="/icons/map-lines-decorative.svg"
            alt=""
            class="absolute left-0 top-1/2 w-full -translate-y-1/2 opacity-[0.15]"
          />
          <div
            class="pointer-events-none absolute inset-0 bg-[radial-gradient(circle_at_50%_40%,rgba(31,175,56,0.15),transparent_60%)]"
          ></div>

          <!-- Pin berdenyut -->
          <div
            class="relative flex h-full flex-col items-center justify-center px-6 pb-28 pt-10 text-center"
          >
            <div class="relative flex h-20 w-20 items-center justify-center">
              <span
                class="absolute h-full w-full animate-ping rounded-full bg-[#1faf38]/40"
              ></span>
              <span
                class="relative flex h-14 w-14 items-center justify-center rounded-full bg-[#1faf38] shadow-[0_0_0_6px_rgba(31,175,56,0.15)]"
              >
                <img
                  src="/icons/icon-store-pin.svg"
                  alt=""
                  class="h-6 w-6 brightness-0 invert"
                />
              </span>
            </div>
            <span
              class="mt-6 rounded-full border border-white/15 bg-white/10 px-4 py-[6px] text-xs font-semibold text-white backdrop-blur-sm"
            >
              Pasar Alfa Indah
            </span>
            <p class="mt-3 max-w-[300px] text-sm text-white/60">
              Jl. Palem V, Petukangan Utara, Pesanggrahan, Jakarta Selatan
              12660.
            </p>
          </div>

          <!-- Kartu toko mengambang -->
          <div
            class="absolute inset-x-4 bottom-4 flex flex-col gap-4 rounded-2xl border border-white/10 bg-white/95 p-6 backdrop-blur-md transition-transform duration-300 hover:-translate-y-1 sm:flex-row sm:items-center sm:justify-between"
          >
            <div>
              <p
                class="text-xs font-bold uppercase tracking-[0.8px] text-[#137a32]"
              >
                Jam Buka
              </p>
              <p class="mt-2 text-[15px] font-bold text-[#131b2e]">
                Setiap hari &middot; 06.00&ndash;10.00 WIB
              </p>
            </div>
            <span
              class="flex h-11 w-fit shrink-0 items-center gap-[10px] rounded-xl border border-[#131b2e]/15 px-5 text-sm font-bold text-[#131b2e] transition-all duration-300 hover:bg-[#131b2e] hover:text-white"
            >
              <img src="/icons/icon-navigation.svg" alt="" class="h-4 w-4" />
              Petunjuk Arah
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const infoItems = [
  { label: "Alamat Toko", value: "Pasar Alfa Indah" },
  { label: "WhatsApp", value: "0813 101 112 74" },
  { label: "Lokasi", value: "Jakarta Selatan" },
  { label: "Jam Operasional", value: "06.00 - 10.00 WIB" },
];
</script>
