
# Sistem Informasi Perpustakaan - REST API & Frontend

Proyek praktikum Pemrograman Berorientasi Objek (PBO), Program Studi Sistem Informasi, Universitas Tanjungpura.

## Identitas Mahasiswa

- **Nama:** Raihan Ikram Maulana
- **NIM:** H1101251049
- **Kelas:** A
- **Mata Kuliah:** Praktikum Pemrograman Berorientasi Objek

## Deskripsi Proyek

Sistem Informasi Perpustakaan merupakan aplikasi berbasis web yang dibangun dengan arsitektur frontend dan backend terpisah.

Backend menyediakan REST API menggunakan PHP, Composer, PDO, dan MySQL. Frontend menggunakan HTML, Tailwind CSS, serta JavaScript ES Module untuk mengakses API melalui HTTP dan JSON.

## Teknologi

| Teknologi | Kegunaan |
|---|---|
| PHP 8 | Backend dan REST API |
| Composer | Autoload PSR-4 |
| MySQL | Database |
| PDO | Koneksi dan query database |
| HTML | Struktur frontend |
| Tailwind CSS | Styling antarmuka |
| JavaScript ES Module | Interaksi dan integrasi API |
| cURL | Pengujian API |
| Postman | Pengujian HTTP Request |
| Git & GitHub | Version control dan dokumentasi |

## Fitur Aplikasi

### Backend
- REST API untuk data buku dan kategori.
- Operasi GET, POST, PUT, dan DELETE.
- Model, Repository, Service, dan Controller.
- Dependency Injection menggunakan Container.
- Front Controller dan Router.
- Validasi input dan penanganan error.
- Konfigurasi database melalui `.env`.
- CORS untuk komunikasi frontend dan backend.

### Frontend
- Dashboard statistik buku dan kategori.
- Daftar lima buku terbaru.
- Halaman manajemen buku.
- Form tambah dan edit buku.
- Halaman manajemen kategori.
- Form tambah dan edit kategori.
- Notifikasi menggunakan toast.
- Integrasi frontend dengan REST API.

**Catatan pengujian:** Penambahan buku melalui frontend dan penambahan kategori melalui frontend telah dibuktikan. Pengujian edit dan hapus kategori melalui frontend belum diverifikasi secara terpisah.

## Struktur Proyek

```text
pbo-lks-h1101251049-raihan-ikram-maulana/
│
├── README.md
├── .gitignore
│
├── rest-api-perpustakaan/
│   ├── public/
│   ├── src/
│   ├── database/
│   ├── tests/
│   ├── composer.json
│   └── .env.example
│
├── frontend-perpustakaan/
│   ├── index.html
│   ├── css/
│   └── js/
│       ├── app.js
│       ├── api.js
│       ├── config.js
│       ├── utils.js
│       └── pages/
│
├── screenshot-final/
│
├── pertemuan-01/
├── pertemuan-02/
├── pertemuan-03/
├── pertemuan-04/
├── pertemuan-05/
├── pertemuan-06/
└── pertemuan-07/
```

## Cara Menjalankan Proyek

### 1. Persiapan Backend

Masuk ke folder backend:

```bash
cd rest-api-perpustakaan
```

Salin `.env.example` menjadi `.env`, kemudian sesuaikan konfigurasi database MySQL.

Pastikan database `perpustakaan` sudah tersedia.

Jalankan Composer:

```bash
composer install
composer dump-autoload -o
```

Jalankan backend:

```bash
php -S localhost:8000 -t public
```

Backend tersedia di:

`http://localhost:8000`

### 2. Persiapan Frontend

Buka terminal kedua, lalu:

```bash
cd frontend-perpustakaan
```

Jalankan frontend:

```bash
php -S localhost:3000
```

Buka browser:

`http://localhost:3000`

**Penting:** Backend dan frontend harus berjalan bersamaan agar integrasi API berfungsi.

## Endpoint REST API

### Buku

| Method | Endpoint | Fungsi |
|---|---|---|
| GET | `/api/books` | Daftar buku |
| GET | `/api/books/{id}` | Detail buku |
| POST | `/api/books` | Tambah buku |
| PUT | `/api/books/{id}` | Ubah buku |
| DELETE | `/api/books/{id}` | Hapus buku |

### Kategori

| Method | Endpoint | Fungsi |
|---|---|---|
| GET | `/api/categories` | Daftar kategori |
| GET | `/api/categories/{id}` | Detail kategori |
| POST | `/api/categories` | Tambah kategori |
| PUT | `/api/categories/{id}` | Ubah kategori |
| DELETE | `/api/categories/{id}` | Hapus kategori |

## Dokumentasi Praktikum

### Pertemuan 1 — Setup & Database
- [Langkah 1](pertemuan-01/langkah-01.png)
- [Langkah 2](pertemuan-01/langkah-02.png)
- [Langkah 3](pertemuan-01/langkah-03.png)
- [Langkah 4](pertemuan-01/langkah-04.png)
- [Langkah 5](pertemuan-01/langkah-05.png)

### Pertemuan 2 — Core OOP & CRUD Buku
- [Langkah 6](pertemuan-02/langkah-06.png)
- [Langkah 7](pertemuan-02/langkah-07.png)
- [Langkah 8](pertemuan-02/langkah-08.png)
- [Langkah 9 — GET](pertemuan-02/langkah-09.png)
- [Langkah 9 — POST dan PUT](pertemuan-02/langkah-09-02.png)
- [Langkah 9 — DELETE](pertemuan-02/langkah-09-03.png)

### Pertemuan 3 — Validasi & Postman
- [Langkah 10](pertemuan-03/langkah-10.png)
- [Langkah 11](pertemuan-03/langkah-11.png)

### Pertemuan 4 — Automated Testing
- [Langkah 12 — Test 1 sampai 3](pertemuan-04/langkah-12.png)
- [Langkah 12 — Test 4 sampai 6](pertemuan-04/langkah-12-02.png)

### Pertemuan 5 — CRUD Kategori
- [Langkah 13](pertemuan-05/langkah-13.png)
- [Langkah 14](pertemuan-05/langkah-14.png)
- [Langkah 15 — POST dan PUT](pertemuan-05/langkah-15.png)
- [Langkah 15 — DELETE dan Validasi](pertemuan-05/langkah-15-02.png)

### Pertemuan 6 — Frontend
- [Langkah 16 — CORS](pertemuan-06/langkah-16.png)
- [Langkah 17 — Setup Frontend](pertemuan-06/langkah-17.png)
- [Langkah 18 — Dashboard](pertemuan-06/langkah-18.png)
- [Langkah 18 — Tabel dan Modal Buku](pertemuan-06/langkah-18-02.png)
- [Langkah 18 — Tambah Buku](pertemuan-06/langkah-18-03.png)

### Pertemuan 7 — Integrasi & Finalisasi
- [Langkah 19 — Halaman Kategori](pertemuan-07/langkah-19.png)
- [Langkah 19 — Backend](pertemuan-07/langkah-19-02.png)
- [Langkah 19 — Frontend](pertemuan-07/langkah-19-03.png)
- Langkah 20 — Finalisasi repository

## Screenshot Aplikasi Final

- [Dashboard](screenshot-final/dashboard.png)
- [Halaman Buku](screenshot-final/halaman-buku.png)
- [Halaman Kategori](screenshot-final/halaman-kategori.png)

## Repository

GitHub: https://github.com/RaihanIkram/pbo-lks-h1101251049-raihan-ikram-maulana

---

Dokumentasi disusun sebagai bagian dari penyelesaian Lembar Kerja Mahasiswa Praktikum Pemrograman Berorientasi Objek.

