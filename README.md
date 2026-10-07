# The Wedding — Emerald Velvet & Maroon

Undangan HTML mobile-first. Desain dibangun ulang mengikuti komposisi video acuan pengguna: tirai emerald sepanjang layar, amplop maroon miring dengan tepi scalloped dan wax seal emas, renda oval ivory, bunga bertekstur fotografis, panel maroon–emerald, dan cameo pengantin berselang kiri/kanan.

**Status: demo desain.** Nama, tanggal, waktu, orang tua, dan lokasi bukan data pernikahan sebenarnya. RSVP/ucapan hanya tersimpan di browser perangkat yang sama.

## Desain dan interaksi

- Tirai dan bunga bukan lagi gambar vektor datar. Material visual memakai aset raster lokal; sumber tekstur, renda, bunga, serta segel diolah dari video acuan yang diberikan pengguna. Tidak ada portrait, nama orang, nomor rekening, watermark platform, atau logo studio dalam aset undangan.
- Lapisan kertas amplop dibuat terpisah: belakang → surat/konten asli → kantong depan; flap membuka secara 3D dan seal terlepas. Semua bagian konten memiliki efek keluar amplop saat scroll pertama/menu diklik. Beranda pertama dibuka langsung dari cover agar tidak terjadi dua animasi amplop berturut-turut.
- Kedua mempelai tetap **ilustrasi SVG beranimasi, bukan foto orang**, dalam bingkai emas.
- Bunga bergoyang pelan, kain bergerak halus, kelopak melayang. Tombol jeda dan `prefers-reduced-motion` didukung.
- Nama tamu dari `?to=Bapak+Guntoro`; input menggunakan `textContent` dan dibatasi panjangnya.
- Countdown, kalender ICS berlabel CONTOH, ucapan localStorage dengan validasi dan fallback.
- Node form dipertahankan saat animasi/menu berubah sehingga draft tidak hilang.
- Tidak ada backend, analytics, atau kredensial.

## Menjalankan

Buka `index.html`, atau `python -m http.server 8000`. Tidak perlu build. CSS dan JavaScript berada di HTML, gambar lokal di `assets/`, font dari Google Fonts (dengan fallback).

## Personalisasi

Ubah nama, judul, tanggal, waktu, orang tua, alamat. Sinkronkan `eventTime` dan konten `calendar` di JavaScript. Data tanggal demo: 12 Desember 2027, WIB. Tambahkan peta setelah alamat benar diisi. Backend RSVP dan rekening hadiah sengaja tidak diisi dengan data rekaan.

## Publikasi

GitHub Pages: branch `main`, root `/`, `.nojekyll`. Versi sebelumnya tersimpan dalam riwayat Git. Video sumber dan alat QA tidak dipublikasikan.
