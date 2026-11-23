# RPL_KEL9

**Aplikasi Web Pencatatan dan Pengelolaan Stok Barang pada Toko Guns Sport**

> Catat Barang Masuk, Kontrol Barang Keluar, Pantau Stok Lebih Akurat.

---

## 1. Informasi Aplikasi

**Aplikasi Pencatatan dan Pengelolaan Stok Barang pada Toko Guns Sport** adalah aplikasi berbasis web yang dirancang untuk membantu pengelola Toko Guns Sport dalam mencatat dan mengelola persediaan barang secara lebih terstruktur, menggantikan pencatatan stok yang sebelumnya dilakukan secara manual.

Aplikasi ini menyediakan fitur pengelolaan data barang, pencatatan barang masuk dan barang keluar, perhitungan stok secara otomatis, penanda stok menipis, serta penyajian laporan stok berdasarkan periode tertentu.

Melalui dashboard, pemilik toko dapat melihat ringkasan jumlah jenis barang, total stok, dan daftar barang yang stoknya sudah mencapai batas minimum. Setiap perubahan stok hanya terjadi melalui transaksi barang masuk atau barang keluar, sehingga data stok tetap konsisten dengan riwayat transaksi.

### Role Pengguna

Aplikasi memiliki dua jenis pengguna:

| Role | Deskripsi dan Hak Akses |
| --- | --- |
| **Pemilik Toko** | Memantau dan mengawasi pengelolaan stok. Dapat melihat dashboard, data barang, riwayat transaksi, dan laporan stok tanpa dapat mengubah data (*read-only*). |
| **Admin Sistem** | Mengelola operasional pencatatan stok, meliputi mengelola data barang, mencatat barang masuk dan barang keluar, memperbarui stok, serta melihat laporan. |

### Platform

Aplikasi merupakan aplikasi web yang dapat diakses melalui komputer, laptop, maupun smartphone menggunakan browser modern seperti Chrome, Firefox, dan Edge.

---

## 2. Fitur Utama

- **Autentikasi:** Login menggunakan username dan password, serta logout. Pengguna diarahkan ke halaman sesuai role.
- **Dashboard:** Menampilkan jumlah jenis barang, total stok, dan daftar barang dengan stok menipis.
- **Pengelolaan Data Barang:** Menambah, mengubah, menghapus, serta mencari dan memfilter data barang berdasarkan nama, kode, atau kategori.
- **Barang Masuk:** Mencatat transaksi barang masuk yang menambah stok secara otomatis, lengkap dengan riwayat transaksi.
- **Barang Keluar:** Mencatat transaksi barang keluar yang mengurangi stok secara otomatis, dengan validasi agar jumlah keluar tidak melebihi stok yang tersedia.
- **Peringatan Stok Minimum:** Menandai status stok barang sebagai Aman, Menipis, atau Habis berdasarkan batas minimum yang ditentukan.
- **Laporan Stok:** Menampilkan laporan stok per periode dan kategori, serta mencetak atau mengunduh laporan dalam format PDF atau spreadsheet.

---

## 3. Cara Penggunaan Aplikasi

### A. Pemilik Toko

1. **Login ke aplikasi**

   Masuk menggunakan username dan password yang telah terdaftar.

2. **Melihat dashboard**

   Setelah login, dashboard menampilkan jumlah jenis barang, total stok, dan daftar barang yang stoknya menipis.

3. **Melihat data barang**

   Buka halaman data barang untuk melihat daftar barang. Gunakan pencarian atau filter kategori untuk menemukan barang tertentu.

4. **Melihat riwayat transaksi**

   Lihat riwayat transaksi barang masuk dan barang keluar beserta waktu pencatatannya.

5. **Melihat laporan stok**

   Pilih rentang tanggal dan kategori barang untuk menampilkan laporan stok. Laporan dapat dicetak atau diunduh dalam format PDF atau spreadsheet.

6. **Mengelola profil dan logout**

   Buka halaman profil dan pengaturan jika diperlukan, lalu lakukan logout untuk mengakhiri sesi aplikasi.

### B. Admin Sistem

1. **Login ke aplikasi**

   Masuk menggunakan akun Admin Sistem.

2. **Mengelola data barang**

   Tambahkan data barang (kode, nama, kategori, harga, satuan, stok awal, dan batas minimum stok). Data barang dapat diubah atau dihapus setelah konfirmasi, selama belum pernah dipakai pada transaksi.

3. **Mencatat barang masuk**

   Isi kode barang, tanggal masuk, jumlah, dan keterangan. Setelah disimpan, stok barang bertambah secara otomatis.

4. **Mencatat barang keluar**

   Isi kode barang, tanggal keluar, jumlah, dan keterangan. Setelah disimpan, stok barang berkurang secara otomatis. Transaksi ditolak jika jumlah melebihi stok yang tersedia.

5. **Memantau stok menipis**

   Perhatikan penanda status stok pada dashboard dan halaman data barang, lalu lakukan pengadaan untuk barang berstatus Menipis atau Habis.

6. **Melihat laporan stok**

   Tampilkan laporan berdasarkan periode dan kategori, lalu cetak atau unduh jika diperlukan.

7. **Logout**

   Lakukan logout setelah selesai menggunakan aplikasi.

---

## 4. Alur Penggunaan Singkat

```
                +------------------+
                |      Login       |
                +------------------+
                         |
                         v
              +----------------------+
              | Dashboard sesuai Role|
              +----------------------+
                   /            \
                  v              v
      +-------------------+  +---------------------+
      |   Pemilik Toko    |  |    Admin Sistem     |
      +-------------------+  +---------------------+
      | - Dashboard       |  | - Data barang       |
      | - Data barang     |  | - Barang masuk      |
      | - Riwayat         |  | - Barang keluar     |
      |   transaksi       |  | - Stok menipis      |
      | - Laporan stok    |  | - Laporan stok      |
      |   (read-only)     |  +---------------------+
      +-------------------+            |
                 \                     /
                  v                   v
                +------------------+
                |      Logout      |
                +------------------+
```

---

## 5. Catatan

- Fitur yang dapat digunakan setiap pengguna mengikuti role dan hak akses masing-masing.
- Jumlah stok tidak dapat diubah langsung melalui form data barang, hanya melalui transaksi barang masuk atau barang keluar.
- Laporan stok mencerminkan data transaksi yang telah dicatat di dalam sistem.
- Penghapusan data penting dilakukan setelah pengguna memberikan konfirmasi.
- Data barang yang sudah memiliki riwayat transaksi tidak dapat dihapus permanen agar laporan tetap utuh.
- Sesi pengguna berakhir otomatis setelah 30 menit tanpa aktivitas.
- Tampilan aplikasi dirancang responsif agar dapat digunakan pada berbagai ukuran perangkat.

---

**Toko Guns Sport** --- Aplikasi Web Pencatatan dan Pengelolaan Stok Barang.
