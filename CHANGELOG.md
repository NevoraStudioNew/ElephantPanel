# Changelog

Catatan perubahan lengkap tiap versi ada di deskripsi masing-masing rilis pada tab [Releases](../../releases) — isinya sama dengan `RELEASE_NOTES.md` yang berlaku saat versi itu dirilis.

File ini hanya ringkasan garis besar per topik, bukan pengganti catatan rilis resmi.

## K6 LOAD TEST
- Ditambahkan egg K6 LOAD TEST untuk load testing web/API sendiri pakai k6 (Grafana), k6 terpasang otomatis.
- Perbaikan crash "signal 4" saat menjalankan k6 di sebagian chip Android, dengan menonaktifkan beberapa pengecekan CPU Go yang tidak didukung PRoot.
