# lab11web

### Nama  : Monica Fabiola Pasaribu
### Kelas : TI.20.D1
### NIM   : 312010083

### Praktikum 11: PHP Framework (Codeigniter)
### Langkah-langkah
1. Mengaktifkan Ekstensi
- Aktifkan ekstensi tersebut melalui XAMPP Control Panel pada bagian Apache dengan cara klik Config -> PHP.ini seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/172684173-34e37c50-82fc-459c-b344-9733d5071480.png)

- Lalu pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan seperti berikut. Kemudian simpan kembali filenya dan restart Apache web server.

![image](https://user-images.githubusercontent.com/101724604/172684725-a2d39422-0b20-4cbc-98db-b620f2aa00a1.png)
2. Instalasi CodeIgniter 4
- Codeigniter dapat didownload dari website https://codeigniter.com/download

- Extrak file zip Codeigniter ke direktori htdocs/lab11_php_ci.

- Ubah nama directory framework-4.x.xx menjadi ci4.

- Buka browser dengan alamat http://localhost/lab11web_ci/ci4/public/ Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual seperti berikut.
- 
![image](https://user-images.githubusercontent.com/101724604/172692448-445e2bc2-15d2-4c81-a7d9-fb24e4b74272.png)
3. Menjalankan CLI (Command Line Interface)
Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt, lalu arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (C:\xampp\htdocs\Lab11web_ci\ci4). Kemudian setelah itu jalankan perintah untuk memanggil CLI Codeigniter

![image](https://user-images.githubusercontent.com/101724604/172692342-025f5a66-8864-4c9c-9ea1-bd8ce64a40f8.png)

4.Mengaktifkan Mode Debugging Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/173069823-85f737c2-4ee3-4ccf-9c3e-6d3a84e2eeea.png)

Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu mengaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. Kemudian mengubah nama file env menjadi .env lalu setelah itu buka file tersebut dan ubah nilai variable CI_ENVORNMENT menjadi development. Setelah mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. maka hapus tanda tagar (#) pada awal baris CI_ENVIRONMENT. Dan yang terakhir, ubah kode pada file app/Controller/Home.php kemudian hilangkan titik koma (;) pada akhir kode seperti berikut.

![image](https://user-images.githubusercontent.com/101724604/173071473-730f72a0-a8d6-4e63-bce9-82570006bb9f.png)

Maka hasilnya akan terjadi error seperti berikut.

![image](https://user-images.githubusercontent.com/101724604/173080741-0b385558-d927-4865-b730-e51863539ad6.png)

5. Membuat Route Baru. Menambahkan kode di dalam Routes.php seperti berikut.

![image](https://user-images.githubusercontent.com/101724604/173074122-a22228ed-6970-4dd0-94c6-d0e172bf5558.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about seperti berikut. Maka hasilnya akan terjadi error, yang artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

![image](https://user-images.githubusercontent.com/101724604/173075130-26e37c18-f7d9-4c25-aa3b-9a1f4d34dfe8.png)

6. Membuat Controller
Selanjutnya adalah membuat Controller Page. Buat file dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut
![image](https://user-images.githubusercontent.com/101724604/173094636-45f15f45-8cd9-42a4-9e56-1da16e39a066.png)

7. Auto Routing
Secara default fitur autoroute pada Codeigniter sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variablenya. Untuk menonaktifkan ubah nilai true menjadi false
![image](https://user-images.githubusercontent.com/101724604/173098098-ef8d1c73-4684-4859-b1f9-849e011713b4.png)

8. Membuat View
Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/173098978-82427eaf-0177-4b53-b624-1a8d4d6ebf92.png)

Ubah method about pada class Controller Page menjadi seperti berikut:
![image](https://user-images.githubusercontent.com/101724604/173099867-914ed065-d1f3-493d-ab20-03cbd743b316.png)

Maka hasilnya akan seperti berikut:
![image](https://user-images.githubusercontent.com/101724604/173100145-3668f409-6a48-40ff-8d2b-dff48361beb3.png)

9. . Membuat Layout Web dengan CSS
Pada dasarnya layout web dengan css dapat diimplementasikan dengan mudah pada codeigniter. Yang perlu diketahui adalah, pada Codeigniter 4 file yang menyimpan asset css dan javascript terletak pada direktori public.

Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout) Kita akan gunakan layout yang pernah dibuat pada praktikum 4.
![image](https://user-images.githubusercontent.com/101724604/173111399-79c564da-da5d-4672-8a43-881f3fe69fb8.png)


Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php
![image](https://user-images.githubusercontent.com/101724604/173104474-e40298b5-c421-49e8-a38c-3b2c8df7cef5.png)
![image](https://user-images.githubusercontent.com/101724604/173104634-60f0318a-b560-41f4-8164-c916d69fd7c8.png)

Maka hasilnya seperti berikut:
![image](https://user-images.githubusercontent.com/101724604/173109848-d8e5e997-cc7f-4981-9d44-b2b43c73e26b.png)

PERTANYAAN DAN TUGAS

Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.
![image](https://user-images.githubusercontent.com/101724604/173110959-6a19666f-ea29-444e-9a05-6ea6cf4d9132.png)

![image](https://user-images.githubusercontent.com/101724604/173111894-85b48e7d-2b87-4d46-8dbf-03e7445fecb5.png)

#Praktikum 12: Framework Lanjutan (CRUD) Langkah-langkah Praktikum

Persiapan

Untuk memulai membuat aplikasi CRUD sederhana, yang perlu disiapkan adalah database server menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui XAMPP seperti berikut.
#Praktikum 12: Framework Lanjutan (CRUD) Langkah-langkah Praktikum

Persiapan

Untuk memulai membuat aplikasi CRUD sederhana, yang perlu disiapkan adalah database server menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui XAMPP seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175327201-a3980173-7577-4157-bfd5-01cb76dd682f.png)

Langkah 1 Membuat database kemudian membuat Tabel dan masukkan kode pada database query seperti berikut.

Langkah 2 Konfigurasi koneksi database
Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. Kemudian melakukan konfigurasi dengan cara mengubah beberapa kode pada file htdocs\lab11_php_ci\ci4.env. Lalu cari pada line DATABASE dan hilangkan tanda pagar (#) didepan seperti berikut ini.
![image](https://user-images.githubusercontent.com/101724604/175327436-87023461-1cfa-4d37-8edd-b462f5c8124a.png)

Langkah 3 Membuat Model
Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori app/Models dengan nama ArtikelModel.php lalu masukkan kode seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175327604-943f88fc-f626-44f4-8a4b-fe52f6e528a3.png)

Langkah 4 Membuat Controller
Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers lalu masukkan kode seperti berikut.

![image](https://user-images.githubusercontent.com/101724604/175327777-4b19051d-05c0-4d03-ac62-8f6174d68850.png)

Langkah 5 Membuat View
Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file baru dengan nama index.php.
![image](https://user-images.githubusercontent.com/101724604/175327997-140dae69-4d54-4fe4-be42-47d99c1f4938.png)

Selanjutnya buka browser kembali, dengan mengakses url http://localhost:8080/artikel maka hasilnya akan seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175328198-8523ce33-ede7-43ab-b561-3260eb45a180.png)

Terlihat belum ada data yang diampilkan. Kemudian coba tambahkan beberapa data pada database query agar dapat ditampilkan datanya seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175328341-28c0b1b4-f8de-4c00-befd-4748cca8e81a.png)

Lalu refresh kembali browser, sehingga akan ditampilkan hasilnya seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175328447-91aa09a8-2c15-421a-8e49-0b4cdb52bc5d.png)

Langkah 6 Membuat Tampilan Detail Artikel

Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. Tambahkan fungsi baru pada Controller Artikel dengan nama view().
![image](https://user-images.githubusercontent.com/101724604/175575565-10e1dcd7-fb4c-43f3-aa98-3b392d89537c.png)


Langkah 7 Membuat View Detail
Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175575691-955b63c3-0116-4648-b214-0ada0decb50d.png)

Langkah 8 Membuat Routing untuk artikel detail
Buka kembali file app/config/Routes.php, kemudian tambahkan routing untuk artikel detail maka hasilnya akan seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175575904-951d961b-c7ff-4b1b-9822-7bfcc9196b34.png)

Langkah 9 Membuat Menu Admin
Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama admin_index() seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175576271-6413442d-d8ad-4423-b602-12816149e30a.png)

Selanjutnya buat view untuk tampilan admin dengan nama admin_index.php seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175577129-7cebfeb4-ea4a-47d5-ae86-f64ad54955bb.png)


Setelah itu tambahkan routing untuk menu admin seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175577475-ae9c4b99-33d2-4796-a4e2-d9f57a296d6f.png)

Kemudian akses menu admin dengan url http://localhost:8080/admin/artikel seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175577683-b625dbc3-dcf9-4e46-bea4-7676683bf50b.png)

Langkah 10 Menambah Data Artikel

Tambahkan fungsi/method baru pada Controller Artikel dengan nama add() seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175579253-ebb0503b-03c8-4d61-ade3-f2019a9b08bf.png)


Kemudian buat view untuk form tambah dengan nama form_add.php seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/175593883-d8ecc1e4-737c-4517-9259-746c871b9117.png)

![image](https://user-images.githubusercontent.com/101724604/175595427-93bcd2dd-35c3-45d9-ac30-72eb2c790437.png)

#Praktikum 13: Framework Lanjutan (Modul Login)

- Langkah 1 Membuat Tabel User
Membuat tabel user pada database lab_ci4 seperti berikut.

![image](https://user-images.githubusercontent.com/101724604/176089390-f67c3b30-0ad6-4752-b34e-77a8dcc0d930.png)

- Langkah 2 Membuat Model User
Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori app/Models dengan nama UserModel.php dan masukkan kode seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176090879-9ca2bac9-947c-4360-b475-3d7640c817d7.png)

- Langkah 3 Membuat Controller User
Buat Controller baru dengan nama User.php pada direktori app/Controllers. Kemudian tambahkan method index() untuk menampilkan daftar user, dan method login() untuk proses login dan masukkan kode seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176091120-c18b8f37-2a21-4908-8c07-effa0ba2c622.png)
![image](https://user-images.githubusercontent.com/101724604/176091151-ba1c4757-4802-4ecd-8a08-1d0c277c66a7.png)

- Langkah 4 Membuat View Login
Buat folder baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php dan masukkan kode seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176091232-6e25f139-346b-417d-8313-803f3ab5f983.png)

- Langkah 5 Membuat Database Seeder
Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul login, kita perlu memasukkan data user dan password kedalam database. Untuk itu buat database seeder untuk tabel user. Buka CLI, kemudian ketik perintah berikut:
![image](https://user-images.githubusercontent.com/101724604/176092438-bfe1c170-8026-4edd-9149-bebc14150e3b.png)

Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori /app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut:
![image](https://user-images.githubusercontent.com/101724604/176092609-15e29458-6dfe-4cd1-b5f9-0e3a85c7d52f.png)

Selanjutnya buka kembali CLI dan ketik perintah berikut:
![image](https://user-images.githubusercontent.com/101724604/176093213-6d2bbe09-4997-46af-a196-a2b71c8e39d2.png)


Selanjutnya buka url http://localhost:8080/user/login seperti berikut:
![image](https://user-images.githubusercontent.com/101724604/176094180-5ae2e330-5eea-40f2-aaf5-86510df87e8c.png)

- Langkah 6 Menambahkan Auth Filter
Selanjutnya membuat filter untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori app/Filters dan masukkan kode seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176094539-0d4c2870-9cc5-4149-8137-cc25769266f2.png)

Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:
![image](https://user-images.githubusercontent.com/101724604/176095142-64380279-bf8b-4926-a761-bde8615429fd.png)

- Langkah 7 Fungsi Logout
Tambahkan method logout pada Controller User dan masukkan kode seperti berikut:
![image](https://user-images.githubusercontent.com/101724604/176095960-e87c5564-6c58-46fc-af0c-c6c747d6beff.png)

- Langkah 8 Tombol Logout
Menambahkan tombol Logout pada menu header admin dengan cara ke direktori app\view\template lalu buka file admin_header.php dan masukkan kode seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176096478-37090659-11a6-41b8-8323-e1ddab533785.png)

Praktikum 14: Pagination dan Pencarian

- Langkah-langkah Praktikum Persiapan
Hal pertama yang dilakukan adalah menjalankan Apache & MySQL server di XAMPP seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176218304-ba7afa36-68c7-44e2-9226-2432efa901e2.png)

- Langkah 1 Membuat Pagination
Pagination merupakan proses yang digunakan untuk membatasi tampilan yang panjang dari data yang banyak pada sebuah website. Fungsi pagination adalah memecah tampilan menjadi beberapa halaman tergantung banyaknya data yang akan ditampilkan pada setiap halaman.

Pada Codeigniter 4, fungsi pagination sudah tersedia pada Library sehingga cukup mudah menggunakannya

Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi kode pada method admin_index seperti berikut
![image](https://user-images.githubusercontent.com/101724604/176223662-d5a2c6c5-f2ca-48ba-9457-1846cbd207f3.png)

Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut dibawah deklarasi tabel data.
![image](https://user-images.githubusercontent.com/101724604/176219662-53780cae-6943-4efe-b18e-26c8c11de34c.png)

Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat hasilnya.
![image](https://user-images.githubusercontent.com/101724604/176219913-bddc9d0c-6c46-457c-9ee5-5d27502bfde2.png)

Membuat Pencarian.
Pencarian data digunakan untuk memfilter data.Untuk membuat pencarian data, buka kembali Controller Artikel, pada method admin_index ubah kodenya seperti berikut
![image](https://user-images.githubusercontent.com/101724604/176224268-a12cfa75-25cb-4aa1-9e70-b7149a313f91.png)

Kemudian buka kembali file views/artikel/admin_index.php dan tambahkan form pencarian sebelum deklarasi tabel seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176225152-e5e11e66-fdaa-4085-b75e-88c47825494a.png)

Dan pada link pager ubah seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176225724-5d36bee3-4ad2-4bdf-9f79-83e557f28846.png)

Selanjutnya ujicoba dengan membuka kembali halaman admin artikel, masukkan kata kunci tertentu pada form pencarian.
![image](https://user-images.githubusercontent.com/101724604/176226235-cc265660-8f70-463e-8d50-438499394dfc.png)

- Langkah 3 Upload Gambar
Menambahkan fungsi unggah gambar pada tambah artikel. Buka kembali Controller Artikel, sesuaikan kode pada method add seperti berikut:
![image](https://user-images.githubusercontent.com/101724604/176227005-b4a8bc67-0ed4-4fb0-ab61-08f8160c508a.png)

Kemudian pada file views/artikel/form_add.php tambahkan field input file seperti berikut.
![image](https://user-images.githubusercontent.com/101724604/176227490-520340c3-ea71-4410-aafd-26eac4531d1f.png)

Dan sesuaikan tag form dengan menambahkan ecrypt type seperti berikut
![image](https://user-images.githubusercontent.com/101724604/176228035-baa9f1eb-3d1e-409d-b10d-81a1d65f8509.png)

Ujicoba file upload dengan mengakses menu tambah artikel.


![image](https://user-images.githubusercontent.com/101724604/176228444-539690f5-ebf9-4392-a154-f96c7591d7ec.png)


































