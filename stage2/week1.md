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

# 3. Backend

## Deploy Aplikasi Backend
- Clone Aplikasi Backend, jalankan perintah ini untuk meng-clone repositori `git clone url-repository`.

  ![backend1 1](https://github.com/user-attachments/assets/08eb5705-74c9-4f12-bef9-e274f99ba34a)

- Menggunakan Node.js Versi 14.

  ![backend1 2](https://github.com/user-attachments/assets/311cdb8d-1c8e-4621-8287-73a1fac75aeb)

  ![backend1 3](https://github.com/user-attachments/assets/e1f910fd-1fc3-4536-ae58-4eb1aa6dc62d)

- Mengubah Konfigurasi pada dumbflix-backend/config/config.json. Sesuaikan bagian berikut dengan konfigurasi database kita.

  ![backend1 4](https://github.com/user-attachments/assets/dc50a7ca-b700-4a92-9ecf-fe7f75c5274d)

- Install sequelize-cli secara global dan Install dependensi backend.

  ![backend1 5](https://github.com/user-attachments/assets/758e029d-874d-4e72-b1cb-e3d5611d7c3f)

  ![backend1 6](https://github.com/user-attachments/assets/317f9025-c42a-42c3-89d4-9c42e8bac5fc)

- Jalankan Migrasi dan Gunakan sequelize-cli, untuk menjalankan migrasi database
  masukkan perintah `npx sequelize-cli db:migrate`.

  ![backend1 7](https://github.com/user-attachments/assets/9a6de238-ced4-4683-9305-4b8d618754d7)

- Deploy Aplikasi Menggunakan PM2.

  Install pm2.

  ![backend1 8](https://github.com/user-attachments/assets/c5f9514d-62a1-430b-b440-523045d0ac91)

  Jalankan aplikasi menggunakan PM2.

  ![backend1 9](https://github.com/user-attachments/assets/457a9bfd-5d51-4f17-aed6-bee6f2fc0da3)

  ![backend1 10](https://github.com/user-attachments/assets/5dae3985-f43a-4734-90b8-eda89056981e)

- Jalankan aplikasi di browser `ip-server:5000`.

  ![backend1 11](https://github.com/user-attachments/assets/c1abdd6b-2605-42fe-87e2-f337729b0e91)

---

# 4. Frontend

## Deploy Aplikasi Frontend
- Clone Aplikasi Frontend `git clone url-repository`.

  ![fe1 1](https://github.com/user-attachments/assets/054be289-f8ea-425c-ace6-00d1cfd260cb)

- Gunakan Node.js Versi 14

  ![fe1 2](https://github.com/user-attachments/assets/aa7df825-7cc7-4782-8c69-ab3f7af016ef)

- Mengubah Konfigurasi pada `src/config/api.js` menjadi `"http://localhost:5000/api";`.

  ![fe1 3](https://github.com/user-attachments/assets/d1ec5c06-1ec8-4656-9149-e70d4d6a53d9)

- Install Dependensi 'npm install'.

  ![fe1 4](https://github.com/user-attachments/assets/08eca747-ac0f-4da2-90a4-cea12a75bc2e)

- Deploy Frontend Menggunakan PM2.

  ![fe1 5](https://github.com/user-attachments/assets/3a4bf556-2a4a-44c8-850d-608b802814a0)

  ![fe1 6](https://github.com/user-attachments/assets/c0272bfd-8b98-4b83-9724-f37335751df6)

- Mencoba akses Aplikasi Frontend `ip-server:3000`.

  ![fe1 7](https://github.com/user-attachments/assets/21364212-42df-4f08-8a48-0927af83feda)


---

# 5. Webserver

## Install Nginx
- Install Nginx di server kita dan setelah instalasi selesai, pastikan Nginx berjalan.

  ![ws1 1](https://github.com/user-attachments/assets/56502d0f-0635-499a-8dd8-9769e9cb14c2)


  ![ws1 2](https://github.com/user-attachments/assets/a16af069-aef1-4107-a696-c9503289f60f)

##  Buat Reverse Proxy dan Konfigurasi Domain
- Buat file konfigurasi baru untuk frontend dan tambahkan konfigurasi reverse proxy nya.

  ![ws1 3](https://github.com/user-attachments/assets/37f569e4-98c0-4cba-9f43-2be490d7621e)

- Buat file konfigurasi baru untuk backend dan tambahkan konfigurasi reverse proxy nya.

  ![ws1 4](https://github.com/user-attachments/assets/30d55d78-ac1d-4690-8aa5-0c18b4e5ae13)

## Pasang SSL untuk Domain
- Menggunakan Certbot.

  Install certbot.

  ![ws1 5](https://github.com/user-attachments/assets/78c482c4-0d8b-4425-8592-f1f5d8f30655)

  Jalankan Certbot untuk mengaktifkan SSL.

  ![ws1 6](https://github.com/user-attachments/assets/443d3f42-4056-4626-b694-24a33d57bf3d)

  ![ws1 7](https://github.com/user-attachments/assets/13859799-cebb-4da0-9e21-97c36ade921c)

## Implementasi Wildcard SSL
- Wildcard SSL memungkinkan kita menggunakan satu sertifikat SSL untuk banyak subdomain di domain yang sama misalnya
 (*.zakky.studentdumbways.my.id).

  Jalankan perintah `sudo certbot -d *.nama-domain --manual --preferred-challenges dns certonly`.

  ![ws1 8](https://github.com/user-attachments/assets/f9a46d61-8026-4bd0-96a2-c933cda118d3)

  Certbot akan memberikan teks yang perlu kita tambahkan ke DNS TXT Record di cloudflare.
  
  ![ws1 9](https://github.com/user-attachments/assets/a4648b1e-b8a0-49c3-96a9-4457b484caa8)

  Setelah menambahkan DNS TXT Record, lanjutkan proses hingga selesai.

  ![ws1 10](https://github.com/user-attachments/assets/310c861f-3a94-41cd-b405-14ea694540e0)

  




  
  



  

  



  

  


   

   




  








  



  
  
  


   








  

  











  

