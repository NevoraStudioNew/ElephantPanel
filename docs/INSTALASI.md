# Instalasi

## Kebutuhan
- Android dengan arsitektur **arm64 (aarch64)** atau **x86_64**. Arsitektur lain (misal armv7 32-bit) belum didukung.
- Koneksi internet saat pertama kali memakai egg berjalur `alpine`, karena package/runtime diunduh saat itu.
- Penyimpanan cukup, terutama kalau menjalankan server yang butuh banyak dependency (Node.js, Python, Java, dll).

## Langkah install
1. Unduh file APK dari tab [Releases](../../releases) repo ini.
2. Karena bukan dari Play Store, Android akan menampilkan peringatan "sumber tidak dikenal" — izinkan untuk file ini saja.
3. Buka app, ikuti layar sambutan yang menjelaskan izin yang diminta.
4. Buat server pertama dari salah satu egg yang tersedia (lihat [EGG.md](EGG.md)).

## Izin yang diminta
App akan menjelaskan di layar sambutan kenapa tiap izin dibutuhkan (misalnya notifikasi untuk status server berjalan di latar belakang). Tidak ada izin yang diminta di luar yang dijelaskan di layar tersebut.

## Update
App mengecek update otomatis di latar belakang. Saat ada versi baru, akan muncul notifikasi dan pop up berisi catatan rilis. Update juga bisa diunduh manual dari tab [Releases](../../releases).
