# Toko Online CodeIgniter 4

Proyek ini merupakan sistem toko online sederhana berbasis [CodeIgniter 4](https://codeigniter.com/). Aplikasi ini mendukung fungsionalitas dasar e-commerce seperti katalog produk, keranjang belanja, checkout, sistem diskon otomatis harian, dan panel admin untuk manajemen data. Tampilan antarmuka dibuat responsif dengan template [NiceAdmin](https://bootstrapmade.com/nice-admin-bootstrap-admin-html-template/).

## Daftar Isi

- [Fitur](#fitur)
- [Persyaratan Sistem](#persyaratan-sistem)
- [Instalasi](#instalasi)
- [Struktur Proyek](#struktur-proyek)

---

## Fitur

### ✅ Katalog Produk
- Menampilkan daftar produk lengkap dengan gambar, nama, harga.
- Diskon otomatis ditampilkan apabila ada diskon yang berlaku di tanggal login.
- Produk dapat ditambahkan ke keranjang langsung dari katalog.
- Halaman produk menggunakan komponen responsif dari NiceAdmin.

### 🛒 Keranjang Belanja
- Menyimpan produk yang dipilih user dalam sesi keranjang.
- Hitung harga otomatis setelah potongan diskon jika tersedia.
- Tambah, ubah jumlah, dan hapus produk dari keranjang.
- Kosongkan seluruh isi keranjang.
- Menampilkan subtotal per produk dan total keseluruhan.

### 💳 Sistem Transaksi
- Checkout: user mengisi alamat dan memilih ongkir via integrasi API RajaOngkir.
- Harga diskon dan ongkir akan dihitung secara otomatis sebelum pembelian.
- Transaksi dan detailnya akan disimpan di dua tabel: `transaction` dan `transaction_detail`.
- Diskon hari ini akan tercatat di setiap detail transaksi.

### 🔐 Autentikasi & Session
- Login pengguna berdasarkan username dan password terenkripsi.
- Role pengguna (admin/user) disimpan dalam session.
- Diskon harian otomatis dicek saat login dan disimpan dalam session `diskon_nominal`.

### 🛠️ Panel Admin
- **Manajemen Produk** (CRUD + upload gambar)
- **Manajemen Kategori** produk
- **Manajemen Diskon** harian berdasarkan tanggal
- **Laporan Transaksi**
- Ekspor produk dan transaksi ke PDF
- Dashboard berbasis API: data transaksi ditampilkan melalui endpoint `api` menggunakan `curl`.

### 🌐 Web API (Web Service)
- Endpoint RESTful `api` untuk mendapatkan data transaksi dan detailnya.
- Digunakan pada halaman dashboard eksternal untuk menampilkan laporan transaksi real-time.

---

## Persyaratan Sistem

- PHP >= 8.2
- MySQL atau MariaDB
- Composer
- Web server lokal (disarankan: XAMPP)
- Ekstensi PHP aktif:
  - `intl`
  - `curl`
  - `mbstring`
  - `openssl`
  - `pdo_mysql`

---

## Instalasi

### 1. Clone Repository
```bash
git clone [URL repository]
cd belajar-ci-tugas
