# Klinik Gunung - Sistem Manajemen Klinik Medis

[![Laravel](https://img.shields.io/badge/Laravel-12.x-FF2D20?style=for-the-badge\&logo=laravel)](https://laravel.com)
[![React](https://img.shields.io/badge/React-18.x-61DAFB?style=for-the-badge\&logo=react)](https://reactjs.org)
[![Inertia.js](https://img.shields.io/badge/Inertia.js-2.x-9553E9?style=for-the-badge\&logo=inertia)](https://inertiajs.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.x-38B2AC?style=for-the-badge\&logo=tailwind-css)](https://tailwindcss.com)

Sistem manajemen klinik medis lengkap yang dirancang untuk klinik di daerah pegunungan, menyediakan layanan kesehatan digital termasuk manajemen pasien, janji temu, pemeriksaan, dan rekam medis.

## ✨ Fitur Unggulan

### Layanan Medis Inti

* **Manajemen Pasien** - Pendaftaran dan pengelolaan profil pasien secara lengkap
* **Penjadwalan Janji Temu** - Sistem booking canggih dengan ketersediaan dokter
* **Rekam Medis** - Sistem EMR digital dengan riwayat pasien lengkap
* **Pemeriksaan Kesehatan** - Pemeriksaan offline dan online
* **Pemeriksaan Fisik** - Formulir dan dokumentasi digital

### 👥 Dasbor Multi-Peran

* **Panel Admin** - Administrasi sistem dan manajemen pengguna
* **Dasbor Dokter** - Konsultasi, rekam medis, dan janji temu
* **Antarmuka Paramedis** - Pemeriksaan dan manajemen skrining
* **Sistem Kasir** - Pemrosesan pembayaran dan transaksi
* **Laporan Manajer** - Analitik dan pelaporan menyeluruh
* **Portal Pasien** - Layanan mandiri untuk pasien

### 🔧 Fitur Lanjutan

* **Integrasi AI** - Google Gemini AI untuk bantuan medis dan analisis
* **Sistem QR Code** - Identifikasi digital dan akses cepat
* **Pembuatan PDF** - Laporan medis dan dokumentasi
* **Notifikasi Email** - Pemberitahuan dan konfirmasi otomatis
* **Hasil Skrining Otomatis ke Email** - Hasil skrining langsung dikirim ke email pasien dalam bentuk PDF
* **Manajemen Inventaris** - Pelacakan obat dan alat medis dengan sistem batch

  * **Sistem Stok Ganda**: Mengelola batch inventaris (`medicine_batches`) dan stok utama (`medicines`)
  * **Pengurangan Stok Otomatis**: Stok berkurang secara otomatis saat pasien membeli obat
  * **Pelacakan Batch**: Melacak batch obat beserta tanggal kadaluarsa dan pemasok
  * **Validasi Stok**: Mencegah penjualan melebihi stok tersedia
* **Platform Komunitas** - Komunitas pasien dan berbagi informasi kesehatan

### 🌐 Layanan Online

* **Pemeriksaan Jarak Jauh** - Penilaian kesehatan secara online
* **Telemedisin** - Konsultasi dan tindak lanjut digital
* **Pembayaran Online** - Proses pembayaran yang aman
* **Laporan Digital** - Sertifikat medis dan laporan yang dapat diunduh

## 🛠️ Teknologi yang Digunakan

### Backend

* **Laravel 12.x** - Framework PHP yang andal
* **MySQL/SQLite** - Sistem manajemen basis data
* **Sanctum** - Autentikasi dan keamanan API
* **Queue System** - Pemrosesan tugas latar belakang
* **Pembuatan PDF** - DomPDF untuk pembuatan dokumen

### Frontend

* **React 18.x** - Library JavaScript modern untuk UI
* **Inertia.js 2.x** - Rendering sisi server dengan pengalaman SPA
* **Tailwind CSS 3.x** - Framework CSS utility-first
* **Shadcn/UI** - Komponen UI yang cantik dan aksesibel
* **React Hook Form** - Pengelolaan form yang efisien
* **Radix UI** - Primitif UI yang aksesibel

### Alat Tambahan

* **Vite** - Alat build cepat
* **Google Gemini AI** - Bantuan medis bertenaga AI
* **Simple QR Code** - Pembuatan kode QR
* **Maatwebsite Excel** - Import/Export file Excel
* **Laravel Socialite** - Autentikasi OAuth

## 📋 Prasyarat

Pastikan Anda telah menginstal:

* **PHP >= 8.2** beserta ekstensi yang diperlukan
* **Composer** - Pengelola dependensi PHP
* **Node.js >= 18.x** dan **npm**
* **MySQL 8.x** atau **SQLite**
* **Git**

### Ekstensi PHP yang Dibutuhkan

```bash
php-curl
php-dom
php-fileinfo
php-filter
php-hash
php-mbstring
php-openssl
php-pcre
php-pdo
php-session
php-tokenizer
php-xml
php-zip
php-gd
```

## 🚀 Instalasi

### 1. Kloning Repository

```bash
git clone https://github.com/your-username/klinik-gunung.git
cd klinik-gunung
```

### 2. Instalasi Dependensi PHP

```bash
composer install
```

### 3. Instalasi Dependensi Node.js

```bash
npm install
```

### 4. Konfigurasi Lingkungan

```bash
cp .env.example .env
php artisan key:generate
```

### 5. Setup Database

```bash
# Untuk MySQL\mysql -u root -p
CREATE DATABASE klinik_gunung;
exit

# Untuk SQLite
touch database/database.sqlite
```

### 6. Konfigurasi File .env

Edit `.env` sesuai kebutuhan proyek Anda.

### 7. Migrasi dan Seeder Database

```bash
php artisan migrate
php artisan db:seed
```

### 8. Setup Storage

```bash
php artisan storage:link
chmod -R 775 storage bootstrap/cache
```

### 9. Build Frontend

```bash
npm run dev
# atau untuk production
npm run build
```

## 🏃‍ Menjalankan Aplikasi

### Mode Pengembangan

```bash
composer run dev
# atau jalankan manual:
php artisan serve
npm run dev
php artisan queue:work
```

### Mode Produksi

```bash
npm run build
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan queue:work --daemon
```

Akses aplikasi: `http://localhost:8000`

## 👤 Akun Pengguna Default

| Peran     | Email                                                           | Password | Akses                  |
| --------- | --------------------------------------------------------------- | -------- | ---------------------- |
| Admin     | [admin@klinikgunung.com](mailto:admin@klinikgunung.com)         | password | Akses penuh            |
| Dokter    | [doctor@klinikgunung.com](mailto:doctor@klinikgunung.com)       | password | Layanan medis          |
| Paramedis | [paramedic@klinikgunung.com](mailto:paramedic@klinikgunung.com) | password | Skrining kesehatan     |
| Kasir     | [cashier@klinikgunung.com](mailto:cashier@klinikgunung.com)     | password | Pembayaran & transaksi |
| Manajer   | [manager@klinikgunung.com](mailto:manager@klinikgunung.com)     | password | Laporan & analitik     |

## 📊 Arsitektur Sistem

```
Frontend <-> Backend <-> Database
React    <-> Laravel <-> MySQL
         <-> API, Queue, Mail, AI
```

## 🔐 Keamanan

* **Autentikasi** - Laravel Sanctum
* **Otorisasi** - Kontrol akses berbasis peran
* **Enkripsi Data** - Untuk data medis sensitif
* **Perlindungan CSRF**
* **Validasi Input** dan Upload Aman

## 📊 Optimisasi Performa

* **Index Database**, **Caching**, **Optimisasi Aset**
* **Lazy Loading**, **Queue** untuk proses berat
* **Manajemen Stok Efisien**

## 🥺 Pengujian

```bash
php artisan test
php artisan test --testsuite=Feature
```

## 📦 Deployment

Pastikan:

* `.env` disesuaikan untuk production
* Cache dan assets dibangun ulang
* Supervisor di-setup untuk queue

## 📞 Dukungan

* **Wiki**: [Dokumentasi](https://github.com/your-username/klinik-gunung/wiki)
* **Masalah Teknis**: [GitHub Issues](https://github.com/your-username/klinik-gunung/issues)
* **Email**: [support@klinikgunung.com](mailto:support@klinikgunung.com)

## 📄 Lisensi

Proyek ini dilisensikan di bawah MIT License - lihat file [LICENSE](LICENSE) untuk detailnya.
