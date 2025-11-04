# 🛒 FórtiStore - E-Commerce Management System

## 👨‍💻 Identitas Project

| Nama | NIM | Kelas | Mata Kuliah |
|------|-----|-------|-------------|
| [Nama Anda] | [NIM Anda] | [Kelas Anda] | Pemrograman Framework |

## 📖 Tentang Project

**FórtiStore** adalah sistem manajemen toko online (e-commerce) yang dirancang untuk memudahkan pengelolaan toko secara digital. Platform ini menyediakan fitur lengkap mulai dari manajemen produk, customer, transaksi penjualan, hingga laporan keuangan — semuanya dalam satu sistem yang modern, responsif, dan mudah digunakan.

## 🎥 Demo Video

> 🚧 Coming Soon - Video demo sedang dalam proses pembuatan

## ✨ Fitur Utama

| 🧩 Fitur | 💡 Deskripsi |
|----------|-------------|
| 🏠 **Dashboard Admin** | Menampilkan ringkasan data seperti total produk, customer, transaksi, dan pendapatan |
| 👥 **Manajemen Customer** | CRUD (Create, Read, Update, Delete) data pelanggan dengan tampilan tabel interaktif |
| 📦 **Manajemen Produk** | Kelola katalog produk, harga, stok, kategori, dan gambar produk |
| 🛍️ **Manajemen Transaksi** | Proses pemesanan, pembayaran, dan tracking status pesanan |
| 📊 **Laporan Penjualan** | Tampilkan laporan penjualan harian, bulanan, dan tahunan secara otomatis |
| 🏷️ **Manajemen Kategori** | Organisir produk berdasarkan kategori untuk memudahkan pencarian |
| 📈 **Analisis Data** | Dashboard analitik untuk melihat tren penjualan dan produk terlaris |
| ⚙️ **Pengaturan Toko** | Konfigurasi informasi toko, metode pembayaran, dan pengiriman |

## 🛠️ Teknologi yang Digunakan

- **Backend Framework:** [ASP.NET Core / Laravel / Spring Boot / Express.js]
- **Frontend:** [HTML, CSS, JavaScript / React / Vue.js / Bootstrap]
- **Database:** [MySQL / PostgreSQL / MongoDB / SQL Server]
- **Version Control:** Git & GitHub
- **Tools:** Visual Studio Code, Git Bash

## 📦 Instalasi & Setup

### Prerequisites
- [Runtime/SDK yang dibutuhkan, contoh: .NET 6+, Node.js 16+]
- [Database yang digunakan, contoh: MySQL 8.0+]
- Git

### Langkah Instalasi

1. **Clone repository**
```bash
git clone https://github.com/ariq190505/FramworkUpb.git
cd FramworkUpb
```

2. **Install dependencies**
```bash
# Sesuaikan dengan framework yang digunakan
# Contoh untuk .NET:
dotnet restore

# Contoh untuk Node.js:
npm install
```

3. **Setup database**
```bash
# Buat database baru
# Import file database atau jalankan migration
# Contoh: mysql -u root -p < database/fortistore.sql
```

4. **Konfigurasi environment**
```bash
# Copy file konfigurasi
cp .env.example .env

# Edit file .env sesuai dengan setup lokal Anda
# Atur connection string database, API keys, dll
```

5. **Jalankan aplikasi**
```bash
# Sesuaikan dengan framework yang digunakan
# Contoh untuk .NET:
dotnet run

# Contoh untuk Node.js:
npm start
```

6. **Akses aplikasi**
```
Buka browser dan akses: http://localhost:5000
Login default:
- Username: admin
- Password: admin123
```

## 🎨 Mockup / Desain Awal

Bagian ini menampilkan hasil rancangan antarmuka (mockup) dari **FórtiStore**. Desain ini dibuat sebagai panduan visual sebelum proses pengembangan dimulai, membantu dalam menentukan struktur halaman, tata letak fitur, dan alur navigasi sistem.

### 🔐 Login Page
> Screenshot halaman login admin

