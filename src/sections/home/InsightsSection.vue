<script setup>
// Dummy data is removed for production readiness.
// This section displays a 'Coming Soon' state adhering to the Tevori Global design language.
</script>

<template>
  <section id="insights" class="scroll-mt-16 py-16 md:py-24 px-4 bg-white border-t border-gray-100">
    <div class="container mx-auto max-w-6xl">
      <!-- Section Header -->
      <div class="text-center mb-12 md:mb-16 max-w-3xl mx-auto">
        <h2 class="text-3xl md:text-4xl font-bold text-slate-800 mb-4">Berita & <span class="text-[#737474]">Artikel Terbaru</span></h2>
        <div class="w-16 h-1 bg-[#737474] mx-auto mb-4"></div>
        <p class="text-slate-600 mt-2 text-base md:text-lg">Update terkini seputar industri komoditi, furnitur, seni, serta regulasi ekspor Indonesia.</p>
      </div>

      <!-- Coming Soon Card -->
      <div class="bg-gray-50 rounded-3xl p-8 sm:p-12 md:p-16 border border-gray-100 shadow-sm text-center max-w-3xl mx-auto relative overflow-hidden">
        <!-- Subtle decorative glow -->
        <div class="absolute -top-12 -right-12 w-44 h-44 bg-white rounded-full blur-3xl opacity-80 pointer-events-none"></div>
        <div class="absolute -bottom-12 -left-12 w-44 h-44 bg-white rounded-full blur-3xl opacity-80 pointer-events-none"></div>

        <div class="relative z-10">
          <!-- Icon -->
          <div class="w-16 h-16 sm:w-20 sm:h-20 bg-white text-[#737474] rounded-2xl flex items-center justify-center mx-auto mb-6 border border-gray-200/80 shadow-sm">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 sm:w-10 sm:h-10 text-[#737474]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z" />
            </svg>
          </div>

          <!-- Status Badge -->
          <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-slate-200/80 text-[#737474] font-bold text-xs uppercase tracking-wider mb-5">
            <span class="w-2 h-2 rounded-full bg-[#737474] animate-pulse"></span>
            Segera Hadir / Coming Soon
          </div>

          <h3 class="text-2xl sm:text-3xl font-bold text-slate-800 mb-4">
            Artikel & Wawasan Ekspor Sedang Disiapkan
          </h3>

          <p class="text-slate-600 text-sm sm:text-base leading-relaxed max-w-xl mx-auto mb-8">
            Kami tengah menyusun analisis mendalam, panduan regulasi ekspor terkini, serta tren komoditas global untuk membantu keputusan bisnis Anda. Nantikan peluncuran publikasi perdana kami segera!
          </p>

          <!-- Action Buttons -->
          <div class="flex flex-wrap items-center justify-center gap-3">
            <NuxtLink to="/products" class="bg-[#737474] text-white hover:bg-slate-700 font-bold px-6 py-3 rounded-xl transition-all shadow-md text-xs sm:text-sm inline-flex items-center gap-2">
              <span>📦</span> Jelajahi Katalog Produk
            </NuxtLink>
            <NuxtLink to="/insights" class="border border-slate-300 text-slate-700 hover:border-[#737474] hover:text-[#737474] bg-white font-bold px-6 py-3 rounded-xl transition-all text-xs sm:text-sm inline-flex items-center gap-2">
              <span>📰</span> Info Publikasi
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
