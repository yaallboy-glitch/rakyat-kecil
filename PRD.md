# PRD — Landing Page "Rakyat Kecil"

Versi 1.0 · 13 Okt 2026 · Status: siap eksekusi (keputusan dipatok, lihat §9)

## 1. Ringkasan produk
Landing page statis untuk jasa pembuatan website. Satu halaman, satu tujuan: orang
menekan tombol WhatsApp dan mengirim pesan. Semua transaksi, negosiasi, dan brief
terjadi di WhatsApp — halaman tidak punya form, tidak punya akun, tidak punya database.

- Nama brand: **Rakyat Kecil**
- Tagline kerja: "Jasa bikin website apa saja. Dari UMKM sampai perusahaan."
- Pemilik: satu orang (freelancer/perorangan), bukan agensi

### Tujuan (goals)
1. Menghasilkan chat WhatsApp masuk dari calon klien (metrik utama, lihat §7).
2. Menjelaskan tiga tingkat harga dalam < 10 detik baca, supaya klien datang dengan
   ekspektasi budget yang benar.
3. Memamerkan karya nyata sebagai bukti kemampuan.

### Non-goals
- Tidak ada form kontak, newsletter, atau login.
- Tidak ada CMS/admin. Teks + gambar diubah langsung di file.
- Tidak ada pembayaran online / invoice / keranjang.
- Tidak ada blog.
- Tidak ada backend, tidak ada analitik pihak ketiga, tidak ada cookie banner.

## 2. Target user
Dua persona, keduanya pakai WhatsApp sebagai alat kerja harian.

**Persona A — Bu Rina, pemilik UMKM**
Katering rumahan, 8 pesanan/hari via WhatsApp dan IG. Belum punya website; katalog
cuma berupa foto di feed yang tenggelam. Budget Rp 500rb terasa sudah mahal.
Dia butuh: halaman yang bisa dikirim ke calon pembeli, punya menu + harga + tombol chat.
Ketakutan: ditipu, dibayar di depan lalu kabur, istilah teknis ("domain", "hosting").

**Persona B — Pak Dedi, admin/marketing perusahaan kecil**
Toko bahan bangunan atau vendor jasa, 15-40 karyawan. Punya website lama (2016) yang
rusak di HP. Dia diminta bos mencari yang lebih murah dan cepat daripada agensi.
Dia butuh: sistem yang bisa dipakai tim (harga produk, stok, katalog), atau aplikasi
web/marketplace. Budget Rp 1,2jt–Rp 2jt+. Dia membandingkan penawaran, tanya
portofolio dan "siapa yang ngerjain".

## 3. Struktur halaman
Satu halaman, urutan blok tetap (tidak ada tab/route):

| # | Section | Tujuan | Angle copy |
|---|---|---|---|
| 1 | Hero | Tangkap 5 detik pertama | Wordmark "Rakyat Kecil" besar + kalimat harga terendah + 2 tombol (Chat WA, Lihat karya) |
| 2 | Band jasa | Perluas persepsi "apa saja" | Pita berjalan berisi jenis web yang bisa dibuat |
| 3 | Layanan | Jawab "kamu bisa apa" | 4 baris bernomor (bukan kartu seragam): Landing, Web + Backend, Web App/Marketplace, Perawatan |
| 4 | Karya | Bukti | 6 kartu karya; 1 kartu unggulan lebih besar |
| 5 | Cara kerja | Kurangi risiko | 4 langkah pendek, ditegaskan DP 50% dan revisi |
| 6 | Harga | Kualifikasi budget | 3 tingkat: 500rb / 1,2jt / mulai 2jt + isi paket |
| 7 | Kenapa Rakyat Kecil | Ganti testimoni | 3 alasan jujur (dikerjakan langsung, harga terbuka, garansi revisi) |
| 8 | FAQ | Bongkar keberatan | 6 pertanyaan: DP, revisi, domain/hosting, lama pengerjaan, pembayaran, sumber kode |
| 9 | CTA penutup | Konversi terakhir | Kalimat + satu tombol WA besar |
| 10 | Footer | Info + navigasi | Kontak WA, tahun, navigasi ringkas |

Catatan: **tidak ada section testimoni.** Belum ada klien nyata; mengarang kutipan
dilarang. Diganti section §7 "Kenapa Rakyat Kecil".
## 4. Harga dan isi paket
Angka final dari klien:

| Tingkat | Harga | Peruntukan |
|---|---|---|
| Landing Page | **Rp 500.000** | Satu halaman, promosi/profil, UMKM |
| Web + Backend | **Rp 1.200.000** | Website dengan panel admin, data dinamis |
| Web App / Marketplace | **mulai Rp 2.000.000** | Aplikasi web penuh, multi-user, marketplace |

Isi paket (usulan, boleh dikoreksi tanpa mengubah kode lain — lihat §10):
- **Landing Page**: 1 halaman, responsif HP/tablet/desktop, tombol WhatsApp, teks
  dibantu tulis, gratis 1 putaran revisi, pengerjaan 2–4 hari kerja.
- **Web + Backend**: semua isi Landing + banyak halaman, panel admin untuk isi konten
  sendiri, database, formulir yang tersimpan, daftar produk/harga dinamis,
  pengerjaan 1–2 minggu.