### 🏠 Dashboard
> Screenshot dashboard utama dengan statistik toko

### 👥 Data Customer
> Screenshot halaman manajemen pelanggan

### 📦 Katalog Produk
> Screenshot halaman daftar produk

### 🛍️ Transaksi Penjualan
> Screenshot halaman transaksi dan orders

### 📊 Laporan & Analitik
> Screenshot halaman laporan penjualan

## 📊 Diagram Bisnis Proses

Berikut adalah alur bisnis proses dari sistem **FórtiStore**:

```
[Admin Login]
    ↓
[Dashboard Utama]
    ↓
    ├── [Manajemen Customer] → [Tambah/Edit/Hapus/Lihat Data]
    ├── [Manajemen Produk] → [Tambah/Edit/Hapus/Upload Gambar]
    ├── [Manajemen Kategori] → [Tambah/Edit/Hapus Kategori]
    ├── [Transaksi] → [Proses Pesanan/Update Status/Cetak Invoice]
    └── [Laporan] → [Lihat/Export Laporan Penjualan]
    ↓
[Database] ← Semua perubahan tersimpan otomatis
```

**Flow Customer:**
```
[Customer Browse Produk] 
    ↓
[Tambah ke Keranjang]
    ↓
[Checkout & Pembayaran]
    ↓
[Konfirmasi Pesanan]
    ↓
[Tracking Status Pengiriman]
```

## 📊 Diagram Model Data

Sistem **FórtiStore** menyimpan data dengan beberapa tabel/koleksi utama:

### Struktur Database

**1. Tabel Admin**
- id (Primary Key)
- username
- email
- password (hashed)
- role
- created_at

**2. Tabel Customer**
- id (Primary Key)
- nama
- email
- no_telepon
- alamat
- kota
- kode_pos
- created_at

**3. Tabel Kategori**
- id (Primary Key)
- nama_kategori
- deskripsi
- icon

**4. Tabel Produk**
- id (Primary Key)
- nama_produk
- deskripsi
- harga
- stok
- kategori_id (Foreign Key)
- gambar_url
- is_active
- created_at

**5. Tabel Transaksi**
- id (Primary Key)
- customer_id (Foreign Key)
- tanggal_transaksi
- total_harga
- status (pending/paid/shipped/completed/cancelled)
- metode_pembayaran
- alamat_pengiriman

**6. Tabel Detail Transaksi**
- id (Primary Key)
- transaksi_id (Foreign Key)
- produk_id (Foreign Key)
- jumlah
- harga_satuan
- subtotal

**7. Tabel Laporan Penjualan**
- id (Primary Key)
- tanggal
- total_transaksi
- total_pendapatan
- produk_terlaris

### Relasi Antar Tabel
- Customer **1 : N** Transaksi (Satu customer bisa memiliki banyak transaksi)
- Transaksi **1 : N** Detail Transaksi (Satu transaksi bisa memiliki banyak item)
- Produk **N : 1** Kategori (Banyak produk dalam satu kategori)
- Produk **1 : N** Detail Transaksi (Satu produk bisa dibeli berkali-kali)

## 🚀 Roadmap Pengembangan

- [x] Setup project & database
- [x] Implementasi login & authentication
- [x] CRUD Customer
- [x] CRUD Produk & Kategori
- [ ] Sistem keranjang belanja
- [ ] Proses checkout & pembayaran
- [ ] Integrasi payment gateway
- [ ] Sistem notifikasi (email/WhatsApp)
- [ ] Laporan & dashboard analitik
- [ ] Responsive mobile design
- [ ] Deployment ke production

## 📝 Lisensi

Project ini dibuat untuk keperluan akademik - Universitas Pelita Bangsa

## 👤 Kontak

Jika ada pertanyaan atau saran, silakan hubungi:
- Email: [email@example.com]
- GitHub: [@ariq190505](https://github.com/ariq190505)

---

⭐ Jangan lupa berikan star jika project ini bermanfaat!

**Dibuat dengan ❤️ untuk Mata Kuliah Pemrograman Framework - UPB**
