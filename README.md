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




