- **Web App / Marketplace**: semua isi Web + Backend + akun pengguna, peran
  admin/penjual/pembeli, keranjang atau transaksi, dashboard, pengerjaan sesuai
  kesepakatan. Harga akhir tergantung fitur — karena itu "mulai dari".

Setiap paket punya tombol WhatsApp dengan pesan awal berbeda, menyebut nama paket
dan harganya, supaya pemilik langsung tahu konteks chat.

## 5. Portofolio (karya)
6 kartu. Skema satu karya: `nama` · `jenis` · `ringkas` (1 baris) · `link` (opsional).

Slot yang disiapkan (nama/jenis placeholder, isi final menyusul dari klien):
1. Alif Bimbel — web lembaga bimbel
2. Kedai Kopi — landing UMKM + menu
3. Studio Portofolio — situs portofolio pribadi
4. DSMD — web profil
5. Aplikasi Web — web app
6. Karya ke-6 — diisi klien atau dihapus

Screenshot: **menyusul dari klien.** Sampai gambar ada, kartu memakai blok
placeholder bermotif + judul, dan `<img>` yang gagal dimuat disembunyikan sendiri
sehingga tidak ada ikon gambar rusak. Struktur kartu tidak berubah setelah gambar
masuk — cukup taruh file di `assets/` sesuai nama yang diminta di kode.

## 6. Kebutuhan fungsional
1. **Bahasa ganda** ID ⇄ EN. Tombol di header. Default Indonesia. Pilihan disimpan
   di `localStorage` (kunci: `rk-lang`). Semua teks lewat atribut `data-i18n`.
   Judul dokumen ikut berubah.
2. **CTA WhatsApp.** Semua tombol menuju `https://wa.me/6285173064953` dengan
   parameter `?text=` berbeda per paket. Nomor tampil juga sebagai link `tel:` di footer.
3. **Navigasi.** Anchor `#layanan #karya #proses #harga #faq #kontak`, geser halus,
   header menandai section aktif. Menu mobile: satu tombol buka/tutup.
4. **Animasi.** Reveal saat scroll, hover, pita berjalan. Semua dimatikan bila
   `prefers-reduced-motion: reduce`.
5. **Tanpa form, tanpa jaringan.** Tidak ada fetch, tidak ada API, tidak ada
   dependency eksternal selain Google Fonts (dengan fallback font sistem).
## 7. Non-functional requirements
- **Performa**: satu halaman, total aset kecil, tata letak tanpa pergeseran (font
  fallback seukuran), gambar `loading="lazy"`.
- **SEO**: `<title>`, meta description, canonical, Open Graph + Twitter card,
  JSON-LD `ProfessionalService` + `FAQPage`. Bahasa `lang="id"` di `<html>`.
- **Aksesibilitas**: kontras teks ≥ 4.5:1 di atas latar sebenarnya, `:focus-visible`
  jelas, tombol/tautan bernama, `<details>` asli untuk FAQ, target sentuh ≥ 44px,
  `aria-label` untuk tombol ikon, `aria-expanded` untuk menu mobile.
- **Responsif**: diuji di 390×780 dan 1280×800. Tidak ada scroll horizontal.
- **Kode**: HTML + CSS + JS dipisah (`index.html`, `style.css`, `script.js`).
  Tanpa framework, tanpa build step.
- **Teks panjang tanpa spasi** (mis. nama domain panjang) tidak boleh merusak tata
  letak — pakai `overflow-wrap: anywhere` pada blok teks.

### Metrik sukses
- Klik WhatsApp per 100 kunjungan (utama). Target awal: ≥ 5%.
- Waktu sampai halaman siap < 2,5 detik di jaringan seluler.
- Tidak ada satu pun error konsol di 390×780 dan 1280×800.

## 8. Kriteria terima
1. Semua teks Indonesia punya padanan Inggris; toggle mengubah seluruh halaman.
2. Semua tombol WA membuka `wa.me` dengan pesan awal sesuai paket.
3. 390×780 dan 1280×800: tidak ada overflow horizontal, tidak ada error konsol.
4. Bagian harga menyebut tepat 500.000 / 1.200.000 / mulai 2.000.000.
5. Tampilan tetap utuh walau gambar karya belum ada.
6. `prefers-reduced-motion` mematikan animasi.

## 9. Keputusan yang sudah dipatok
- Folder proyek: `rakyat-kecil/`
- Logo: wordmark teks (tanpa file gambar), animasi halus saat dimuat
- Tema: gelap-editorial + satu aksen hangat; font display serif berpasangan dengan
  sans geometris (Fraunces + Plus Jakarta Sans), fallback font sistem
- Animasi tingkat sedang (bukan parallax berat)
- Testimoni: dibuang, diganti section alasan (§3 no. 7)
- Bahasa default: Indonesia

## 10. Pertanyaan terbuka (tidak menghambat)
1. Teks isi paket (§4 usulan) — koreksi bila ada yang tidak sesuai praktik nyata.
2. Nama + jenis + 1 baris deskripsi tiap karya, dan screenshot-nya.
3. URL demo tiap karya, kalau ada.
4. Kontak selain WhatsApp (IG/TikTok/email) — sekarang belum ada di footer.
5. Domain dan hosting — belum diputuskan; halaman murni statis jadi bisa dipasang
   di mana saja.