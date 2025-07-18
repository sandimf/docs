---
description: Panduan Login Sistem Klinik Gunung
---

# Panduan Login

Dokumentasi ini menjelaskan proses login ke sistem Klinik Gunung yang dibangun menggunakan Laravel. Login diperlukan untuk mengakses fitur-fitur yang bersifat privat sesuai dengan peran pengguna (pasien, dokter, paramedis, admin, dsb).

## Alur Login

1. **Akses Halaman Login**
   - Endpoint: `GET /login`
   - Menampilkan form login. Jika login dengan Google diaktifkan, akan muncul opsi login sosial.

2. **Kirim Data Login**
   - Endpoint: `POST /login`
   - Data yang dikirim:
     - `email` (wajib)
     - `password` (wajib)
   - Jika data valid, pengguna akan diarahkan ke dashboard sesuai peran.
   - Jika gagal, akan muncul pesan error.

3. **Logout**
   - Endpoint: `POST /logout`
   - Mengakhiri sesi login dan mengarahkan ke halaman utama.

## Fitur Tambahan

- **Lupa Password**
  - Endpoint: `GET /forgot-password` untuk menampilkan form permintaan reset password.
  - Endpoint: `POST /forgot-password` untuk mengirim permintaan reset password ke email.
  - Endpoint: `GET /reset-password/{token}` untuk mengatur ulang password.
  - Endpoint: `POST /reset-password` untuk menyimpan password baru.

- **Verifikasi Email**
  - Setelah registrasi, pengguna akan menerima email verifikasi.
  - Endpoint: `GET /verify-email` untuk menampilkan prompt verifikasi.
  - Endpoint: `GET /verify-email/{id}/{hash}` untuk memverifikasi email.
  - Endpoint: `POST /email/verification-notification` untuk mengirim ulang email verifikasi.

- **Login Sosial (Google)**
  - Endpoint: `GET /auth/google/redirect` untuk login dengan Google.
  - Endpoint: `GET /auth/google/callback` untuk callback setelah autentikasi Google.

## Catatan Keamanan
- Semua data login dienkripsi dan diproses secara aman menggunakan Laravel Auth.
- Sesi pengguna akan otomatis berakhir jika logout atau token kadaluarsa.

---

Untuk pertanyaan lebih lanjut, hubungi admin sistem atau lihat dokumentasi pengembang.



