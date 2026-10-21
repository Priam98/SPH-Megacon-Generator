# Generator Surat Penawaran — MEGACON PRECAST

Aplikasi HTML lokal untuk menyusun Surat Penawaran Harga (SPH), mengelola master harga, menghitung total, serta mengekspor dokumen ke PDF melalui dialog cetak dan `.doc` kompatibel Word.

## Peringatan penting
- Nomor surat dibuat pada browser/perangkat lokal, bukan server terpusat. Jangan gunakan sebagai nomor lintas cabang tanpa backend bersama.
- Data penawaran, master harga, logo, dan identitas perusahaan tersimpan di `localStorage`; gunakan ekspor cadangan JSON secara rutin.
- Harga dan data perusahaan sengaja kosong sampai diisi berdasarkan sumber resmi.


## Menjalankan
1. Ekstrak ZIP.
2. Buka `index.html` dengan Firefox, Chrome, atau Edge.
3. Isi identitas perusahaan dan unggah logo resmi di menu **Identitas Perusahaan**.
4. Tambahkan produk serta harga resmi di menu **Master Produk & Harga**.
5. Buat penawaran dan periksa pratinjau. Harga, data perusahaan, dan customer tidak diisi dengan data contoh.
6. Untuk PDF, klik **Cetak / Simpan PDF**, pilih kertas A4, skala 100% atau sesuaikan bila diperlukan, lalu aktifkan pencetakan latar/grafik latar agar ornamen biru tercetak.
7. Untuk Word, klik **Unduh Word (.doc)**. Format `.doc` berbasis HTML kompatibel Microsoft Word; ini belum `.docx` native.
8. Ekspor cadangan JSON berkala dari menu Riwayat.

## Acuan layout

Template menggunakan dokumen Word SPH sebagai acuan. Aset logo simbol, gambar stempel, dan ornamen footer diekstrak langsung dari dokumen Word dan ditanam di HTML agar tidak bergantung pada file aset eksternal. Kertas cetak ditetapkan A4. Data harga/customer tetap harus dimasukkan pengguna.

## Penyesuaian template
Pratinjau surat mengikuti susunan dokumen contoh yang diberikan: logo/nama di kiri, rincian perusahaan di kanan, garis pemisah, nomor dan perihal di kiri dengan tanggal di kanan, penerima/Attn, tabel lima kolom (Item no, Description, Unit Harga Per Satuan, Quantity, Jumlah), catatan, spesifikasi teknis, penutup, tanda tangan, serta ornamen footer geometris biru/abu-abu.

Field alamat dan kontak perusahaan saat ini tampil dalam satu blok sesuai data yang diisi pada Identitas Perusahaan. Untuk mereproduksi alamat/telepon/fax/email sebagai baris terpisah, isi kontak dengan susunan baris baru bila diperlukan.

## Batasan
- Data disimpan di `localStorage` browser/perangkat ini; tidak sinkron antarperangkat.
- Nomor otomatis hanya lokal browser, belum aman untuk penggunaan multiuser/antar cabang.
- PDF dicetak melalui dialog browser; lakukan uji cetak sebelum pengiriman resmi.
- Word adalah `.doc` berbasis HTML kompatibel Microsoft Word, bukan `.docx` native. Rendering dapat sedikit berbeda antarversi Word/LibreOffice; periksa hasil sebelum dikirim.
- Master harga kosong sampai pengguna memasukkan harga resmi.
- Ketentuan yang dimasukkan ke kolom Ketentuan Pengiriman, Syarat Pembayaran, dan Catatan Tambahan ditampilkan sebagai butir Catatan. Masa berlaku dihitung dari tanggal surat hingga tanggal berlaku sampai.
- Tidak ada logo, tanda tangan, stempel, harga, atau data perusahaan contoh yang dibuat otomatis.
