# Generator Surat Penawaran — template MEGACON PRECAST

## Menjalankan
1. Ekstrak ZIP.
2. Buka `index.html` dengan Firefox, Chrome, atau Edge.
3. Isi identitas perusahaan dan unggah logo resmi di menu **Identitas Perusahaan**.
4. Tambahkan produk serta harga resmi di menu **Master Produk & Harga**.
5. Buat penawaran dan periksa pratinjau. Harga, data perusahaan, dan customer tidak diisi dengan data contoh.
6. Untuk PDF, klik **Cetak / Simpan PDF**, pilih kertas A4, skala 100% atau sesuaikan bila diperlukan, lalu aktifkan pencetakan latar/grafik latar agar ornamen biru tercetak.
7. Untuk Word, klik **Unduh Word (.doc)**. Format `.doc` berbasis HTML kompatibel Microsoft Word; ini belum `.docx` native.
8. Ekspor cadangan JSON berkala dari menu Riwayat.

## Penyesuaian template
Pratinjau surat mengikuti susunan dokumen contoh yang diberikan: logo/nama di kiri, rincian perusahaan di kanan, garis pemisah, nomor dan perihal di kiri dengan tanggal di kanan, penerima/Attn, tabel lima kolom (Item no, Description, Unit Harga Per Satuan, Quantity, Jumlah), catatan, spesifikasi teknis, penutup, tanda tangan, serta ornamen footer geometris biru/abu-abu.

Field alamat dan kontak perusahaan saat ini tampil dalam satu blok sesuai data yang diisi pada Identitas Perusahaan. Untuk mereproduksi alamat/telepon/fax/email sebagai baris terpisah, isi kontak dengan susunan baris baru bila diperlukan.

## Batasan
- Data disimpan di `localStorage` browser/perangkat ini; tidak sinkron antarperangkat.
- Nomor otomatis hanya lokal browser, belum aman untuk penggunaan multiuser/antar cabang.
- PDF dicetak melalui dialog browser; lakukan uji cetak sebelum pengiriman resmi.
- Word adalah `.doc` kompatibel, bukan `.docx` native.
- Master harga kosong sampai pengguna memasukkan harga resmi.
- Ketentuan yang dimasukkan ke kolom Ketentuan Pengiriman, Syarat Pembayaran, dan Catatan Tambahan ditampilkan sebagai butir Catatan. Masa berlaku dihitung dari tanggal surat hingga tanggal berlaku sampai.
- Tidak ada logo, tanda tangan, stempel, harga, atau data perusahaan contoh yang dibuat otomatis.
