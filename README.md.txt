# WargaHubP04

**Aplikasi Laporan Lingkungan Berbasis Android**

## 1. Identitas Praktikum

| Keterangan | Informasi |
|---|---|
| Nama | Syariah Nor Alfisah |
| NIM | 240104040130 |
| Program Studi | Teknologi Informasi |
| Mata Kuliah | Pemrograman Mobile |
| Proyek | Praktikum 04 |
| Nama Aplikasi | WargaHubP04 |
| Package | `id.antasari.p04.wargahub` |

## 2. Deskripsi Aplikasi

WargaHubP04 merupakan aplikasi Android sederhana yang dirancang untuk menampilkan informasi laporan lingkungan. Aplikasi ini memiliki beberapa halaman, yaitu Beranda, Daftar Laporan, dan Detail Laporan.

Aplikasi menyediakan 15 data laporan contoh yang dapat dipilih untuk melihat informasi lebih lengkap. Selain itu, terdapat fitur pengujian daftar kosong dan pemulihan data contoh untuk menguji perubahan tampilan aplikasi.

Data yang digunakan masih berupa data simulasi dan belum terhubung dengan database maupun server.

## 3. Fitur Aplikasi

1. **Beranda:** Menampilkan halaman awal aplikasi dan tombol menuju daftar laporan.
2. **Daftar Laporan:** Menampilkan 15 data laporan contoh menggunakan RecyclerView.
3. **Detail Laporan:** Menampilkan ID, judul, kategori, deskripsi, dan status laporan yang dipilih.
4. **Uji Daftar Kosong:** Mengubah tampilan daftar menjadi kondisi kosong.
5. **Tampilkan Data Contoh:** Mengembalikan daftar laporan menjadi 15 data contoh.
6. **Navigasi:** Mendukung navigasi menggunakan Up toolbar dan Back sistem Android.
7. **Rotasi Layar:** Menguji kemampuan aplikasi mempertahankan kondisi tampilan saat perangkat diputar.

## 4. Teknologi yang Digunakan

- Android Studio
- Bahasa pemrograman Kotlin
- XML Layout
- ViewBinding
- Fragment
- RecyclerView
- Navigation Component
- ConstraintLayout
- Android SDK

## 5. Struktur Proyek

```text
WargaHubP04/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/id/antasari/p04/wargahub/
│           │   ├── adapter/
│           │   │   └── LaporanAdapter.kt
│           │   │
│           │   ├── data/
│           │   │   ├── Laporan.kt
│           │   │   └── LaporanContoh.kt
│           │   │
│           │   ├── ui/
│           │   │   ├── HomeFragment.kt
│           │   │   ├── ListFragment.kt
│           │   │   └── DetailFragment.kt
│           │   │
│           │   └── MainActivity.kt
│           │
│           └── res/
│               ├── layout/
│               ├── navigation/
│               └── values/
│
├── docs/
├── screenshots/
├── README.md
├── build.gradle.kts
└── settings.gradle.kts
```

## 6. Persyaratan Sistem

- Android Studio.
- Android SDK Platform 37.
- Gradle Wrapper bawaan proyek.
- Emulator Android atau perangkat Android fisik.
- Minimum Android SDK: API 26.

## 7. Cara Menjalankan Aplikasi

1. Buka Android Studio.
2. Pilih **Open**.
3. Cari dan buka folder proyek `WargaHubP04`.
4. Tunggu proses Gradle Sync sampai selesai.
5. Pastikan konfigurasi aplikasi menggunakan `compileSdk = 37`.
6. Pilih emulator atau perangkat Android.
7. Pilih konfigurasi `app`.
8. Tekan tombol **Run (▶)**.
9. Tunggu proses instalasi sampai aplikasi terbuka.

### Build melalui Terminal

Buka Terminal Android Studio pada direktori utama proyek, kemudian jalankan:

```powershell
.\gradlew.bat assembleDebug
```

Jika proses berhasil, akan muncul pesan:

```text
BUILD SUCCESSFUL
```

File APK debug dapat ditemukan pada:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## 8. Skenario Pengujian

| No. | Skenario Pengujian | Hasil |
|---|---|---|
| 1 | Build aplikasi | Isi hasil aktual |
| 2 | Menampilkan Beranda | Isi hasil aktual |
| 3 | Menampilkan 15 laporan | Isi hasil aktual |
| 4 | Membuka Detail Laporan | Isi hasil aktual |
| 5 | Menguji daftar kosong | Isi hasil aktual |
| 6 | Memulihkan data contoh | Isi hasil aktual |
| 7 | Menguji navigasi Up toolbar | Isi hasil aktual |
| 8 | Menguji navigasi Back sistem | Isi hasil aktual |
| 9 | Menguji rotasi perangkat | Isi hasil aktual |
| 10 | Menguji ukuran font | Isi hasil aktual |
| 11 | Menguji tampilan landscape | Isi hasil aktual |
| 12 | Menguji TalkBack | Isi hasil aktual |
| 13 | Pengujian bersama pengguna | Isi hasil aktual |

## 9. Dokumentasi Screenshot

Bukti pengujian aplikasi disimpan pada folder `screenshots`.

Dokumentasi yang disiapkan meliputi:

- Tampilan Beranda.
- Tampilan Daftar Laporan.
- Tampilan Detail Laporan.
- Kondisi daftar kosong.
- Pemulihan data contoh.
- Navigasi Up dan Back.
- Pengujian rotasi layar.
- Pengujian ukuran font.
- Tampilan landscape dan layar kecil.
- Pengujian aksesibilitas.
- Dokumentasi perbaikan UX sebelum dan sesudah.

## 10. Kendala dan Catatan

Pengujian aplikasi dilakukan menggunakan emulator Android. Beberapa pengujian dapat mengalami kendala yang bergantung pada konfigurasi perangkat, ukuran layar, dan ketersediaan fitur aksesibilitas.

Hasil pengujian dan kendala yang ditemukan dicatat berdasarkan kondisi aktual selama praktikum berlangsung.

## 11. Kesimpulan

WargaHubP04 merupakan aplikasi Android sederhana yang menerapkan penggunaan Activity, Fragment, RecyclerView, ViewBinding, dan Navigation Component. Aplikasi ini dibuat untuk memahami pengelolaan tampilan, perpindahan halaman, pengolahan data contoh, serta pengujian pengalaman pengguna pada perangkat Android.

---

**Praktikum 04 – Pemrograman Mobile**  
**Teknologi Informasi – Universitas Islam Negeri Antasari Banjarmasin**