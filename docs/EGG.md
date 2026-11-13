# Daftar Egg / Template Server

Egg adalah template siap pakai saat membuat server baru: sudah termasuk runtime, perintah start, file awal (kalau ada), dan variable default. Semua bisa diedit lagi setelah server dibuat.

| Egg | Runtime | Port default | Keterangan |
|---|---|---|---|
| DEMO | native | - | Contoh heartbeat sederhana untuk coba-coba panel |
| WA BOT | alpine | - | Bot WhatsApp pakai Baileys, login dengan pairing code |
| DISCORD BOT | alpine | - | Bot Discord pakai discord.js v14. Isi variable `DISCORD_TOKEN` setelah dibuat |
| NEXT.JS | alpine | 3000 | Menjalankan project Next.js yang diupload sendiri ke folder server |
| EXPRESS API | alpine | 3000 | REST API Node.js + Express, siap jalan |
| NODE | alpine | - | Node.js generik, untuk project Node.js sendiri |
| FLASK | alpine | 5000 | Web/API Python Flask |
| PYTHON | alpine | 8080 | Python generik, default jalan sebagai file server sederhana |
| WEB | alpine | 8080 | Hosting halaman statis (HTML/CSS/JS) dari folder `www` |
| MINECRAFT PAPER | alpine | 25565 | Server Minecraft Java (PaperMC), jar terbaru diunduh otomatis saat pertama start |
| K6 LOAD TEST | alpine | - | Load testing pakai k6 (Grafana) untuk web/API **milik sendiri**. k6 dipasang otomatis sekali lalu test berjalan sesuai skenario di `test.js` dan berhenti sendiri — bukan flood tanpa henti. Isi variable `TARGET_URL` dengan alamat yang mau ditest |
| SHELL | native | - | Shell polos tanpa template apa-apa |

## Catatan soal egg ALPINE
Egg dengan runtime `alpine` berjalan di dalam Alpine Linux lewat PRoot, jadi bisa pasang package tambahan sendiri lewat `apk add`. Perlu koneksi internet di HP saat instalasi package pertama kali.

## Catatan soal K6 LOAD TEST
Egg ini dibuat khusus untuk menguji kapasitas web/API milik sendiri secara terukur (ada durasi test yang jelas, bukan menembak terus-menerus). Jangan dipakai untuk menguji server milik orang lain tanpa izin.
