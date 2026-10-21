# Generator Surat Penawaran MEGACON PRECAST

## Struktur file
- `index.html` — struktur aplikasi dan template surat.
- `style.css` — gaya antarmuka, kop surat, tabel, tanda tangan, footer, dan aturan cetak.
- `app.js` — logika master produk, kalkulasi, penomoran lokal, riwayat, dan ekspor.
- `assets/` — gambar tetap untuk dokumen:
  - `brand.jpg` — logo default MEGACON PRECAST (dipakai jika logo perusahaan belum diunggah)
  - `stamp.png` — stempel/tanda tangan visual
  - `footer.png` — ornamen footer surat
- `README.md` — petunjuk penggunaan.

## Menjalankan
1. Simpan semua file dengan struktur folder di atas (termasuk folder `assets/`).
2. Buka `index.html` di Firefox, Chrome, atau Edge.
   - Disarankan lewat server lokal sederhana agar `fetch` asset lancar, contoh:
     ```bash
     # Python
     python3 -m http.server 8080
     # lalu buka http://localhost:8080
     ```
   - Atau buka langsung `index.html` (gambar tetap bisa tampil lewat path relatif).
3. Isi identitas perusahaan dan logo dari menu **Identitas Perusahaan**.
4. Isi master produk dengan harga resmi.
5. Buat penawaran dan uji hasil PDF/Word.

## Mengatur bagian kop
Kop masih perlu dibandingkan langsung dengan Word asli. CSS kop berada di `style.css`, terutama selector:
- `.qt-header`
- `.qt-brand`
- `.qt-brand-name`
- `.qt-company`
- `.qt-rule`

Struktur HTML kop dibuat oleh fungsi `documentHtml()` di `app.js`. Logo perusahaan diunggah lewat aplikasi; data perusahaan dan harga tidak diisi otomatis.

Asset default (logo brand, stempel, footer) ada di folder `assets/` dan dimuat saat aplikasi start. Untuk ganti gambar default, cukup ganti file di folder tersebut (nama file tetap).

## Batasan
- Data tersimpan di `localStorage` browser/perangkat, belum tersinkron antar pengguna.
- Penomoran otomatis bersifat lokal per browser, bukan nomor terpusat lintas cabang.
- PDF memakai dialog cetak browser. Pilih kertas A4 dan lakukan uji cetak.
- Ekspor Word menggunakan format `.doc` kompatibel Word, bukan `.docx` native.
- Saat ekspor Word, gambar di-embed sebagai data URI (jika asset berhasil dimuat); pastikan folder `assets/` ikut tersedia saat menjalankan aplikasi.
