# Laporan Praktikum: Membangun UI Profil Flutter (Hari 1-4)

## Hari 1: Kerangka Dasar & Refactoring Awal
**Tugas:** 
Membuat halaman dasar profil (`main.dart` dan `profile_page.dart`) dengan Scaffold, lalu memecah widget yang menumpuk.

Perbaikan & Update Kode:
* Menambahkan keyword `const` pada pemanggilan `MainApp()` untuk optimasi performa.
* Memperbaiki tata letak jarak antara foto profil dan nama pengguna dengan mengubah `SizedBox(width: 16)` menjadi `height: 16` (karena susunannya vertikal di dalam `Column`).
* Melakukan *extract widget* pada bagian foto dan teks menjadi `ProfileAvatar` dan `ProfileInfo`.


## Hari 2: Menambahkan Komponen Statistik Profil
**Tugas:** 
Menambahkan deretan angka statistik (Proyek, Followers, Following) menggunakan `Row`, kemudian mengekstrak komponen tersebut menjadi widget mandiri.

**Perbaikan & Update Kode:**
* Memperbaiki jarak antar angka statistik dengan mengubah `SizedBox(height: 24)` menjadi `width: 24` (karena susunannya horizontal di dalam `Row`).
* Memperbaiki error tipe data pada angka statistik dengan mengubah nilai integer `42` menjadi string `'42'`.
* Melakukan *extract widget* pada blok baris statistik menjadi `ProfileStats`.


## Hari 3: Menambahkan Daftar Pengalaman (ListView)
**Tugas:** 
Menampilkan daftar dummy pengalaman kerja yang bisa di-scroll menggunakan `ListView.builder`, lalu merapikan tampilannya menjadi bentuk Card.

**Perbaikan & Update Kode:**
* Memperbaiki error saat aplikasi dijalankan dengan menambahkan tanda koma (`,`) yang hilang pada penulisan array data `experiences`.
* Membungkus `ListView` menggunakan widget `Expanded` agar daftar pengalaman tidak menabrak batas ukuran layar (*overflow*).
* Melakukan *extract widget* pada desain item riwayat pengalaman menjadi `ExperienceCard`.


## Hari 4: Finishing & Interaksi Statis (SnackBar)
**Tugas:** 
Merapikan tata letak komponen profil secara keseluruhan dan memberikan aksi statis pada tombol utama.

**Perbaikan & Update Kode:**
* Mengecek dan menyesuaikan ulang padding serta jarak (`SizedBox`) antar komponen agar proporsi UI terlihat lebih rapi.
* Menambahkan fungsi `onPressed` pada tombol "Edit Profil" menggunakan perintah `ScaffoldMessenger`.
* Menampilkan notifikasi `SnackBar` berisi pesan "Fitur edit belum aktif pada modul statis" saat tombol ditekan.