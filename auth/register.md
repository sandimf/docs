---
description: Panduan Registrasi Sistem Klinik Gunung
---

# Panduan Registrasi

Dokumentasi ini menjelaskan proses registrasi (pendaftaran akun) pada sistem Klinik Gunung yang dibangun menggunakan Laravel. Registrasi diperlukan agar pengguna dapat mengakses layanan dan fitur sesuai peran (pasien, dokter, paramedis, dsb).

## Alur Registrasi

1. **Akses Halaman Registrasi**
   - Endpoint: `GET /register`
   - Menampilkan form registrasi akun baru.

2. **Kirim Data Registrasi**
   - Endpoint: `POST /register`
   - Data yang dikirim:
     - `name` (wajib)
     - `email` (wajib, unik)
     - `password` (wajib, konfirmasi password)
   - Jika data valid, akun akan dibuat dan pengguna otomatis login.
   - Pengguna akan diarahkan ke dashboard dan diminta verifikasi email.

3. **Verifikasi Email**
   - Setelah registrasi, sistem akan mengirim email verifikasi ke alamat email yang didaftarkan.
   - Pengguna wajib memverifikasi email sebelum dapat menggunakan seluruh fitur.

## Catatan Keamanan
- Password disimpan secara terenkripsi (bcrypt) di database.
- Email harus unik dan valid.
- Sistem menggunakan validasi Laravel untuk memastikan keamanan data.

## Registrasi dengan Google (Opsional)
- Jika fitur login sosial diaktifkan, pengguna dapat mendaftar menggunakan akun Google melalui:
  - Endpoint: `GET /auth/google/redirect`
  - Endpoint: `GET /auth/google/callback`

---

Untuk pertanyaan lebih lanjut, hubungi admin sistem atau lihat dokumentasi pengembang.

