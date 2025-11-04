# 🛒 FórtiStore - E-Commerce Management System

## 👨‍💻 Identitas Project

| Nama | NIM | Kelas | Mata Kuliah |
|------|-----|-------|-------------|
| [Ariq Ibtihal] | [312310446] | [TI.23.A5] | Pemrograman Visual|

## 📖 Tentang Project

**FórtiStore** adalah sistem manajemen toko online (e-commerce) yang dirancang untuk memudahkan pengelolaan toko secara digital. Platform ini menyediakan fitur lengkap mulai dari manajemen produk, customer, transaksi penjualan, hingga laporan keuangan — semuanya dalam satu sistem yang modern, responsif, dan mudah digunakan.

## 🎥 Demo Video

https://youtu.be/h4gzLjbwK4E

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


## 🎨 Mockup / Desain Awal

Bagian ini menampilkan hasil rancangan antarmuka (mockup) dari **FórtiStore**. Desain ini dibuat sebagai panduan visual sebelum proses pengembangan dimulai, membantu dalam menentukan struktur halaman, tata letak fitur, dan alur navigasi sistem.

### 🔐 Login Page
<img width="456" height="205" alt="image" src="https://github.com/user-attachments/assets/814376ae-6d12-4a4f-8b39-291b503961c3" />

### 🏠 Dashboard
<img width="449" height="239" alt="image" src="https://github.com/user-attachments/assets/eab5e027-62e5-4506-bf83-6a06139b5ea9" />

## 🏭 Alur Bisnis Proses – FórtiStore (Manajemen Gudang)

```text
[Admin Login]
    ↓
[Dashboard Utama]
    ↓
    ├── [Manajemen Barang]
    │       ├─ Tambah Barang Baru
    │       ├─ Edit Informasi Barang
    │       ├─ Hapus Barang
    │       └─ Lihat/Stok Barang (dengan status masuk & keluar)
    │
    ├── [Manajemen Karyawan]
    │       ├─ Tambah/Edit/Hapus Data Karyawan
    │       ├─ Atur Jabatan & Tugas
    │       └─ Monitoring Aktivitas / Riwayat Input
    │
    ├── [Manajemen Layanan / Operasional]
    │       ├─ Input Layanan (misal: perbaikan, pengiriman, pemeliharaan)
    │       ├─ Update Status Layanan
    │       └─ Catatan Biaya / Penggunaan Barang
    │
    ├── [Transaksi Gudang]
    │       ├─ Barang Masuk (Penerimaan dari Supplier)
    │       ├─ Barang Keluar (Distribusi / Pemakaian)
    │       └─ Cetak Bukti / Laporan Transaksi
    │
    └── [Laporan & Analisis]
            ├─ Laporan Stok Barang
            ├─ Laporan Aktivitas Karyawan
            ├─ Laporan Layanan
            └─ Export Data (PDF / Excel)
    ↓
[Database] ← Semua perubahan tersimpan otomatis


```

**Flow Customer:**
```
[Customer Internal / Divisi Meminta Barang]
    ↓
[Form Permintaan Barang/Layanan]
    ↓
[Admin Gudang Verifikasi Permintaan]
    ↓
    ├── Jika stok tersedia → [Proses Barang Keluar]
    │                             ↓
    │                        [Update Database Stok]
    │                             ↓
    │                        [Barang Dikirim / Layanan Dijalankan]
    │                             ↓
    │                        [Customer Menerima Barang / Layanan]
    │                             ↓
    │                        [Catat Status: Selesai]
    │
    └── Jika stok tidak tersedia → [Permintaan Ditolak / Pending]
                                   ↓
                             [Notifikasi ke Customer]

```

## 📊 Diagram Bisnis Proses

-Diagram ini menggambarkan alur utama sistem FórtiStore, yaitu aplikasi
manajemen gudang untuk mencatat dan mengelola data karyawan, data barang,
layanan permintaan barang, serta laporan aktivitas gudang.
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/dd0d63ad-6e83-4bab-a29c-cf0529e3027f" />


## 📝 Diagram Model Data
-Sistem FórtiStore menyimpan data di MongoDB dengan beberapa koleksi utama:
Admin, Karyawan, Barang, Permintaan, dan Laporan Gudang.
Setiap koleksi memiliki struktur serta relasi yang sederhana dan saling terhubung.
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/a0c67d19-33d7-4eb6-9777-4089bfdce538" />

