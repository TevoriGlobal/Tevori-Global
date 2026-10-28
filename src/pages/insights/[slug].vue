<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

const goBack = () => {
  router.push('/insights')
}

useSeoMeta({
  title: 'Artikel Segera Hadir - PT Tevori Global Indonesia',
  description: 'Artikel sedang dalam proses verifikasi dan penyusunan.',
})
</script>

<template>
  <div class="pt-24 pb-16 md:py-32 px-4 bg-gray-50 min-h-screen flex items-center justify-center">
    <div class="container mx-auto max-w-xl text-center">
      <div class="bg-white p-8 sm:p-12 rounded-3xl border border-gray-100 shadow-sm">
        <div class="w-16 h-16 bg-gray-50 text-[#737474] rounded-2xl flex items-center justify-center mx-auto mb-6 border border-gray-200/60 shadow-inner">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8 text-[#737474]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.8" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
          </svg>
        </div>

        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-slate-100 text-[#737474] border border-slate-200 font-bold text-xs uppercase tracking-wider mb-4">
          <span class="w-2 h-2 rounded-full bg-[#737474] animate-pulse"></span>
          Coming Soon
        </div>

        <h2 class="text-2xl font-bold text-slate-800 mb-3">Artikel Sedang Dalam Penyusunan</h2>
        <p class="text-slate-600 text-sm mb-6 leading-relaxed">
          Artikel yang Anda tuju sedang dalam tahap kurasi dan verifikasi sebelum dipublikasikan secara resmi.
        </p>

        <button @click="goBack" class="bg-[#737474] hover:bg-slate-700 text-white font-bold px-6 py-2.5 rounded-xl transition-all text-xs sm:text-sm">
          Kembali ke Halaman Berita
        </button>
      </div>
    </div>
  </div>
</template>
