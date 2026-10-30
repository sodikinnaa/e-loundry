# E-Laundry Bersih Express — Panduan Pengembangan & Persyaratan

Dokumentasi spesifikasi teknis dan panduan pengembangan proyek **E-Laundry** sesuai kurikulum workshop [Worksheet Development Katalog UMKM](https://worksheet.andixurniawan.com/development).

---

## 1. Ringkasan Proyek

- **Nama Repositori**: `sodikinnaa/e-loundry`
- **Tipe**: Katalog Layanan Laundry UMKM & Pemesanan WhatsApp
- **Live Demo (GitHub Pages)**: `https://sodikinnaa.github.io/e-loundry/`
- **Fitur Utama**:
  - Landing page responsif modern (Tailwind CSS)
  - Dark Mode otomatis & manual switch
  - Kalkulator estimasi biaya cuci kiloan/satuan interaktif
  - Generator format pesan pemesanan ke WhatsApp resmi
  - Antar-jemput dan penentuan titik koordinat/alamat pelanggan

---

## 2. Pemenuhan Requirements (Worksheet Development)

Berdasarkan silabus 15 langkah dan user stories pada worksheet:

| Modul | Kebutuhan Worksheet | Implementasi di Repo Ini |
|---|---|---|
| **Langkah 1 - 2** | Setup repo GitHub publik, deployment online | Repositori berstatus **Public**, GitHub Pages aktif di root branch `main` |
| **Langkah 3 - 5** | Database & Identitas Usaha | Konfigurasi tarif, paket cuci, nomor WhatsApp, dan jam operasional |
| **Langkah 9 - 11** | Katalog Layanan & Order WhatsApp | Kartu paket layanan + tombol otomatis direct WhatsApp chat API |
| **Bonus US-12** | Pilihan kuantitas / berat cucian | Input kilogram/pcs dinamis dengan auto-recalculate |
| **Bonus US-21** | Estimasi keranjang total biaya | Subtotal dihitung otomatis + ongkir antar-jemput |
| **Bonus US-25** | Mode Gelap (Dark Mode) | Toggle tema light/dark terintegrasi dengan `localStorage` |
| **Bonus US-26** | Metadata SEO & OpenGraph | Meta tags deskripsi layanan lengkap di `<head>` |

---

## 3. Struktur File Repositori

```text
e-loundry/
├── index.html       # Halaman utama aplikasi (GitHub Pages entry point)
└── README.md        # Dokumentasi persyaratan & panduan
```

---

## 4. Cara Menjalankan Lokal

Karena proyek ini menggunakan web standar (HTML5 + Tailwind CSS CDN + Vanilla JavaScript), tidak memerlukan kompilasi rumit:

```bash
# Clone repositori
git clone https://github.com/sodikinnaa/e-loundry.git
cd e-loundry

# Buka langsung file di browser
# Di Linux / Mac:
xdg-open index.html   # atau: open index.html
# Atau jalankan HTTP server sederhana:
python3 -m http.server 8080
```

---

## 5. Pengaturan WhatsApp & Profil Toko

Ubah nilai nomor WhatsApp di file `index.html`:
```javascript
const noWA = '6281234567890'; // Ubah ke nomor WhatsApp admin laundry aktif
```
