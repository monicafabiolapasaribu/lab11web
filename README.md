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
- 
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
