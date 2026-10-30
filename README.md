# E-Laundry — Interactive Development Worksheet & Requirements

Dokumentasi lengkap seluruh requirement dan panduan workshop development katalog UMKM yang diadaptasi untuk proyek **E-Laundry**, merujuk langsung pada kurikulum resmi [worksheet.andixurniawan.com/development](https://worksheet.andixurniawan.com/development).

---

## 1. Akses GitHub Pages

Halaman requirement interaktif (lengkap dengan checkbox progres tersimpan, copy prompt AI satu klik, dan checklist 500 poin):
👉 **[https://sodikinnaa.github.io/e-loundry/](https://sodikinnaa.github.io/e-loundry/)**

---

## 2. Struktur 15 Langkah Utama (Worksheet Wajib)

| No | Tahap / User Story | Ringkasan Instruksi & Target |
|:---:|---|---|
| **01** | **Salin template & online-kan Vercel** | Clone template katalog repo, buat repo publik, deploy instan di Vercel. |
| **02** | **Buat proyek Supabase** | Inisialisasi database Postgres Supabase region Southeast Asia (Singapore). |
| **03** | **Buat tabel produk dengan skrip** | Eksekusi `docs/schema.sql` di SQL Editor Supabase untuk skema & RLS. |
| **04** | **Buat akun admin toko** | Daftarkan email & password admin di Supabase Auth, matikan *Allow new users to sign up*. |
| **05** | **Sambungkan Vercel ke Supabase** | Isi `SUPABASE_URL`, `SUPABASE_PUBLISHABLE_KEY`, `SUPABASE_SECRET_KEY` di Environment Variables Vercel lalu redeploy. |
| **06** | **Salin proyek ke laptop** | Clone ke lokal via Git, jalankan `npm install`. |
| **07** | **Pasang kunci & jalankan lokal** | Copy `.env.example` ke `.env.local`, isi kredensial, jalankan `npm run dev`. |
| **08** | **Ubah identitas toko** | Kustomisasi nama, tagline, alamat, jam buka, dan `nomorWhatsApp` di `lib/toko.js`. |
| **09** | **US-01: Katalog dari database** | Hubungkan `app/page.jsx` ke Supabase server-side untuk membaca katalog produk. |
| **10** | **US-02: Detail produk** | Hubungkan `app/produk/[id]/page.jsx` secara dinamis dengan handling `notFound()`. |
| **11** | **US-03: Pesan via WhatsApp** | Pasang format teks WhatsApp otomatis berisi detail layanan & harga di `TombolWhatsApp.jsx`. |
| **12** | **US-04: Login admin** | Buat autentikasi admin via `@supabase/ssr` dan cookie di `app/admin/login/page.jsx`. |
| **13** | **US-05: Ganti password admin** | Server Action ganti password minimal 8 karakter di `app/admin/password/page.jsx`. |
| **14** | **US-06: Proteksi halaman admin** | Buat `proxy.js` (Next.js 16) untuk mengunci seluruh rute `/admin/*` kecuali `/admin/login`. |
| **15** | **Cek keamanan & kumpulkan karya** | Verifikasi checklist keamanan K-6 s/d K-13, lengkapi link Vercel & repo, kumpulkan ke panitia. |

---

## 3. Daftar 44 User Stories Bonus (US-07 s/d US-50)

| Kode | Nama Fitur | Poin |
|---|---|:---:|
| **US-07** | List Produk di panel Admin | 10 |
| **US-08** | Tambah produk baru | 10 |
| **US-09** | Ubah data produk | 10 |
| **US-10** | Hapus produk | 10 |
| **US-11** | Filter kategori atau pencarian produk | 10 |
| **US-12** | Pilih jumlah atau varian kuantitas | 10 |
| **US-13** | Progressive Web App (PWA) | 10 |
| **US-14** | Deskripsi produk dibuat otomatis AI | 10 |
| **US-15** | Urutkan produk (termurah, termahal, terbaru) | 5 |
| **US-16** | Paginasi atau tombol muat lebih banyak | 10 |
| **US-17** | Rekomendasi produk terkait di detail produk | 5 |
| **US-18** | Galeri multi foto produk | 10 |
| **US-19** | Status ketersediaan stok produk | 5 |
| **US-20** | Tampilan harga coret (diskon) & badge promo | 5 |
| **US-21** | Keranjang belanja & pesan borongan via WhatsApp | 15 |
| **US-22** | Halaman Tentang Toko & kontak lengkap | 5 |
| **US-23** | Fitur bagikan dan salin tautan produk | 5 |
| **US-24** | Simpan produk favorit di local storage browser | 10 |
| **US-25** | Toggle Mode Gelap (Dark Mode) | 10 |
| **US-26** | Metadata SEO & OpenGraph media sosial | 5 |
| **US-27** | Generator sitemap.xml dan robots.txt | 5 |
| **US-28** | Halaman 404 kustom & loading skeleton | 5 |
| **US-29** | Upload file gambar ke Supabase Storage | 15 |
| **US-30** | Dashboard metrik & statistik ringkasan admin | 10 |
| **US-31** | Manajemen kategori produk di admin | 15 |
| **US-32** | Toggle status aktif / arsip produk | 10 |
| **US-33** | Fitur pencarian & paginasi di tabel admin | 10 |
| **US-34** | Validasi skema form admin di sisi server | 10 |
| **US-35** | Ekspor seluruh data produk ke file CSV | 10 |
| **US-36** | Riwayat produk terakhir dilihat oleh pengunjung | 5 |
| **US-37** | Fitur bandingkan spesifikasi 2 produk | 15 |
| **US-38** | Sistem ulasan, testimoni, dan rating bintang | 15 |
| **US-39** | Panel moderasi ulasan pembeli di admin | 10 |
| **US-40** | Tracking counter klik pesan WhatsApp | 10 |
| **US-41** | Daftar produk terlaris di dashboard admin | 10 |
| **US-42** | Banner promosi beranda yang dapat dikelola | 10 |
| **US-43** | Manajemen pengaturan identitas toko dari admin | 15 |
| **US-44** | Manajemen banyak akun admin toko | 15 |
| **US-45** | Audit log rekaman aktivitas admin | 10 |
| **US-46** | Fitur impor massal produk via berkas CSV | 15 |
| **US-47** | Atur urutan tampil (display order) produk | 10 |
| **US-48** | Varian harga dinamis per ukuran / paket | 15 |
| **US-49** | Halaman filter khusus per kategori produk | 10 |
| **US-50** | Widget Asisten AI cerdas tanya-jawab produk | 15 |

---

## 4. Checklist Standar Keamanan Aplikasi (K-6 s/d K-13)

| Kode | Kriteria Pemeriksaan Keamanan | Poin |
|---|---|:---:|
| **K-6** | Header keamanan lengkap di aplikasi live (X-Content-Type-Options, Referrer-Policy, HSTS) | 10 |
| **K-7** | Bebas dari celah XSS (`dangerouslySetInnerHTML` / `eval` tanpa sanitasi) | 5 |
| **K-8** | Seluruh rute `/admin` diblokir dari indeks mesin pencari (`X-Robots-Tag: noindex, nofollow`) | 10 |
| **K-9** | Error handler global tidak mengekspos stack trace / traceback ke publik | 5 |
| **K-10** | Dependensi bersih dari celah keamanan kritis (`npm audit --production`) | 5 |
| **K-11** | Penerapan Content-Security-Policy (CSP) ketat | 10 |
| **K-12** | Proteksi rate limit pada endpoint login admin | 10 |
| **K-13** | Tidak ada `console.log` yang mencetak kredensial sensitif atau token auth | 5 |
