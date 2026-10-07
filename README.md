# Sepucuk Janji — Drapery Collection

Undangan pernikahan HTML statis, mobile-first. Desain maroon, emerald green, ivory, dan antique gold. Dibuat sebagai **demo desain**: nama, orang tua, tanggal, waktu, dan lokasi belum merupakan data pengantin sebenarnya.

## Desain

- Amplop CSS dengan segel emas, flap 3D, dan surat yang keluar saat dibuka.
- Drapery SVG orisinal dengan lipatan kain, tieback, tassel, dan gerak pelan.
- Ilustrasi pengantin SVG beranimasi; **tidak menggunakan foto pengantin atau foto stok**.
- Nama tamu dinamis: `?to=Bapak+Guntoro`.
- Countdown, unduh kalender ICS dengan label CONTOH, dan navigasi bagian.
- Form RSVP/ucapan merupakan pratinjau lokal: hanya tersimpan di browser perangkat yang sama, bukan database publik dan bukan konfirmasi kepada pengantin.
- Hormati pengaturan `prefers-reduced-motion`.

## Menjalankan

Buka `index.html` langsung, atau jalankan:

```sh
python -m http.server 8000
```

Tidak ada build step. CSS, JavaScript, dan ilustrasi berada di `index.html`. Font memakai Google Fonts dengan fallback lokal. Tidak ada analytics, kredensial, foto, atau backend.

## Mengisi data sebenarnya

Edit nama singkat, nama lengkap, nama orang tua, monogram pada segel/surat, judul halaman, tanggal, waktu, dan alamat di HTML. Sinkronkan `eventTime` dan isi `calendar` di JavaScript saat mengubah tanggal. Tanggal demo: 12 Desember 2027, waktu WIB. Jangan menghapus penanda demo sebelum seluruh data telah diganti dan diverifikasi. Isi lokasi yang benar sebelum menambahkan tombol peta.

Backend RSVP dan rekening hadiah sengaja tidak diisi dengan data rekaan.

## Publikasi

GitHub Pages dari branch `main`, direktori root `/`. `.nojekyll` disertakan. Repo ini terpisah dari undangan sebelumnya.
