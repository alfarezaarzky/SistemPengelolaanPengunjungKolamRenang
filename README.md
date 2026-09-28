# Sistem Pengelolaan Pengunjung Kolam Renang


| Keterangan | Data |
|---|---|
| Nama | Muhammad Rizky Alfa Reza Basyah |
| NIM | 2509116086 |
| Kelas | C 2025 |
| Mata Kuliah | Pemrograman Berorientasi Objek |

---

## Penjelasan Studi Kasus

Program ini merupakan aplikasi berbasis Java yang digunakan untuk mengelola data pengunjung kolam renang. Program dibuat untuk menerapkan konsep Pemrograman Berorientasi Objek (PBO), khususnya inheritance.

Sistem ini memiliki beberapa class utama, yaitu `Pengunjung`, `Member`, dan `Tiket`. Class `Pengunjung` digunakan untuk menyimpan informasi dasar pengunjung. Class `Member` merupakan turunan dari class `Pengunjung` yang memiliki informasi tambahan sebagai anggota kolam renang. Class `Tiket` digunakan untuk mengelola informasi tiket yang digunakan oleh pengunjung.

Program menyediakan fitur untuk menambahkan, menampilkan, mengubah, dan menghapus data pengunjung. Program juga menggunakan input dari pengguna sehingga data dapat dikelola melalui menu yang tersedia.

---

## Struktur Class

Program terdiri dari beberapa class utama:

### 1. Class Pengunjung

Class `Pengunjung` merupakan class dasar yang menyimpan informasi umum mengenai pengunjung kolam renang.

Atribut yang digunakan antara lain:
- `nama`
- `umur`

Class ini menjadi parent class yang dapat diturunkan oleh class lain.

### 2. Class Member

Class `Member` merupakan turunan dari class `Pengunjung`. Class ini digunakan untuk menyimpan informasi tambahan mengenai pengunjung yang memiliki status sebagai member.

Atribut tambahan antara lain:
- `idMember`
- `Diskon`

Class `Member` menerapkan konsep inheritance dengan mewarisi atribut dan method dari class `Pengunjung`.

### 3. Class Tiket

Class `Tiket` digunakan untuk mengelola informasi tiket masuk kolam renang.

Atribut yang digunakan antara lain:
- `jenisTiket`
- `harga tiket`

Class ini digunakan untuk menyimpan informasi mengenai jenis dan harga tiket yang digunakan pengunjung.

---

## Penerapan Inheritance 

<img width="786" height="719" alt="image" src="https://github.com/user-attachments/assets/7b4a62d5-9ecf-4202-888e-c19c81762f13" />

Inheritance diterapkan pada class `Member` melalui `extends Pengunjung`, sehingga `Member` dapat mewarisi atribut dan method dari class `Pengunjung`. Constructor `super(nama, umur)` digunakan untuk memanggil constructor parent class, sedangkan `idMember` menjadi atribut tambahan pada `Member`. Method `hitungBiaya()` dan `tampilkanInfo()` menggunakan `@Override` untuk memberikan implementasi khusus bagi member, seperti mendapatkan diskon **20% dari harga tiket**.

## Polimorphism 

<img width="753" height="383" alt="image" src="https://github.com/user-attachments/assets/353aa43c-3f79-4b25-973a-4e786f754d3f" />

Polymorphism diterapkan melalui method hitungBiaya() dan tampilkanInfo() yang menggunakan @Override pada class Member. Method tersebut mengubah implementasi dari class Pengunjung sehingga Member memiliki perilaku khusus, yaitu mendapatkan diskon 20% dari harga tiket dan menampilkan informasi tambahan seperti ID member. Dengan demikian, method yang sama dapat menghasilkan perilaku yang berbeda sesuai dengan objek yang digunakan.

## Condition 

<img width="576" height="582" alt="image" src="https://github.com/user-attachments/assets/c6b91211-b2ee-46b9-b010-f029a44782fa" />

Condition diterapkan pada bagian if (daftarPengunjung.isEmpty()) untuk memeriksa apakah daftar pengunjung masih kosong. Jika kondisi bernilai true, program menampilkan pesan “Belum ada data pengunjung.”. Jika kondisi bernilai false, program menjalankan blok else dan menampilkan seluruh data pengunjung menggunakan perulangan for. Dengan demikian, condition digunakan untuk menentukan proses yang dijalankan berdasarkan kondisi data pengunjung.

## Perulangan

<img width="735" height="420" alt="image" src="https://github.com/user-attachments/assets/40cd0854-8958-4b75-b66b-b8d245645060" />

<img width="338" height="150" alt="image" src="https://github.com/user-attachments/assets/d6735f52-a920-4a0b-86a9-a5640f8fbcc3" />

Perulangan diterapkan menggunakan blok `do-while` untuk menampilkan menu interaktif **Sistem Pengelolaan Pengunjung Kolam Renang** dan memproses input pengguna secara berulang. Blok kode di dalam `do` akan mengeksekusi tampilan menu pilihan (seperti **1. Tambah Pengunjung Umum** hingga **6. Keluar**), menerima input angka `pilihan` dari pengguna, dan mengeksekusi percabangan `switch (pilihan)` minimal satu kali. Kondisi `while (pilihan != 6)` memastikan bahwa program akan terus mengulang penampilkan menu selama pengguna tidak memilih menu **6 (Keluar)**. Setelah pengguna memilih opsi **6**, perulangan akan dihentikan dan objek *scanner* ditutup dengan `input.close()`.

