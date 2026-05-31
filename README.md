# 🌴 Karawang Tourism Guide
### *Dari Pantai Hingga Sejarah dalam Satu Destinasi*

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?style=flat-square&logo=github)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

> Website panduan wisata Kabupaten Karawang yang memperkenalkan keindahan pantai utara, situs sejarah peradaban tertua di Jawa, dan pesona alam pegunungan Sanggabuana — semuanya dalam satu halaman yang elegan.

---

## 🔗 Demo Live

**[karawang-tourism.github.io](https://username.github.io/karawang-tourism)**
> *(ganti `username` dengan GitHub username kamu)*

---

## 📸 Preview

| Hero Section | Destinasi Cards | Modal Detail |
|---|---|---|
| Full-screen pantai | Grid 9 destinasi | Info lengkap tiap wisata |

---

## ✨ Fitur Website

- **🎨 Desain Modern** — Typografi Playfair Display + DM Sans, palet warna earth tone terinspirasi alam Karawang
- **📱 Fully Responsive** — Tampil sempurna di desktop, tablet, dan mobile
- **🔍 Filter Destinasi** — Sortir berdasarkan kategori: Pantai, Sejarah, Alam, Rekreasi
- **🖼️ Modal Popup** — Detail lengkap setiap destinasi (lokasi, jam buka, harga, deskripsi)
- **🎞️ Auto-Scroll Gallery** — Strip galeri foto bergerak otomatis, pause saat hover
- **🗺️ Google Maps Embed** — Peta interaktif lokasi Karawang
- **✨ Scroll Reveal Animation** — Elemen muncul dengan animasi saat di-scroll
- **🌙 Sticky Navbar** — Navigasi transparan yang berubah saat scroll
- **♿ Accessible** — Semantic HTML, alt text pada semua gambar, keyboard navigation
- **⚡ Zero Dependencies** — Pure HTML/CSS/JS, tidak butuh framework atau npm

---

## 🗂️ Struktur File

```
karawang-tourism/
│
├── index.html          # File utama (single-page website)
├── README.md           # Dokumentasi ini
├── LICENSE             # MIT License
└── .gitignore          # File yang diabaikan Git
```

> Website ini dibuat sebagai **single HTML file** — semua CSS dan JavaScript sudah diembed langsung di dalam `index.html` untuk kemudahan deploy di GitHub Pages.

---

## 🏖️ Destinasi yang Ditampilkan

| No | Nama Destinasi | Kategori | Harga Tiket |
|----|----------------|----------|-------------|
| 1 | Candi Jiwa — Situs Batujaya | 🏛️ Sejarah | Rp 5.000 |
| 2 | Pantai Pelangi | 🌊 Pantai | Rp 15.000 |
| 3 | Curug Cigentis | 🌿 Alam | Rp 10.000 |
| 4 | Pantai Tanjung Baru | 🌊 Pantai | Rp 10.000 |
| 5 | Danau Cipule | 🌿 Alam | Rp 10.000 |
| 6 | Pantai Sedari | 🌊 Pantai | Gratis |
| 7 | New Marigold Garden | 🎡 Rekreasi | Rp 15.000 |
| 8 | Curug Bandung | 🌿 Alam | Rp 10.000 |
| 9 | Kampung Turis | 🎡 Rekreasi | Rp 25.000 |

---

## 🚀 Cara Deploy ke GitHub Pages

### Langkah 1 — Buat Repository Baru
```
1. Login ke github.com
2. Klik tombol "+" → "New repository"
3. Nama repo: karawang-tourism (atau nama lain)
4. Pilih: Public ✅
5. Klik "Create repository"
```

### Langkah 2 — Upload File
```
1. Di halaman repo, klik "uploading an existing file"
2. Drag & drop semua file dari folder ini (index.html, README.md, dll)
3. Scroll ke bawah → tulis commit message: "Initial commit"
4. Klik "Commit changes"
```

### Langkah 3 — Aktifkan GitHub Pages
```
1. Klik tab "Settings" di repo
2. Scroll ke bagian "Pages" di sidebar kiri
3. Source: pilih "Deploy from a branch"
4. Branch: main / root
5. Klik "Save"
6. Tunggu 1-2 menit ☕
7. Website live di: https://[username].github.io/karawang-tourism
```

### Atau via Git CLI
```bash
git init
git add .
git commit -m "Initial commit: Karawang Tourism Guide"
git branch -M main
git remote add origin https://github.com/USERNAME/karawang-tourism.git
git push -u origin main
```

---

## 🛠️ Teknologi

| Teknologi | Kegunaan |
|-----------|----------|
| HTML5 | Struktur halaman |
| CSS3 | Styling, animasi, responsive layout |
| Vanilla JavaScript | Interaktivitas (filter, modal, scroll) |
| Google Fonts | Playfair Display, DM Sans, Bebas Neue |
| Unsplash API | Foto destinasi wisata |
| Wikimedia Commons | Foto Candi Jiwa asli |
| Google Maps Embed | Peta interaktif Karawang |

---

## 📁 Cara Edit Konten

### Menambah Destinasi Baru
Buka `index.html`, cari bagian `<!-- CARD -->` dan duplikasi satu blok card:

```html
<div class="card" data-cat="KATEGORI"
     onclick="openModal('NAMA','KATEGORI','URL_FOTO','LOKASI','JAM','HARGA','DESKRIPSI','ALAMAT','JARAK','FASILITAS')">
  <div class="card-img-wrap">
    <img src="URL_FOTO" alt="NAMA" loading="lazy"/>
    <span class="card-category cat-KATEGORI">Label</span>
  </div>
  <div class="card-body">
    <h3 class="card-name">NAMA DESTINASI</h3>
    ...
  </div>
</div>
```

**Kategori yang tersedia:** `pantai` · `sejarah` · `alam` · `rekreasi`

### Mengganti Warna Tema
Cari bagian `:root` di CSS dan ubah variabel warna:
```css
:root {
  --rust:    #C4572A;   /* Warna aksen utama */
  --ochre:   #C89B3C;   /* Warna emas/highlight */
  --teal:    #1A5C58;   /* Warna hijau-biru */
  --navy:    #0D2B3E;   /* Warna gelap utama */
}
```

---

## 📝 Lisensi

Proyek ini menggunakan lisensi **MIT** — bebas digunakan, dimodifikasi, dan didistribusikan untuk keperluan pribadi maupun komersial.

Foto dari **Unsplash** (lisensi Unsplash gratis) dan **Wikimedia Commons** (lisensi Creative Commons).

---

## 🙌 Kredit

- Dibuat dengan ❤️ untuk memperkenalkan keindahan **Kabupaten Karawang**
- Data wisata bersumber dari berbagai referensi lokal dan artikel perjalanan
- Foto oleh para fotografer di Unsplash & kontributor Wikimedia Commons

---

*Made with love for Karawang 🌴*
