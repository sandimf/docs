# Klinik Gunung - Sistem Manajemen Klinik Medis

Sistem manajemen klinik medis yang dirancang untuk kebutuhan klinik di daerah pegunungan. Sistem ini menyediakan layanan digital untuk manajemen pasien, penjadwalan janji temu, pemeriksaan kesehatan, rekam medis, pembayaran, komunitas, dan pelaporan.

## Fitur Utama

### Layanan Medis
- Manajemen data pasien
- Penjadwalan janji temu dengan dokter
- Rekam medis elektronik (EMR)
- Pemeriksaan kesehatan offline dan online
- Pemeriksaan fisik digital

### Dasbor Multi-Peran
- Panel administrator untuk manajemen sistem
- Dasbor dokter untuk konsultasi dan rekam medis
- Antarmuka paramedis untuk skrining dan pemeriksaan
- Sistem kasir untuk pembayaran dan transaksi
- Laporan manajer untuk analitik dan pelaporan
- Portal pasien untuk layanan mandiri

### Fitur Lanjutan
- Integrasi AI untuk bantuan medis
- Sistem QR Code untuk identifikasi dan akses cepat
- Pembuatan laporan PDF
- Notifikasi email otomatis
- Hasil skrining otomatis ke email pasien
- Manajemen inventaris obat dan alat medis
- Platform komunitas pasien

### Layanan Online
- Pemeriksaan kesehatan jarak jauh
- Telemedisin
- Pembayaran online
- Laporan digital yang dapat diunduh

## Teknologi yang Digunakan

### Backend
- Laravel 12.x (PHP)
- MySQL/SQLite
- Laravel Sanctum untuk autentikasi
- Queue system untuk pemrosesan latar belakang
- DomPDF untuk pembuatan dokumen PDF

### Frontend
- React 18.x
- Inertia.js 2.x
- Tailwind CSS 3.x
- Shadcn/UI dan Radix UI
- React Hook Form

### Alat Tambahan
- Vite untuk build frontend
- Google Gemini AI
- Simple QR Code
- Maatwebsite Excel untuk import/export
- Laravel Socialite untuk autentikasi OAuth

## Prasyarat

- PHP >= 8.2 beserta ekstensi yang diperlukan
- Composer
- Node.js >= 18.x dan npm
- MySQL 8.x atau SQLite
- Git

### Ekstensi PHP yang Dibutuhkan
- php-curl
- php-dom
- php-fileinfo
- php-filter
- php-hash
- php-mbstring
- php-openssl
- php-pcre
- php-pdo
- php-session
- php-tokenizer
- php-xml
- php-zip
- php-gd

## Struktur Direktori dan Penjelasan Setup

### 1. Direktori `app/`
Berisi seluruh kode aplikasi backend (Laravel), termasuk:
- `Http/Controllers/` : Pengendali (controller) untuk setiap fitur dan endpoint
- `Models/` : Model data untuk ORM Eloquent
- `Services/` : Layanan bisnis dan logika aplikasi
- `Jobs/` : Tugas latar belakang (queue)
- `Mail/` : Template dan logika email
- `Events/` : Event aplikasi
- `Repositories/` : Abstraksi akses data
- `Helpers/` : Fungsi bantu

### 2. Direktori `config/`
Berisi seluruh file konfigurasi aplikasi, seperti:
- `app.php` : Konfigurasi utama aplikasi
- `auth.php` : Pengaturan autentikasi
- `database.php` : Pengaturan koneksi database
- `mail.php` : Pengaturan email
- `services.php` : Integrasi layanan eksternal
- File konfigurasi lain untuk cache, queue, session, dan lain-lain

### 3. Direktori `database/`
Berisi:
- `migrations/` : File migrasi skema database
- `seeders/` : Seeder data awal
- `factories/` : Factory untuk pembuatan data dummy
- `database.sqlite` : File database SQLite (jika digunakan)

### 4. Direktori `go-realtime-server/`
Berisi server realtime berbasis Go untuk kebutuhan notifikasi dan komunikasi realtime. File utama:
- `main.go` : Implementasi server realtime
- `go.mod` dan `go.sum` : Manajemen dependensi Go

### 5. Direktori `routes/`
Berisi seluruh definisi rute aplikasi Laravel:
- `web.php` : Rute utama aplikasi web
- `api.php` : Rute untuk API
- `auth.php` : Rute autentikasi (login, registrasi, reset password, dsb)
- File rute lain untuk modul admin, pasien, kasir, manajer, komunitas, dan lain-lain

## Langkah Instalasi dan Setup

1. **Kloning Repository**
   ```bash
   git clone https://github.com/your-username/klinik-gunung.git
   cd klinik-gunung
   ```
2. **Instalasi Dependensi PHP**
   ```bash
   composer install
   ```
3. **Instalasi Dependensi Node.js**
   ```bash
   npm install
   ```
4. **Konfigurasi Lingkungan**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
5. **Setup Database**
   - Untuk MySQL:
     ```bash
     # Masuk ke MySQL dan buat database
     CREATE DATABASE klinik_gunung;
     exit
     ```
   - Untuk SQLite:
     ```bash
     touch database/database.sqlite
     ```
6. **Edit file `.env`**
   - Sesuaikan konfigurasi database, mail, dan lainnya sesuai kebutuhan.
7. **Migrasi dan Seeder Database**
   ```bash
   php artisan migrate
   php artisan db:seed
   ```
8. **Setup Storage**
   ```bash
   php artisan storage:link
   chmod -R 775 storage bootstrap/cache
   ```
9. **Build Frontend**
   ```bash
   npm run dev
   # Untuk production
   npm run build
   ```
10. **Menjalankan Aplikasi**
    - Mode pengembangan:
      ```bash
      php artisan serve
      npm run dev
      php artisan queue:work
      ```
    - Mode produksi:
      ```bash
      npm run build
      php artisan config:cache
      php artisan route:cache
      php artisan view:cache
      php artisan queue:work --daemon
      ```
    - Akses aplikasi di `http://localhost:8000`

## Akun Pengguna Default

| Peran     | Email                                 | Password | Hak Akses             |
|-----------|---------------------------------------|----------|-----------------------|
| Admin     | admin@klinikgunung.com                | password | Akses penuh           |
| Dokter    | doctor@klinikgunung.com               | password | Layanan medis         |
| Paramedis | paramedic@klinikgunung.com            | password | Skrining kesehatan    |
| Kasir     | cashier@klinikgunung.com              | password | Pembayaran & transaksi|
| Manajer   | manager@klinikgunung.com              | password | Laporan & analitik    |

## Keamanan
- Autentikasi menggunakan Laravel Sanctum
- Otorisasi berbasis peran
- Enkripsi data sensitif
- Perlindungan CSRF
- Validasi input dan upload file

## Pengujian
```bash
php artisan test
php artisan test --testsuite=Feature
```

## Deployment
- Pastikan file `.env` sudah disesuaikan untuk produksi
- Jalankan cache konfigurasi dan assets
- Setup supervisor untuk queue

## Dukungan
- Dokumentasi: Lihat folder `docs-kg/`
- Masalah teknis: Gunakan fitur Issues di repository GitHub
- Email: support@klinikgunung.com

## Lisensi
Proyek ini dilisensikan di bawah MIT License. Lihat file LICENSE untuk detail.
