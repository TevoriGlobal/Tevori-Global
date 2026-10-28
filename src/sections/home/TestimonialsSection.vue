<script setup>
// Dummy data is removed for production readiness.
// This section displays a 'Coming Soon' state adhering to the Tevori Global design language.
</script>

<template>
  <section id="testimonials" class="scroll-mt-20 py-16 md:py-24 px-4 bg-gray-50 border-t border-gray-100">
    <div class="container mx-auto max-w-6xl">
      <!-- Section Header -->
      <div class="text-center mb-12 md:mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-slate-800 mb-6">Kepercayaan <span class="text-[#737474]">Klien Kami</span></h2>
        <div class="w-16 h-1 bg-[#737474] mx-auto mb-6"></div>
        <p class="text-slate-600 mt-4 text-base md:text-lg max-w-2xl mx-auto px-4">Apa kata mitra internasional mengenai kerja sama pengadaan komoditas dari Indonesia bersama Tevori Global.</p>
      </div>

      <!-- Coming Soon Card -->
      <div class="max-w-3xl mx-auto bg-white rounded-3xl p-8 sm:p-12 md:p-16 border border-gray-100 shadow-sm text-center relative overflow-hidden">
        <!-- Subtle decorative glow -->
        <div class="absolute -top-12 -right-12 w-44 h-44 bg-slate-100 rounded-full blur-3xl opacity-60 pointer-events-none"></div>
        <div class="absolute -bottom-12 -left-12 w-44 h-44 bg-slate-100 rounded-full blur-3xl opacity-60 pointer-events-none"></div>

        <div class="relative z-10">
          <!-- Icon -->
          <div class="w-16 h-16 sm:w-20 sm:h-20 bg-slate-50 text-[#737474] rounded-2xl flex items-center justify-center mx-auto mb-6 border border-gray-200/80 shadow-inner">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 sm:w-10 sm:h-10 text-[#737474]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
            </svg>
          </div>

          <!-- Status Badge -->
          <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-slate-100 text-[#737474] border border-slate-200 font-bold text-xs uppercase tracking-wider mb-5">
            <span class="w-2 h-2 rounded-full bg-[#737474] animate-pulse"></span>
            Segera Hadir / Coming Soon
          </div>

          <h3 class="text-2xl sm:text-3xl font-bold text-slate-800 mb-4">
            Ulasan Klien Sedang Dalam Proses Kurasi
          </h3>

          <p class="text-slate-600 text-sm sm:text-base leading-relaxed max-w-xl mx-auto mb-8">
            Kami sedang mengumpulkan dan memverifikasi testimoni resmi dari mitra bisnis serta pembeli global kami. Bagian ini akan segera diperbarui dengan studi kepuasan dan ulasan kemitraan nyata.
          </p>

          <!-- Key highlights -->
          <div class="pt-6 border-t border-gray-100 flex flex-col sm:flex-row items-center justify-center gap-4 sm:gap-6 text-xs sm:text-sm text-slate-500">
            <span class="flex items-center gap-2">
              <span class="text-[#737474] font-bold">✓</span> Kemitraan Terverifikasi
            </span>
            <span class="hidden sm:inline text-slate-300">•</span>
            <span class="flex items-center gap-2">
              <span class="text-[#737474] font-bold">✓</span> Transparansi Ekspor
            </span>
            <span class="hidden sm:inline text-slate-300">•</span>
            <span class="flex items-center gap-2">
              <span class="text-[#737474] font-bold">✓</span> Standar Internasional
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
