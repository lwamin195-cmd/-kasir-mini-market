📄 README.md (Lengkap + Step by Step)
# 🛒 APLIKASI KASIR MINI MARKET

Aplikasi kasir sederhana berbasis **Java Swing** dan **MariaDB** yang digunakan untuk melakukan transaksi penjualan pada mini market.

---

## 📌 DESKRIPSI

Aplikasi ini dibuat untuk membantu proses transaksi seperti:
- Memilih barang
- Menampilkan harga otomatis
- Menghitung total belanja
- Menghitung kembalian
- Menyimpan data ke database

---

## 🚀 FITUR UTAMA

- ✅ ComboBox pilih barang
- ✅ Harga barang otomatis muncul
- ✅ Hitung total harga otomatis
- ✅ Hitung kembalian otomatis
- ✅ Koneksi ke database MariaDB
- ✅ Penyimpanan data transaksi

---

## 🛠️ TEKNOLOGI

- Java (Swing GUI)
- NetBeans IDE
- MariaDB / MySQL
- JDBC

---

## 🗄️ DATABASE SETUP

### 1. Buat Database

Jalankan di HeidiSQL / phpMyAdmin:

```sql
CREATE DATABASE kasir_db;


Jika error "database exists", berarti sudah ada → lanjut saja

2. Gunakan Database
USE kasir_db;

3. Buat Tabel Barang
CREATE TABLE barang (
    id_barang INT AUTO_INCREMENT PRIMARY KEY,
    nama_barang VARCHAR(50),
    harga INT
);

4. Input Data Barang
INSERT INTO barang (nama_barang, harga) VALUES
('Susu', 3000),
('Teh', 4000),
('Coklat', 5000),
('Panda', 1000),
('Adamsari', 5000);

5. Buat Tabel Transaksi
CREATE TABLE transaksi (
    id_transaksi INT AUTO_INCREMENT PRIMARY KEY,
    tanggal DATE,
    total INT,
    bayar INT,
    kembalian INT
);

🔌 KONEKSI DATABASE (JAVA)

Tambahkan kode berikut:

import java.sql.Connection;
import java.sql.DriverManager;

public class Koneksi {
    public static Connection getKoneksi() {
        try {
            Connection conn = DriverManager.getConnection(
                "jdbc:mysql://localhost:3306/kasir_db",
                "root",
                ""
            );
            return conn;
        } catch (Exception e) {
            System.out.println("Koneksi Gagal: " + e.getMessage());
            return null;
        }
    }
}

💻 LOGIKA PROGRAM
1. Menampilkan Harga Otomatis
String NamaBarang = (String) nama_barang.getSelectedItem();

switch (NamaBarang) {
    case "Susu":
        harga_barang.setText("3000000");
        break;
    case "Teh":
        harga_barang.setText("4000000");
        break;
    case "Coklat":
        harga_barang.setText("5000000");
        break;
    case "Panda":
        harga_barang.setText("100000");
        break;
    case "Adamsari":
        harga_barang.setText("500000");
        break;
}

2. Hitung Total Harga
int harga = Integer.parseInt(harga_barang.getText());
int jumlah = Integer.parseInt(jumlah_beli.getText());

int total = harga * jumlah;

jumlah_harga.setText(String.valueOf(total));

3. Hitung Kembalian
int total = Integer.parseInt(jumlah_harga.getText());
int bayar = Integer.parseInt(jumlah_bayar.getText());

int kembalian = bayar - total;

jumlah_kembalian.setText(String.valueOf(kembalian));

▶️ CARA MENJALANKAN APLIKASI
🔹 STEP 1: Jalankan Database

Buka XAMPP / MariaDB

Start MySQL / MariaDB

🔹 STEP 2: Setup Database

Buka HeidiSQL

Jalankan semua query SQL di atas

🔹 STEP 3: Buka Project di NetBeans

File → Open Project

Pilih folder project kamu

🔹 STEP 4: Tambahkan Library MySQL

Klik kanan project

Properties → Libraries

Add JAR → pilih mysql-connector

🔹 STEP 5: Jalankan Program

Klik tombol Run (▶️)

Aplikasi kasir akan muncul

📸 TAMPILAN APLIKASI

Form terdiri dari:

Nama Barang (ComboBox)

Harga Barang

Jumlah Beli

Total Harga

Jumlah Bayar

Kembalian

❗ TROUBLESHOOTING
❌ Error: Can't connect to server

✔ Solusi:

Pastikan MariaDB/XAMPP sudah jalan

❌ Database tidak muncul

✔ Solusi:

Klik kanan → Refresh di HeidiSQL

❌ Table tidak muncul

✔ Solusi:

USE kasir_db;
SHOW TABLES;

❌ Error database exists

✔ Solusi:

Tidak perlu buat ulang database

Langsung pakai saja

👨‍💻 AUTHOR

Nama: Amin

Project: Aplikasi Kasir Mini Market

Tujuan: Tugas Pemrograman Java + Database

🔥 PENGEMBANGAN KE DEPAN

Login User

Cetak Struk

Laporan Transaksi

Manajemen Stok

Scan Barcode

⭐ PENUTUP

Project ini masih versi sederhana, namun sudah mencakup dasar:

GUI

Logika Program

Database

Cocok untuk pembelajaran dan pengembangan lebih lanjut 🚀


---