## Fitur Program

Program Sistem Pengelolaan Pengunjung Kolam Renang memiliki beberapa fitur utama, yaitu:

- **Tambah Data Pengunjung**  
  Digunakan untuk menambahkan data pengunjung baru ke dalam sistem.

  <img width="510" height="826" alt="image" src="https://github.com/user-attachments/assets/833eac67-e03a-41d1-a097-f3e6463555f4" />

Fitur ini digunakan untuk menambahkan data pengunjung baru ke dalam sistem dengan menginputkan informasi dasar seperti nama dan umur. Berdasarkan masukan tersebut, sistem secara otomatis akan mengategorikan jenis pengunjung (seperti Pengunjung Umum), mengidentifikasi jenis tiket yang sesuai (seperti Tiket Reguler), serta menetapkan harga tiket terkait untuk disimpan ke dalam daftar registrasi pengunjung.

- **Tambah Member**  
  Digunakan untuk menambahkan data member baru ke dalam sistem.

  <img width="438" height="859" alt="image" src="https://github.com/user-attachments/assets/104775fe-2f9d-44fc-803b-bacc967488c1" />

Fitur ini digunakan untuk mendaftarkan pengunjung berstatus member ke dalam sistem dengan menginputkan data seperti nama, umur, dan ID Member. Sistem secara otomatis akan mencatat jenis pengunjung sebagai Member, memberikan potongan harga atau diskon khusus (sebesar 20%), serta menyesuaikan total harga tiket yang harus dibayar sebelum menyimpannya ke dalam daftar pengunjung.

- **Tampilkan Data Pengunjung**  
  Digunakan untuk menampilkan seluruh data pengunjung yang telah tersimpan.

  <img width="497" height="474" alt="image" src="https://github.com/user-attachments/assets/4db0ef6d-d4a6-4897-934d-6cc2cdcb21c1" />

Fitur ini digunakan untuk menampilkan seluruh daftar data pengunjung yang telah terdaftar di dalam sistem secara terstruktur. Informasi yang disajikan mencakup nomor urut pengunjung, jenis pengunjung (seperti Umum atau Member), nama, umur, jenis tiket yang dibeli (seperti Tiket Reguler), serta rincian harga tiket masing-masing pengunjung.

- **Tampilkan Daftar Tiket**  
  Digunakan untuk menampilkan jenis tiket yang ada.

  <img width="495" height="347" alt="image" src="https://github.com/user-attachments/assets/efb705d6-4682-45d0-97f5-930d2f637b9c" />

Fitur ini digunakan untuk menyajikan informasi mengenai kategori tiket yang tersedia di dalam sistem beserta rincian tarif harganya masing-masing. Melalui tampilan ini, pengguna dapat melihat daftar jenis tiket yang ditawarkan—seperti Tiket Reguler dengan harga Rp25.000,0 dan Tiket Anak dengan harga Rp15.000,0—sebagai acuan penetapan harga tiket untuk pengunjung.
  
- **Hitung Total Pendapatan**  
  Digunakan untuk menghitung dan menampilkan total pendapatan.

  <img width="436" height="328" alt="image" src="https://github.com/user-attachments/assets/116dbf7b-0a8b-406c-9c51-e21df6651885" />

Fitur ini digunakan untuk menghitung dan menampilkan akumulasi seluruh pendapatan dari hasil penjualan tiket pengunjung yang terdaftar dalam sistem. Sistem secara otomatis menjumlahkan total nominal pembayaran tiket (baik dari Pengunjung Umum maupun Member setelah dipotong diskon) dan menyajikannya dalam jumlah keseluruhan, seperti Total Pendapatan : Rp45000.

- **Keluar**  
  Digunakan untuk keluar dari program atau mengakhiri program.

  <img width="811" height="387" alt="image" src="https://github.com/user-attachments/assets/f73794f5-0cbb-4df4-bc27-f759e412a983" />

Fitur ini digunakan untuk menghentikan dan menutup jalannya program Sistem Pengelolaan Pengunjung Kolam Renang secara aman. Saat opsi ini dipilih, sistem akan menampilkan pesan penutup seperti "Terima kasih telah menggunakan Sistem Pengelolaan Kolam Renang!" lalu mengakhiri sesi pengeksekusian aplikasi.

## Kesimpulan 

Sistem Pengelolaan Pengunjung Kolam Renang merupakan aplikasi berbasis Java yang menerapkan prinsip Pemrograman Berorientasi Objek (PBO), khususnya *inheritance*, melalui hubungan *parent-child* antara class `Pengunjung` dan class `Member` serta dukungan class `Tiket`. Aplikasi ini mempermudah pengelolaan data operasional dengan menyediakan fitur lengkap untuk pendaftaran pengunjung umum maupun member, perhitungan diskon secara otomatis (20%), penayangan daftar tiket dan data pengunjung terdaftar, hingga kalkulasi total pendapatan penjualan tiket dan penutupan program secara aman.
