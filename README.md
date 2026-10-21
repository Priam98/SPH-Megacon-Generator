# SPH MEGACON PRECAST Generator

## File
- `index.html` — UI aplikasi
- `style.css` — layout dan cetak
- `app.js` — kalkulasi, master produk, penomoran, dokumen
- Logo, stempel, dan footer referensi Word tertanam sebagai data URI di `app.js`.

## Kop permanen
Identitas kop ditetapkan pada konstanta `COMPANY` di `app.js`. Form untuk nama perusahaan, alamat, kontak, website, dan upload logo sudah dihapus. Untuk mengubah identitas resmi, edit konstanta `COMPANY` dan aset yang tertanam di `app.js`.

## Menjalankan
Letakkan ketiga file dalam folder yang sama dan buka `index.html` di browser. Isi master produk dan harga aktual sebelum membuat penawaran.

## Catatan
- Data tersimpan pada `localStorage` browser ini.
- Nomor surat otomatis hanya lokal per browser/perangkat, belum terpusat antarcabang.
- PDF memakai dialog cetak browser. Pilih kertas A4.
- Ekspor Word menggunakan `.doc` kompatibel Word, bukan `.docx` native.
