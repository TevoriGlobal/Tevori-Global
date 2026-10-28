# PT Tevori Global - Company Profile & Digital Sourcing Portal

> **Architecture Flow, CMS Integration, Production Readiness & Developer Guide**  
> *Official repository for PT Tevori Global headless CMS & Nuxt 4 frontend.*

---

## 1. System Architecture Flow

Aplikasi ini mengadopsi arsitektur modern **Headless CMS Jamstack / SSR**:

```text
[ Your Admin Panel ] ──(CRUD Updates)──> [ Sanity Free Cloud API ] ──> [ Nuxt Frontend (Cloudflare Workers) ] ──> [ Global B2B Buyer ]
```

### Penjelasan Alur (Flow):

1. **[ Your Admin Panel ] (Sanity Studio v3):**
   - Panel dashboard visual untuk tim internal PT Tevori Global melakukan Create, Read, Update, dan Delete (CRUD) konten tanpa menyentuh kode.
   - Mengelola katalog produk ekspor, artikel edukasi/insights, profil perusahaan, testimonial, dan kategori bisnis.
   - Berada di dalam folder `tevori-studio/` dan dijalankan terpisah secara lokal atau di-deploy ke Sanity Cloud.

2. **[ Sanity Free Cloud API ] (Sanity Content Lake):**
   - Database cloud global web hooks gratis dan real-time dari Sanity.io yang menyimpan dokumen JSON, asset gambar, dan media.
   - Menyediakan GraphQL & GROQ query API super cepat dengan CDN cache global.

3. **[ Nuxt Frontend (Cloudflare Workers) ]:**
   - Frontend modern berbasis **Nuxt 4** (Vue 3, Vite) + **Tailwind CSS v4** yang di-deploy sebagai Cloudflare Worker menggunakan Nitro dan Wrangler.
   - Mendukung Server-Side Rendering (SSR) & kapabilitas hybrid rendering untuk kecepatan loading maksimal dan SEO optimal bagi calon buyer internasional di Google.
   - Mengambil data katalog produk dengan GROQ query via Sanity Client (`@sanity/client`).
   - Dilengkapi **Graceful Fallback & Production Ready States**: Modul yang belum memiliki data live resmi dilindungi dengan tampilan *Coming Soon* terstandar sehingga tidak mengekspos dummy data ke publik.

4. **[ Global B2B Buyer ]:**
   - Pengalaman penjelajahan B2B yang bersih, responsif di semua perangkat (mobile, tablet, desktop).
   - Dilengkapi Call-to-Action seperti **Request Quotation (RFQ) via WhatsApp** dengan template teks pembelian produk terformat otomatis.

---

## 2. Struktur Direktori

```text
tevori_global/
├── tevori-studio/                  # Konfigurasi Schema Sanity Studio v3 (Admin Panel) berbasis TypeScript
│   ├── schemaTypes/
│   │   ├── product.ts              # Skema Katalog Produk Ekspor (SKU, Specs, MOQ, Foto)
│   │   └── index.ts                # Registrasi keseluruhan koleksi schema Sanity
│   ├── sanity.config.ts            # Konfigurasi Sanity Studio v3 & Plugin Vision
│   ├── sanity.cli.ts               # Konfigurasi basis CLI Sanity
│   └── package.json                # Dependensi Sanity Studio
├── src/                            # Direktori Aplikasi Utama (Nuxt 4 Frontend Codebase)
│   ├── App.vue                     # Master layout template (Navbar, Halaman Routing, Footer)
│   ├── pages/                      # Routing URL otomatis Nuxt berbasis struktur folder 
│   │   ├── index.vue               # Beranda utama (One-page landing section)
│   │   ├── products/               # Galeri Katalog interaktif dengan filter kategori & search
│   │   │   ├── index.vue           # Halaman daftar produk
│   │   │   └── [slug].vue          # Halaman detail produk
│   │   └── insights/               # Modul Berita & Wawasan Industri (Coming Soon state)
│   │       ├── index.vue           # Halaman utama daftar artikel berita
│   │       └── [slug].vue          # Halaman detail artikel berita
│   ├── components/                 # Komponen UI modular independen
│   │   ├── cards/                  # Komponen kartu UI (Product, Service, Testimonial, Insight)
│   │   └── layout/                 # Layout shell (Navbar fixed header, Footer)
│   ├── sections/home/              # Komponen section khusus halaman beranda
│   │   ├── HeroSection.vue         # Section pengantar & value proposition
│   │   ├── AboutSection.vue        # Section visi, misi, dan keunggulan
│   │   ├── ServicesSection.vue     # Section 3 pilar komoditi utama
│   │   ├── HowWeWorkSection.vue    # Section 4 langkah alur sourcing & ekspor
│   │   ├── TestimonialsSection.vue # Section ulasan mitra (Coming Soon state)
│   │   ├── InsightsSection.vue     # Section berita & artikel (Coming Soon state)
│   │   └── ContactSection.vue      # Section formulir & kontak WhatsApp
│   ├── composables/                # Reusable Vue 3 Composition API (misal: useSanity)
│   ├── data/                       # Data statis perusahaan & referensi data lokal
│   │   ├── company.js              # Informasi profil, kontak, alamat, & USP perusahaan
│   │   ├── services.js             # Data pilar layanan ekspor
│   │   ├── testimonials.js         # Arsip data ulasan
│   │   └── insights.js             # Arsip data artikel
│   └── assets/                     # Stylesheet global Tailwind v4 (Main.css)
├── nuxt.config.ts                  # Konfig Nuxt 4, Nitro Cloudflare preset, SEO, & Vite-Tailwind setup
├── wrangler.jsonc                  # Konfigurasi deployment Cloudflare Worker dan assets
├── package.json                    # Kumpulan script `npm run dev/build` dan dependensi utama app
└── .env.example                    # Template standard environment local frontend variable
```

