<script setup>
useSeoMeta({
  title: 'Berita & Artikel - PT Tevori Global Indonesia',
  ogTitle: 'Berita & Artikel - PT Tevori Global Indonesia',
  description: 'Update terkini seputar industri komoditi, furnitur, seni kerajinan, dan regulasi ekspor Indonesia.',
  ogDescription: 'Update terkini seputar industri komoditi, furnitur, seni kerajinan, dan regulasi ekspor Indonesia.',
})
</script>

<template>
  <div class="pt-24 pb-16 md:py-32 px-4 bg-gray-50 min-h-screen">
    <div class="container mx-auto max-w-4xl">
      <!-- Header -->
      <div class="text-center mb-10 md:mb-14 mt-4">
        <div class="inline-block px-4 py-1.5 rounded-full bg-slate-200 text-[#737474] font-bold text-xs md:text-sm mb-6">
          Edukasi & Publikasi
        </div>
        <h1 class="text-3xl sm:text-4xl md:text-5xl font-black text-slate-800 mb-6">
          Insight <span class="text-[#737474]">Industri & Berita</span>
        </h1>
        <div class="w-16 h-1 bg-[#737474] mx-auto mb-6"></div>
        <p class="text-slate-600 text-base md:text-lg max-w-2xl mx-auto px-2">
          Pusat wawasan terkini mengenai tren komoditas, kepatuhan regulasi ekspor global, dan standar kualitas Indonesia.
        </p>
      </div>

      <!-- Coming Soon Card -->
      <div class="bg-white rounded-3xl p-8 sm:p-12 md:p-16 border border-gray-100 shadow-sm text-center relative overflow-hidden">
        <div class="w-20 h-20 bg-gray-50 text-[#737474] rounded-2xl flex items-center justify-center mx-auto mb-6 border border-gray-200/60 shadow-inner">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-10 h-10 text-[#737474]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z" />
          </svg>
        </div>

        <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-slate-100 text-[#737474] border border-slate-200 font-bold text-xs uppercase tracking-wider mb-4">
          <span class="w-2 h-2 rounded-full bg-[#737474] animate-pulse"></span>
          Coming Soon
        </div>

        <h2 class="text-2xl sm:text-3xl font-bold text-slate-800 mb-4">
          Publikasi Artikel Sedang Dalam Penyusunan
        </h2>

        <p class="text-slate-600 text-sm sm:text-base leading-relaxed max-w-xl mx-auto mb-8">
          Tim riset dan editorial kami sedang menyiapkan publikasi artikel eksklusif, analisis pasar, dan panduan teknis ekspor. Nantikan update segera di halaman ini.
        </p>

        <!-- Topic Previews -->
        <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-10 max-w-2xl mx-auto text-left">
          <div class="p-5 rounded-2xl bg-gray-50 border border-gray-100 hover:border-[#737474]/30 transition-colors">
            <span class="text-2xl mb-2 block">📋</span>
            <h4 class="font-bold text-slate-800 text-sm mb-1">Regulasi Ekspor</h4>
            <p class="text-xs text-slate-500 leading-relaxed">Panduan SVLK, sertifikasi mutu, dan kepabeanan internasional.</p>
          </div>
          <div class="p-5 rounded-2xl bg-gray-50 border border-gray-100 hover:border-[#737474]/30 transition-colors">
            <span class="text-2xl mb-2 block">☕</span>
            <h4 class="font-bold text-slate-800 text-sm mb-1">Katalog Komoditi</h4>
            <p class="text-xs text-slate-500 leading-relaxed">Standar mutu biji kopi, rempah, serta furnitur kayu jati.</p>
          </div>
          <div class="p-5 rounded-2xl bg-gray-50 border border-gray-100 hover:border-[#737474]/30 transition-colors">
            <span class="text-2xl mb-2 block">🛡️</span>
            <h4 class="font-bold text-slate-800 text-sm mb-1">Quality Control</h4>
            <p class="text-xs text-slate-500 leading-relaxed">Praktik inspeksi kontainer dan pencegahan risiko perdagangan.</p>
          </div>
        </div>

        <!-- Call to actions -->
        <div class="flex flex-wrap items-center justify-center gap-4">
          <NuxtLink to="/products" class="bg-[#737474] text-white hover:bg-slate-700 font-bold px-6 py-3 rounded-xl transition-all shadow-md text-xs sm:text-sm inline-flex items-center gap-2">
            <span>📦</span> Lihat Katalog Produk
          </NuxtLink>
          <NuxtLink to="/" class="border border-slate-300 text-slate-700 hover:bg-slate-100 font-bold px-6 py-3 rounded-xl transition-all text-xs sm:text-sm inline-flex items-center gap-2">
            <span>🏠</span> Kembali ke Beranda
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>
