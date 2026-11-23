# Silikon Nusa - proyek APK (Capacitor)

Isi:
- `www/index.html` : game (satu file, jalan offline)
- `assets/` : ikon dan splash (dipakai @capacitor/assets untuk membuat semua ukuran ikon Android)
- `capacitor.config.json`, `package.json` : konfigurasi Capacitor
- `.github/workflows/build-apk.yml` : GitHub Actions yang membangun APK otomatis

## Cara membuat APK lewat GitHub
1. Buat repository baru di GitHub, unggah SEMUA isi folder ini (termasuk folder `.github`).
2. Buka tab **Actions** > **Build APK** > **Run workflow** (atau otomatis saat push ke main).
3. Setelah hijau (sekitar 5-8 menit), buka run-nya, unduh artifact **silikon-nusa-apk**, ekstrak, pasang `app-debug.apk` di HP (izinkan "pasang dari sumber tidak dikenal").

## Mengubah game
Ganti `www/index.html` dengan versi baru lalu push; APK dibangun ulang.

## Catatan
- APK ini versi debug (bisa dipasang langsung). Untuk Google Play perlu build release bertanda tangan (keystore).
- Nama paket: `com.silikonnusa.game` (ubah di `capacitor.config.json` sebelum build pertama).
- Progres game tersimpan di penyimpanan lokal aplikasi dan tidak terbawa dari versi browser.
- Versi game: v28. Di aplikasi APK, tombol "Unduh .json" memakai unduhan biasa; bila gagal gunakan "Salin ke papan klip" lalu tempel di perangkat lain.
