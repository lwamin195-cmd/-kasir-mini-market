README.md
# 🛒 Aplikasi Kasir Mini Market

Aplikasi kasir sederhana berbasis **Java Swing** dan **MariaDB** untuk membantu proses transaksi penjualan pada mini market.

---

## 📌 Fitur Utama

- ✅ Pilih barang (ComboBox)
- ✅ Menampilkan harga otomatis
- ✅ Input jumlah beli
- ✅ Hitung total harga otomatis
- ✅ Input jumlah bayar
- ✅ Hitung kembalian otomatis
- ✅ Koneksi database (MariaDB)
- ✅ Penyimpanan data barang & transaksi

---

## 🖥️ Tampilan Aplikasi

- Form Kasir:
  - Nama Barang
  - Harga Barang
  - Jumlah Beli
  - Total Harga
  - Jumlah Bayar
  - Kembalian

---

## 🛠️ Teknologi yang Digunakan

- Java (Swing GUI)
- MariaDB / MySQL
- JDBC (Java Database Connectivity)
- NetBeans IDE

---

## 🗄️ Struktur Database

### Database: `kasir_db`

#### Tabel: `barang`
```sql
CREATE TABLE barang (
    id_barang INT AUTO_INCREMENT PRIMARY KEY,
    nama_barang VARCHAR(50),
    harga INT
);

Tabel: transaksi
CREATE TABLE transaksi (
    id_transaksi INT AUTO_INCREMENT PRIMARY KEY,
    tanggal DATE,
    total INT,
    bayar INT,
    kembalian INT
);

🔌 Konfigurasi Database

Pastikan MariaDB sudah berjalan, lalu gunakan konfigurasi berikut di Java:

Connection conn = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/kasir_db",
    "root",
    ""
);

▶️ Cara Menjalankan

Buka project di NetBeans

Jalankan XAMPP / MariaDB

Import database atau jalankan query SQL

Run project

Gunakan aplikasi kasir

📸 Screenshot (Opsional)

Tambahkan screenshot aplikasi di sini untuk memperjelas tampilan.

👨‍💻 Author

Nama: Amin

Project: Aplikasi Kasir Mini Market

Tujuan: Tugas / Pembelajaran Java & Database

📌 Catatan

Aplikasi ini masih versi sederhana dan dapat dikembangkan lebih lanjut seperti:

Login user

Laporan transaksi

Stok barang

Cetak struk

🔥 Selamat ngoding dan semoga lancar bro!


---

## 🚀 Tips Biar Keren di GitHub
- Tambahin screenshot aplikasi kamu 📸
- Kasih icon emoji biar menarik 😎
- Upload file `.sql` juga biar gampang dipakai orang lain

---

