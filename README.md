# The Wedding — Emerald Velvet & Maroon

Undangan HTML mobile-first untuk **Aditya Puja Kisdinata & Pixel Cindy Laura Deffana** (29.11.2026). Tirai emerald sepanjang layar, amplop maroon berscalloped + wax seal emas, renda oval ivory, bunga fotografis, panel maroon–emerald, dan cameo pengantin berselang kiri/kanan.

## Desain dan interaksi

- Material visual memakai aset raster lokal (tekstur, renda, bunga, segel, foto pengantin) — tanpa portrait orang sungguhan di cameo, tanpa watermark platform/logo studio.
- Amplop pembuka: belakang → surat → kantong depan; flap membuka 3D dan seal terlepas. Setiap bagian konten juga dibungkus amplop tersendiri (letter scene) yang terbuka saat scroll pertama / menu diklik.
- Alur bagian: Beranda → Pembuka (doa) → Mempelai → Save the date → **Love Story (timeline)** → Acara/lokasi → RSVP & Ucapan → Penutup.
- Bagian **Our Love Story** berupa timeline 4 titik (2023 The First Meeting, 2026 We Found Each Other Again, The Proposal, And Now…) + kutipan penutup.
- Bunga bergoyang pelan, kain bergerak halus, kelopak melayang. Tombol jeda dan `prefers-reduced-motion` didukung.
- Musik latar `assets/bgm.mp3` ("Nothing's Gonna Change My Love for You" – George Benson) dengan tombol putar/jeda melayang di pojok kanan atas.
- Nama tamu dari `?to=Bapak+Guntoro`; input memakai `textContent`, dibatasi panjangnya.
- Countdown, kalender ICS, ucapan `localStorage` dengan validasi dan fallback.
- Tidak ada backend, analytics, atau kredensial.

## Menjalankan

Buka `index.html`, atau `python -m http.server 8000`. Tidak perlu build. CSS terpisah di `style.css`, JavaScript inline di `index.html`, gambar di `assets/`, font dari Google Fonts (dengan fallback).

## Personalisasi

Ubah nama, judul, tanggal, waktu, orang tua, alamat, dan isi timeline Love Story. Sinkronkan `eventTime` dan konten `calendar` di JavaScript. Tautan peta ditambahkan setelah alamat asli diisi. Backend RSVP dan rekening hadiah sengaja tidak diisi dengan data rekaan.

## Publikasi

GitHub Pages: branch `main`, root `/`, `.nojekyll`. Versi sebelumnya tersimpan dalam riwayat Git. Video sumber dan alat QA tidak dipublikasikan.