# Tugas 9

Jelaskan mengapa kita perlu membuat model Dart saat mengambil/mengirim data JSON? Apa konsekuensinya jika langsung memetakan Map<String, dynamic> tanpa model (terkait validasi tipe, null-safety, maintainability)?
= membuat model dart untuk json membantu kita dalam validasi tipe data, memastikan null-safety, dan meningkatkan maintainability. jika kita langsung memetakan ke Map<String, dynamic>, kita bisa kesulitan dalam menangani tipe data yang salah atau data kosong, yang berisiko menyebabkan error di runtime.

Apa fungsi package http dan CookieRequest dalam tugas ini? Jelaskan perbedaan peran http vs CookieRequest.
= http digunakan untuk mengirim permintaan HTTP (seperti GET, POST, dll) ke server. CookieRequest adalah kelas khusus yang menambahkan dukungan untuk menyimpan dan mengirimkan cookie secara otomatis. perbedaan utama, http mengirimkan permintaan biasa, sementara CookieRequest menangani autentikasi berbasis cookie.

Jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
= instance CookieRequest dibagikan agar setiap bagian aplikasi yang membutuhkan akses ke server bisa menggunakan sesi yang sama (termasuk cookie). ini penting untuk autentikasi dan menjaga konsistensi status login antar layar.

Jelaskan konfigurasi konektivitas yang diperlukan agar Flutter dapat berkomunikasi dengan Django. Mengapa kita perlu menambahkan 10.0.2.2 pada ALLOWED_HOSTS, mengaktifkan CORS dan pengaturan SameSite/cookie, dan menambahkan izin akses internet di Android? Apa yang akan terjadi jika konfigurasi tersebut tidak dilakukan dengan benar?
= kita perlu menambahkan 10.0.2.2 pada ALLOWED_HOSTS untuk memungkinkan komunikasi dengan emulator Android. CORS harus diaktifkan agar aplikasi Flutter bisa mengakses API Django tanpa masalah. pengaturan SameSite dan cookie memastikan bahwa session tetap aman. izin akses internet di Android diperlukan agar aplikasi dapat mengakses server. jika ini tidak dikonfigurasi dengan benar, aplikasi tidak akan dapat berkomunikasi dengan server atau gagal mengirimkan permintaan.

Jelaskan mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter.
= data dikirim dari input pengguna di Flutter (misal, form login) ke server Django menggunakan HTTP request. server kemudian memproses data dan mengirimkan respons kembali ke Flutter, yang kemudian menampilkannya sesuai kebutuhan.
 
Jelaskan mekanisme autentikasi dari login, register, hingga logout. Mulai dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
= pengguna memasukkan data login di Flutter, data dikirim ke Django menggunakan HTTP POST, Django memverifikasi data, dan jika valid, mengirimkan cookie atau token autentikasi, aplikasi flutter menyimpan cookie dan menggunakannya untuk akses lebih lanjut, seperti menuju menu utama setelah login.

Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).
= buat model Dart untuk memetakan data JSON agar mempermudah validasi dan penggunaan, gunakan http untuk mengirim permintaan dan CookieRequest untuk mengelola autentikasi berbasis cookie, konfigurasikan Django untuk mendukung komunikasi dengan Flutter, pastikan CORS diaktifkan dan ALLOWED_HOSTS benar, implementasikan login dan register di Flutter, kirim data ke Django, dan tangani respons untuk autentikasi, bagi instance CookieRequest menggunakan provider agar bisa diakses di seluruh aplikasi.


# Tugas 8

Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement() pada Flutter. Dalam kasus apa sebaiknya masing-masing digunakan pada aplikasi Football Shop kamu?
 = navigator.push() menambahkan halaman baru tanpa menghapus halaman sebelumnya, sehingga bisa kembali ke halaman sebelumnya. navigator.pushreplacement() mengganti halaman aktif dengan yang baru, jadi tidak bisa kembali. di football shop, push digunakan untuk berpindah ke detail produk, sedangkan pushreplacement untuk kembali ke halaman utama setelah menambah produk

 Bagaimana kamu memanfaatkan hierarchy widget seperti Scaffold, AppBar, dan Drawer untuk membangun struktur halaman yang konsisten di seluruh aplikasi?
 = scaffold menjadi kerangka utama halaman, appbar menampilkan judul dan navigasi, sedangkan drawer digunakan untuk berpindah antarhalaman seperti halaman utama dan tambah produk. kombinasi ini membuat tampilan aplikasi konsisten dan mudah digunakan

 Dalam konteks desain antarmuka, apa kelebihan menggunakan layout widget seperti Padding, SingleChildScrollView, dan ListView saat menampilkan elemen-elemen form? Berikan contoh penggunaannya dari aplikasi kamu.
 = padding memberi jarak antar elemen agar rapi, singlechildscrollview membuat form bisa digulir, dan listview menampilkan daftar input dengan mudah. di football shop, form tambah produk dibungkus dengan singlechildscrollview dan diberi padding agar nyaman dilihat

 Bagaimana kamu menyesuaikan warna tema agar aplikasi Football Shop memiliki identitas visual yang konsisten dengan brand toko?
 = tema disesuaikan dengan identitas football shop, misalnya warna hijau dan putih seperti lapangan bola. warna utama digunakan pada appbar dan tombol agar tampilan konsisten dan merepresentasikan brand toko




A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
"# tugas7" 
