# Praktikum 05 – Web Service Katalog Buku

## 1. Identitas Praktikum

| Keterangan | Informasi |
|---|---|
| Nama | Syariah Nor Alfisah |
| NIM | 240104040130 |
| Program Studi | Teknologi Informasi |
| Mata Kuliah | Web Service Engineering |
| Proyek | Praktikum 05 – Web Service Katalog Buku |
| Teknologi | Node.js, Express.js, OpenAPI, Swagger UI |

## 2. Deskripsi Proyek

Web Service Katalog Buku merupakan aplikasi layanan berbasis REST API yang digunakan untuk mengelola data buku. Aplikasi menyediakan fitur menampilkan, mencari, menambahkan, mengubah, dan menghapus data buku.

Proyek ini dibuat menggunakan Node.js dan Express.js. Dokumentasi API disusun menggunakan OpenAPI dan ditampilkan melalui Swagger UI sehingga endpoint dapat dipahami dan diuji dengan lebih mudah.

Data buku disimpan sementara menggunakan penyimpanan dalam memori (*in-memory*), sehingga data tambahan akan kembali ke kondisi awal ketika server dijalankan ulang.

## 3. Fitur Aplikasi

- Menampilkan seluruh data buku.
- Mencari buku berdasarkan judul.
- Menampilkan detail buku berdasarkan ID.
- Menambahkan data buku baru.
- Mengubah data buku.
- Menghapus data buku.
- Menampilkan dokumentasi API menggunakan Swagger UI.
- Menyediakan respons kesalahan dengan kode dan pesan yang jelas.

## 4. Teknologi yang Digunakan

| Teknologi | Kegunaan |
|---|---|
| Node.js | Menjalankan aplikasi JavaScript di sisi server. |
| Express.js | Membuat dan mengatur REST API. |
| OpenAPI 3.1.0 | Menyusun kontrak dan dokumentasi API. |
| Swagger UI | Menampilkan dan menguji endpoint API. |
| VS Code | Menulis dan mengelola kode program. |

## 5. Struktur Folder

```text
praktikum05-webservice/
├── src/
│   ├── errors.cjs
│   ├── buku.repository.cjs
│   ├── buku.service.cjs
│   ├── buku.controller.cjs
│   └── buku.routes.cjs
├── scripts/
│   └── generate-openapi.cjs
├── docs/
│   └── openapi.json
├── samples/
│   ├── buku-baru.json
│   ├── buku-ubah.json
│   ├── buku-salah-tipe.json
│   ├── buku-parsial.json
│   └── json-rusak.txt
├── app.cjs
├── server.cjs
├── client.cjs
├── package.json
└── README.md
```

## 6. Daftar Endpoint API

| Metode | Endpoint | Fungsi |
|---|---|---|
| GET | `/api/buku` | Menampilkan seluruh buku. |
| GET | `/api/buku?q=kotlin` | Mencari buku berdasarkan judul. |
| GET | `/api/buku/:id` | Menampilkan detail buku. |
| POST | `/api/buku` | Menambahkan buku baru. |
| PUT | `/api/buku/:id` | Mengubah data buku. |
| DELETE | `/api/buku/:id` | Menghapus buku. |

## 7. Format Data Buku

Contoh data yang digunakan:

```json
{
  "judul": "Belajar API dengan Express",
  "tersedia": true
}
```

Keterangan:
- `id`: Dibuat otomatis oleh server.
- `judul`: Nama atau judul buku berupa teks.
- `tersedia`: Status ketersediaan buku (`true` atau `false`).

## 8. Cara Menjalankan Proyek

### A. Persiapan

Pastikan Node.js dan npm sudah terpasang.

Periksa melalui terminal:

```bash
node -v
npm -v
```

### B. Instalasi Dependensi

Jalankan perintah:

```bash
npm ci
```

### C. Membuat Dokumentasi OpenAPI

Jalankan:

```bash
npm run docs
```

Perintah tersebut akan menghasilkan atau memperbarui file `docs/openapi.json`.

### D. Menjalankan Server

Jalankan:

```bash
npm start
```

Jika berhasil, server berjalan pada:

```text
http://127.0.0.1:3200
```

## 9. Mengakses API dan Dokumentasi

| Keperluan | Alamat |
|---|---|
| Daftar buku | http://127.0.0.1:3200/api/buku |
| Detail buku pertama | http://127.0.0.1:3200/api/buku/1 |
| Dokumentasi Swagger UI | http://127.0.0.1:3200/docs/ |
| File OpenAPI | http://127.0.0.1:3200/openapi.json |

## 10. Pengujian API

Pengujian dapat dilakukan melalui Swagger UI maupun file `client.cjs`.

Contoh pengujian menggunakan terminal:

```bash
node client.cjs GET /api/buku
node client.cjs GET /api/buku/1
node client.cjs GET "/api/buku?q=kotlin"
```

Contoh menambahkan buku:

```bash
node client.cjs POST /api/buku samples/buku-baru.json
```

Pengujian lainnya dapat dilakukan menggunakan metode PUT dan DELETE.

## 11. Penanganan Kesalahan

Aplikasi menyediakan beberapa respons kesalahan:

| Kode HTTP | Keterangan |
|---|---|
| 400 | Permintaan atau data tidak valid. |
| 404 | Data buku atau endpoint tidak ditemukan. |
| 413 | Ukuran data melebihi batas. |
| 415 | Format media tidak didukung. |
| 500 | Terjadi kesalahan internal server. |

## 12. Catatan

- Server menggunakan alamat `127.0.0.1` dengan port `3200`.
- Data tambahan disimpan sementara di memori.
- Data akan kembali ke kondisi awal setelah server dimulai ulang.
- Dokumentasi API dapat diperbarui melalui perintah `npm run docs`.
- Swagger UI digunakan untuk melihat dan mencoba endpoint API.

## 13. Kesimpulan

Praktikum 05 menghasilkan Web Service Katalog Buku berbasis REST API menggunakan Node.js dan Express.js. Aplikasi memiliki fitur pengelolaan data buku serta dokumentasi OpenAPI yang dapat diakses melalui Swagger UI. Proyek ini membantu memahami perancangan endpoint, pembagian tanggung jawab program, pengujian API, dan dokumentasi layanan web.