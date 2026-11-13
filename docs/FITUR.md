# Penjelasan Fitur

## Manajemen server
ElephantPanel bisa menjalankan banyak server sekaligus dalam satu app, mirip panel Pterodactyl tapi semuanya berjalan lokal di HP. Tiap server punya nama unik, dan bisa dihapus atau diduplikat (termasuk file-filenya) kapan saja.

## Console / shell terminal
Tiap server punya console sendiri berbasis emulator terminal asli (PTY), bukan sekadar kotak log. Mendukung:
- Extra keys (tombol Ctrl, Tab, panah, dll di atas keyboard) untuk kebutuhan shell
- Multi-sesi, jadi bisa buka lebih dari satu shell ke server yang sama
- Dua runtime: **native** (shell Android biasa, ringan) dan **alpine** (Alpine Linux penuh lewat PRoot, bisa `apk add` package seperti Node.js, Python, Java, dll)

## Egg / template server
Server baru dibuat dari "egg" — template siap pakai yang sudah termasuk runtime, perintah start, file awal, dan variable environment. Daftar lengkap egg ada di [EGG.md](EGG.md).

## File manager
File manager penuh di tiap server, termasuk:
- Unarchive (ekstrak) dan buat file zip
- Salin, potong, tempel, duplikat file/folder
- Lihat info file dan cari file di dalam server
- Preview file text/gambar langsung di app

## Variables editor
Variabel environment server (seperti token bot, port, target URL) bisa diedit lewat tab tersendiri tanpa perlu edit file manual, mirip tab "Startup" di Pterodactyl.

## Grafik pemakaian sumber daya
Tiap server menampilkan grafik pemakaian CPU, RAM, dan disk secara berkala, supaya kelihatan kalau server mulai berat.

## Backup & schedule
- Backup server bisa dikunci (lock) supaya tidak kehapus tidak sengaja, dan ada rotasi otomatis supaya backup lama tidak menumpuk
- Jadwal (schedule) bisa dipakai untuk menjalankan aksi tertentu secara berkala

## Activity log
Semua aksi penting (start/stop server, edit variable, hapus file, dll) tercatat di activity log per server, buat ketahuan kalau ada perubahan tak terduga.

## PIN panel & service latar belakang
App bisa dikunci pakai PIN. Server tetap berjalan di latar belakang lewat Android foreground service, dan kalau HP di-reboot atau app diupdate, server yang tadinya berjalan akan otomatis dinyalakan lagi.

## Update otomatis
App mengecek update secara berkala di latar belakang dan memberi notifikasi. Saat ada versi baru, muncul pop up berisi catatan rilis (changelog) sebelum user memilih update atau tidak.
