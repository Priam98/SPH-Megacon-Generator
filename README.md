# Generator Surat Penawaran MEGACON PRECAST

## Struktur file
- `index.html` — struktur aplikasi dan template surat.
- `style.css` — gaya antarmuka, kop surat, tabel, tanda tangan, footer, dan aturan cetak.
- `app.js` — logika master produk, kalkulasi, penomoran lokal, riwayat, dan ekspor.
- `README.md` — petunjuk penggunaan.

## Menjalankan
1. Simpan ketiga file (`index.html`, `style.css`, `app.js`) di folder yang sama.
2. Buka `index.html` di Firefox, Chrome, atau Edge.
3. Isi identitas perusahaan dan logo dari menu Identitas Perusahaan.
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

## Batasan
- Data tersimpan di `localStorage` browser/perangkat, belum tersinkron antar pengguna.
- Penomoran otomatis bersifat lokal per browser, bukan nomor terpusat lintas cabang.
- PDF memakai dialog cetak browser. Pilih kertas A4 dan lakukan uji cetak.
- Ekspor Word menggunakan format `.doc` kompatibel Word, bukan `.docx` native.
