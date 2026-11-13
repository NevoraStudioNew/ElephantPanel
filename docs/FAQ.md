# FAQ

**Apakah ElephantPanel butuh root?**
Tidak. Runtime Alpine Linux berjalan lewat PRoot tanpa perlu akses root.

**Kenapa server dengan runtime alpine lambat saat pertama kali start?**
Wajar, karena saat itu package yang dibutuhkan (Node.js, Python, dependency npm/pip, dll) baru diunduh dan dipasang. Start berikutnya akan lebih cepat selama file tidak dihapus.

**Server saya mati sendiri padahal HP tidak dimatikan.**
Cek apakah Android membatasi app di latar belakang (battery optimization) untuk ElephantPanel. Matikan optimisasi baterai untuk app ini supaya service latar belakang tidak dibunuh sistem.

**Setelah HP restart, server saya otomatis hidup lagi — ini normal?**
Normal. Server yang sedang berjalan sebelum HP restart, app diupdate, atau service berhenti, akan dipulihkan otomatis oleh ElephantPanel.

**Egg K6 LOAD TEST keluar error "terminated with signal 4".**
Ini bug kompatibilitas antara program k6 (ditulis pakai bahasa Go) dengan lingkungan PRoot di sebagian chip Android, bukan kesalahan konfigurasi dari sisi user. Pastikan sudah pakai versi app terbaru dari tab Releases — perbaikan untuk masalah ini sudah dimasukkan ke catatan rilis versi terkait. Kalau masih muncul di app versi terbaru, laporkan lewat tab Issues beserta tipe chip/HP yang dipakai.

**Apakah egg K6 LOAD TEST boleh dipakai ke web orang lain?**
Tidak. Egg ini untuk menguji kapasitas web/API milik sendiri. Test-nya juga punya durasi yang jelas dan berhenti sendiri, bukan flood tanpa henti.

**Apakah source code ElephantPanel open source?**
Tidak. Lisensinya proprietary, lihat [LICENSE](../LICENSE). Repo ini hanya berisi rilis APK dan dokumentasi.
