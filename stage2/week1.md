# 1.Server

## Membuat pengguna baru untuk semua server kita
- pertama kita menaruh ssh-key dari cloud ke lokal kita di dalam direktori `ssh`. 

  ![server1](https://github.com/user-attachments/assets/528a1a55-df30-4394-98b6-34aaf08cac59)

- lalu kita masuk kedalam server kita di cloud dengan perintah `ssh -i file-ssh username@ip-server`.

  ![server2](https://github.com/user-attachments/assets/4aa17a05-946c-4a54-9295-66821043f245)

  ![server3](https://github.com/user-attachments/assets/5b7a59da-3c54-4eb2-9b0d-8f5e41bc4c61)

- Selanjutnya barulah kita membuat user baru di dalam server kita dengan perintah `sudo adduser username` serta kita memberi akses root
  pada user baru kita dengan perintah `sudo usermod -aG sudo username` dan masuk ke dalam user baru dengan perintah `sudo su username`.

  ![server4](https://github.com/user-attachments/assets/dfb97f6e-aede-46e6-bfb8-2538fc43a56c)

  ![server5](https://github.com/user-attachments/assets/e43d15c0-8ef2-4a80-bbec-d94f15014611)

##  Server dapat masuk dengan kunci SSH dan kata sandi 
- Langkah pertama kita merubah PasswordAuthentication pada file 60-cloudimg-settings.conf di dalam direktori `/etc/ssh/sshd_config.d`

  ![server6](https://github.com/user-attachments/assets/5170644b-0c51-41d7-b84f-7ed1ab3c0dcf)

- Berikutnya kita uncomment PubkeyAuthentication yes dan PasswordAuthentication yes pada file sshd_config di dalam direktori
  `/etc/ssh`.

  ![server7](https://github.com/user-attachments/assets/bd1b92f9-a173-4c5c-b3f3-676100f96a5f)

- Barulah kita bisa mengakses server dengan password kita yang ada di cloud dan juga bisa menggunakan ssh-key.

  ![server8](https://github.com/user-attachments/assets/7c3e04e5-3682-4b51-949c-f5a62cbc858c)

  ![server9](https://github.com/user-attachments/assets/81778fe5-18a3-466d-a90f-5a7a21b35b75)

  ---

# 2.Database

##  Deploy Database MySQL
- Install mysql di server kita dengan perintah `sudo apt install mysql-server`.

  ![database1 1](https://github.com/user-attachments/assets/525a4d05-2b44-48cb-b181-28ace168cb26)

- Setup Secure Installation dengan perintah `sudo mysql_secure_installation`.

  ![database1 3](https://github.com/user-attachments/assets/0d851349-c07a-4039-ad74-3baaf5dd7515)

  ![database1 2](https://github.com/user-attachments/assets/e2d62c12-df8c-4a7f-a489-55d8bb859716)

  Ikuti langkah-langkah yang ditampilkan:
    > Hapus user anonymous.
    > Nonaktifkan akses remote root .
    > Hapus database test.
    > Reload tabel hak akses.

- Tambahkan Kata Sandi untuk Pengguna root.

  Login ke MySQL menggunakan hak akses root dengan perintah `sudo mysql`.

  ![database1 4](https://github.com/user-attachments/assets/1688164a-d980-4813-925b-b5376e980a1b)

  Ubah cara autentikasi root ke mysql_native_password dan tambahkan password.

  ![database1 5](https://github.com/user-attachments/assets/5c1cb50e-d15f-4ebe-b1a9-42357e5ba64b)

- Buat Pengguna Baru di MySQL.

  Login kembali ke MySQL menggunakan password root dan membuat user baru.

  ![database1 6](https://github.com/user-attachments/assets/83852c7c-4082-4a71-bad6-a998b3ecb920)

- Buat database baru dengan perintah `CREATE DATABASE new_database;`.

  ![database1 7](https://github.com/user-attachments/assets/28a875cd-97a3-403b-a13e-f75892071198)

- Berikan Hak Akses Penuh ke User baru.

  ![database1 8](https://github.com/user-attachments/assets/8e6defd9-99b4-43d4-a972-55c2b361a5b2)

- Mengubah Bind Address dengan edit file configurasi mysql `/etc/mysql/mysql.conf.d/mysqld.cnf`, lalu ubah Bind Address
  menjadi `0.0.0.0` untuk mengizinkan koneksi remote, setelah itu restart mysql `sudo systemctl restart mysql`.

  ![database1 9](https://github.com/user-attachments/assets/f409fb9a-69f6-46e0-b6e1-f555fd23e66a)

  ![database1 10](https://github.com/user-attachments/assets/d4e8aca3-a218-477e-920d-5f3ce9c4b080)

## Role-Based Management
- Buat database demo dan tabel transaction.

  ![database2 1](https://github.com/user-attachments/assets/e341b9fa-d809-4478-a94a-50f828d07827)

-  Buat Role dan Berikan Hak Akses.

   Buat role admin dan guest.

   ![database2 2](https://github.com/user-attachments/assets/662be0ee-b326-4958-9665-a36e9ebb1cac)

   Berikan hak akses Admin: Hak akses penuh ke tabel transaction, Guest: Hanya akses SELECT.

   ![database2 3](https://github.com/user-attachments/assets/d9ed0acc-4dbe-47a1-b265-23d8569a0297)

- Buat Pengguna Baru dan Tambahkan ke Role.

  Buat pengguna your_name dan tambahkan ke role admin dan buat pengguna guest dan tambahkan ke role guest.

  ![database2 4](https://github.com/user-attachments/assets/80dab9a6-7b18-4083-b5bc-8bf49142dd0a)

- Tes User yang sudah di buat

  ![database2 5](https://github.com/user-attachments/assets/1f0888dd-be29-46b9-a2e7-d0ff0e35207f)

##  Remote User
- Remote Database dari Komputer Lokal.

  Install MySQL Client di komputer lokal lalu hubungkan ke server mysql

  ![database2 6](https://github.com/user-attachments/assets/e4cb7d31-929e-4c76-9c86-54e707e2923b)

  ![database2 7](https://github.com/user-attachments/assets/f46eec1c-0713-4cb7-8d74-8fd72338582e)


---




  



  
  
  


   








  

  











  

