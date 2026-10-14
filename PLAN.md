# PLAN — Landing Page "Rakyat Kecil"

Rencana eksekusi untuk memenuhi `PRD.md`. Tanpa framework, tanpa build step,
tanpa dependency (selain Google Fonts dengan fallback).

## Berkas
| Berkas | Isi |
|---|---|
| `index.html` | Seluruh struktur + teks sumber (Indonesia) + atribut `data-i18n` |
| `style.css` | Semua gaya: token, tata letak, animasi, responsif |
| `script.js` | Kamus ID/EN, toggle bahasa, menu mobile, reveal scroll, tahun footer |
| `assets/` | Tempat screenshot karya (menyusul) |
| `PRD.md` / `PLAN.md` | Dokumen ini |

## Token desain (dikunci di `:root`)
- Latar: `#0E0C0B` (tinta hangat gelap), permukaan `#171412`, garis `#2A241F`
- Teks: `#F4EDE4`, teks lemah `#A79C90`
- Aksen: `#F0A03C` (kuning tanah/hangat), aksen kedua `#E05433` (bata) untuk penanda
- Font: `Fraunces` (display serif, variabel) + `Plus Jakarta Sans` (teks), fallback
  `Georgia` / `system-ui`

## Tahapan
1. **Skaffold** — `index.html` (head: meta, OG, JSON-LD, font) + header + hero
   wordmark. `style.css` (token, reset, tipografi, header, hero).
2. **Section isi** — pita jasa, layanan bernomor, karya 6 kartu, cara kerja.
3. **Section penutup** — harga 3 tingkat, kenapa rakyat kecil, FAQ, CTA, footer.
4. **Interaksi** — `script.js`: kamus ID/EN, toggle + `localStorage('rk-lang')`,
   menu mobile (`aria-expanded`), reveal scroll (`IntersectionObserver`),
   penanda nav aktif, tombol WA berpesan awal per paket, tahun footer.
5. **Responsif & aksesibilitas** — breakpoint 1080/820/560, target sentuh ≥44px,
   `:focus-visible`, `prefers-reduced-motion`, `overflow-wrap: anywhere`.
6. **Verifikasi** — `chromium-browser --headless=new --no-sandbox` dua ukuran layar
   (390×780, 1280×800); cek `pageerror` + `console.error`; cek tanpa overflow
   horizontal; cek toggle bahasa; cek `prefers-reduced-motion`.
7. **Penyelesaian** — laporan: berkas, perintah, hasil.

## Urutan aman (agar halaman tidak rusak di tengah jalan)
Tulis `style.css` bertahap: token+reset → header+hero → pita+layanan → karya+proses →
harga+alasan → FAQ+CTA+footer → responsif. Tiap berkas di bawah 3000 karakter per
penyuntingan; berkas besar dipecah jadi beberapa panggilan, bukan ditimpa total.

## Risiko
| Risiko | Penanganan |
|---|---|
| Google Fonts tidak tersedia (luring) | fallback Georgia/system-ui sudah diset seukuran |
| Screenshot karya belum ada | kartu punya latar bermotif; `<img>` gagal dimuat disembunyikan |
| Teks panjang tanpa spasi merusak tata letak | `overflow-wrap: anywhere` pada blok teks |
| Animasi mengganggu | seluruh animasi dibungkus media query `prefers-reduced-motion` |