---

## 3. Status Produksi: Modul "Coming Soon"

Untuk kesiapan rilis produksi (*production readiness*), bagian yang sebelumnya memuat data tiruan (*dummy data*) telah disesuaikan agar menampilkan status **Coming Soon** dengan bahasa desain (*design system*) resmi PT Tevori Global:

| Modul / Bagian | File Sumber | Status Saat Ini | Detail Tampilan |
| :--- | :--- | :--- | :--- |
| **Testimoni (Beranda)** | `src/sections/home/TestimonialsSection.vue` | ⏳ Coming Soon | Kartu putih beraksen `#737474`, badge status berdenyut (*pulse*), pesan kurasi ulasan resmi pembeli global, dan indikator jaminan standar internasional. |
| **Berita & Artikel (Beranda)** | `src/sections/home/InsightsSection.vue` | ⏳ Coming Soon | Kartu informasi abu-abu modern (`bg-gray-50`), penjelasan proses penyusunan wawasan ekspor, serta tombol cepat ke Katalog Produk dan Info Publikasi. |
| **Halaman Berita Utama** | `src/pages/insights/index.vue` | ⏳ Coming Soon | Tampilan terdedikasi dengan kartu pratinjau topik utama (Regulasi Ekspor, Katalog Komoditi, & *Quality Control*) serta tombol navigasi. |
| **Detail Artikel Berita** | `src/pages/insights/[slug].vue` | ⏳ Coming Soon | Tampilan fallback informatif yang mencegah tampilan dummy dan mengarahkan kembali pengguna ke halaman berita. |

### Karakteristik Desain yang Digunakan:
- **Brand Accent Color**: `#737474` (Tevori Steel Gray) dipadukan dengan tipografi slate (`text-slate-800` & `text-slate-600`).
- **Gaya Kontainer**: Card rounded sudut besar (`rounded-3xl`), border halus (`border-gray-100`), efek bayangan lembut (`shadow-sm`), dan subtle background glow.
- **Micro-Interactions**: Badge status *pulse dot*, transisi tombol hover, serta tautan terintegrasi ke modul katalog produk yang aktif.

---

## 4. Panduan Menjalankan Project

Repositori ini terdiri dari aplikasi **Frontend (Nuxt)** dan **Admin Panel (Sanity Studio)** yang dikelola dalam struktur *monorepo-style*, berjalan pada proses dan folder yang berbeda.

### Prasyarat Umum:

- **Node.js**: Versi `>= 22.18.0` atau `>= 24.12.0` (Sesuai spesifikasi `engines` environment v22+)
- **NPM**: Versi `>= 9.0.0`
- **Akun Cloudflare** dengan akses ke Workers
- **Wrangler**: Terpasang sebagai dev dependency dan dijalankan melalui `npx` atau npm scripts

### A. Menjalankan Aplikasi Utama (Frontend Web)

1. **Pastikan berada di folder direktori proyek Frontend Utama:**  
   Lokasi *root folder* berada di base repository `Tevori-Global/`.

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Setup Environment Variables Frontend:**  
   Salin file dari `.env.example` lalu ubah menjadi bernama `.env`:
   ```bash
   cp .env.example .env
   ```

   *(Opsional)* Buka file `.env` dan lengkapi dengan Project ID Sanity Anda jika ingin menghubungkan frontend langsung ke Sanity Cloud:
   ```env
   SANITY_PROJECT_ID=your-project-id
   SANITY_DATASET=production
   ```

   > **Catatan:** File `.env` hanya untuk development lokal dan tidak boleh di-commit. Untuk Cloudflare deployment, masukkan environment variables melalui Wrangler Secret atau Cloudflare Dashboard.

4. **Jalankan Frontend Live Server:**
   ```bash
   npm run dev
   ```
   Akses aplikasi melalui browser: `http://localhost:3000`

### B. Menjalankan CMS Admin Panel (Sanity Studio)

Sanity Panel dirancang *self-contained* pada direktori `tevori-studio`.

1. **Masuk ke folder direktori panel admin:**
   ```bash
   cd tevori-studio
   ```

2. **Install Dependencies Sanity Panel:**
   ```bash
   npm install
   ```

3. **Jalankan Studio Server:**
   ```bash
   npm run dev
   ```
   Akses panel admin melalui port default: `http://localhost:3333` (Gunakan akun kolaborator admin Sanity yang valid untuk login).

---

## 5. Build & Deploy ke Cloudflare Workers (Production)

Nuxt menggunakan Nitro dengan preset `cloudflare_module`. Konfigurasi deployment berada di `wrangler.jsonc`:

- Worker entry point: `.output/server/index.mjs`
- Static assets: `.output/public/`
- Compatibility date: `2024-11-01`
- Worker name: `tevori-global`

### Set Secrets di Cloudflare (Wrangler)
```bash
npx wrangler secret put SANITY_PROJECT_ID
npx wrangler secret put SANITY_DATASET
npx wrangler secret put SANITY_API_TOKEN
```

### Build & Deploy
Dari root repository, jalankan:
```bash
# Build aplikasi Nuxt
npm run build

# Atau jalankan preview lokal hasil build dengan Wrangler
npm run preview

# Deploy langsung ke Cloudflare Workers
npm run deploy
```
