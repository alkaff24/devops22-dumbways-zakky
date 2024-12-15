## Dokumentasi Shortcut Text Editor Nano

![nano](https://github.com/user-attachments/assets/2dc5980a-8798-45ac-82cb-e1c2e4c956f6)


Nano adalah text editor berbasis terminal yang ringan dan mudah digunakan. Berikut ini adalah daftar shortcut yang dapat membantu Anda bekerja lebih efisien dengan Nano:

### Navigasi Dasar
- **Ctrl + A**: Pindah ke awal baris.
- **Ctrl + E**: Pindah ke akhir baris.
- **Ctrl + Y**: Scroll ke atas.
- **Ctrl + V**: Scroll ke bawah.
- **Ctrl + W**: Cari teks.
- **Ctrl + \\**: Cari dan ganti teks.

### Manipulasi Teks
- **Ctrl + K**: Potong baris (cut).
- **Ctrl + U**: Tempelkan teks yang telah dipotong (paste).
- **Ctrl + J**: Merapikan paragraf (justify).
- **Ctrl + T**: Periksa ejaan.

### File dan Penyimpanan
- **Ctrl + O**: Simpan file.
- **Ctrl + X**: Keluar dari Nano.
- **Ctrl + R**: Masukkan konten dari file lain.
- **Ctrl + G**: Membuka bantuan.

### Pemilihan Teks
- **Ctrl + ^**: Memulai pemilihan teks dari posisi kursor saat ini.

### Shortcut Lainnya
- **Ctrl + C**: Menampilkan posisi kursor saat ini (baris dan kolom).
- **Alt + A**: Menandai teks (selection).
- **Alt + }**: Indentasi ke kanan.
- **Alt + {**: Indentasi ke kiri.
- **Ctrl + _**: Pindah ke baris tertentu.

### Kombinasi Spesifik
Beberapa shortcut di Nano menggunakan kombinasi tombol **Alt** atau **Ctrl**, tergantung pada sistem operasi yang digunakan. Jika Alt tidak berfungsi, Anda dapat mencoba **Esc** sebagai pengganti.

### Catatan Penting
- Simbol **^** berarti tombol **Ctrl**.
- Nano menunjukkan daftar shortcut utama di bagian bawah editor saat sedang digunakan, sehingga memudahkan pengguna untuk mempelajari fungsinya.

---

## Dokumentasi Manipulasi Teks di Terminal

Pada dasarnya, kita bisa melakukan manipulasi pada sebuah file menggunakan terminal tanpa menggunakan teks editor seperti Nano. Berikut adalah beberapa perintah yang dapat digunakan:

### 1. cat
`cat` adalah salah satu perintah yang berfungsi untuk membuat daftar konten atau isi file pada standard output (stdout). Selain itu, cat juga bisa digunakan untuk:

#### Contoh Penggunaan:
- **Melihat isi file**
  `cat file-name`

  ![docmanipul-1](https://github.com/user-attachments/assets/e0587e37-7658-4d52-b226-d9e2cabd3b55)


- **Membuat file baru dan menambahkan teks**
  `cat > file-name`

  ![docmanipul-2](https://github.com/user-attachments/assets/9cbac0a4-2082-40a7-9075-32c191142f8f)


  Setelah menambahkan teks, keluar dengan menekan `Ctrl + C`.

- **Menggabungkan dua file menjadi satu**
  `cat file1 file2 > file3`

  ![docmanipul-3](https://github.com/user-attachments/assets/fb64aee2-4c8e-4c95-b163-e2368c00f1b5)


  Menggabungkan `file1` dan `file2` menjadi `file3`.

### 2. sed
`sed` adalah singkatan dari *stream editor*. Gunanya untuk memanipulasi teks dasar pada file. Dengan `sed`, kita dapat mengganti teks dengan cepat.

#### Contoh Penggunaan:
- **Mengganti teks dalam file**
  `sed -i 's/hello/holla/g' file3`

  ![docmanipul-4](https://github.com/user-attachments/assets/af7104ac-1a94-44a0-86d0-247db1b134b2)


  Mengganti semua kata "hello" menjadi "holla" pada `file3`.

### 3. grep
`grep` digunakan untuk mencari teks dalam file.

#### Contoh Penggunaan:
- **Mencari teks dalam file**
  `grep dumbways file3`

  ![docmanipul-5](https://github.com/user-attachments/assets/28db7095-69de-4717-b8c0-b80c333cb29f)


  Mencari kata "dumbways" pada `file3`.

- **Menghitung jumlah kemunculan kata**
  `grep -c holla file3`

  ![docmanipul-6](https://github.com/user-attachments/assets/0819b327-b902-4c61-9fde-47f110c270d7)

  Menghitung jumlah kata "holla" pada `file3`.

- **Mencari kata di semua file dalam direktori**
  `grep holla *`

  ![docmanipul-7](https://github.com/user-attachments/assets/25e8545e-4140-4b89-b0a7-251612fcfd60)

  Mencari semua file yang berisi kata "holla".

### 4. sort
`sort` digunakan untuk mengurutkan data, baik secara ascending maupun descending.

#### Contoh Penggunaan:
- **Mengurutkan data secara ascending**
  `sort file4`

  ![docmanipul-8](https://github.com/user-attachments/assets/dd4d67e3-e51a-4761-a08c-691d302a7d02)


- **Mengurutkan data secara descending**
  `sort -r file4`

  ![docmanipul-9](https://github.com/user-attachments/assets/2b1edae3-835a-4a67-a5f6-a3d6a10bc619)

  

### 5. echo
`echo` digunakan untuk mencetak string atau pesan ke stdout atau file.

#### Contoh Penggunaan:
- **Mencetak string ke dalam file**
  `echo "hello dumbways!" > file5`

  ![docmanipul-10](https://github.com/user-attachments/assets/611ae1d2-a1cd-4cb6-92f0-093c5df1f30e)


- **Menambahkan string ke file**
  `echo "hello guys!" >> file5`

  ![docmanipul-11](https://github.com/user-attachments/assets/a7dbfb15-ea36-4b33-9c0f-7b9a4a204deb)


- **Mengganti isi file dengan string baru**
  `echo "Replace semua data" > file5`

  ![docmanipul-12](https://github.com/user-attachments/assets/3531dce6-fb1b-4766-871a-205302e344c7)


  Menghapus semua data di `file5` dan menggantinya dengan "Replace semua data".

---

## Case Manipulasi Teks: Formula 1 Drivers

### Deskripsi
Kita bekerja di sebuah tim data analis untuk sebuah situs web yang menampilkan data pembalap Formula 1. Data pembalap disimpan dalam sebuah file teks `formula-one-drivers.md` dengan format berikut:

```plaintext
ID,Nama,Tim,Posisi,Gaji
001,Lewis Hamilton,Mercedes,1,70000000
002,Max Verstappen,Red Bull Racing,2,50000000
003,Sergio Perez,Red Bull Racing,3,25000000
004,Charles Leclerc,Ferrari,4,15000000
005,Lando Norris,Mclaren,5,10000000
006,Daniel Ricciardo,AlphaTauri,6,8000000
```

Tugas Anda adalah melakukan beberapa manipulasi teks menggunakan perintah `sed` di Linux:

### 1. Mengganti "Red Bull Racing" dengan "Red Bull Racing Honda"
Gunakan perintah `sed` untuk mengganti teks pada kolom Tim: `sed -i 's/Red Bull Racing/Red Bull Racing Honda/g' formula-one-drivers.md`.

![casetextmanipul-1](https://github.com/user-attachments/assets/eba34440-4eda-4e8f-9b3f-eefa8c9fb032)


#### Penjelasan:
- **`-i`**: Mengedit file secara langsung.
- **`s/lama/baru/g`**: Mengganti semua kemunculan `lama` ("Red Bull Racing") dengan `baru` ("Red Bull Racing Honda").
- **`g`**: Global, untuk memastikan semua kemunculan dalam baris diganti.

### 2. Menghapus seluruh baris dengan posisi lebih dari 3
Gunakan `sed` untuk mencocokkan dan menghapus baris berdasarkan kolom Posisi (lebih dari 3): `sed -i '/,[4-9],/d' formula-one-drivers.md`.

![casetextmanipul-2](https://github.com/user-attachments/assets/e0c0c2cd-588c-4312-8d05-bf11fcb1bb56)



#### Penjelasan:
- **`/pattern/d`**: Mencocokkan pola tertentu dan menghapus baris tersebut.
- **`,[4-9],`**: Mencari baris 4 hingga 9 yang berada di antara koma.
- **`-i`**: Mengedit file langsung.

### Hasil Akhir
Setelah menjalankan kedua perintah di atas, isi file `formula-one-drivers.md` akan menjadi:

![casetextmanipul-3](https://github.com/user-attachments/assets/5b7de63e-c386-4f9c-b75a-3fff7019602b)


---

## Case Bash Script : Installasi Webserver

1. Buat file dengan nama yang sesuai, misalnya: `install_webserver.sh`.

   ![casebashscript-1](https://github.com/user-attachments/assets/716aa8f7-ed19-4946-bb57-9599beae4c22)

2. Pastikan file memiliki izin eksekusi dengan menjalankan perintah berikut: `chmod +x install_webserver.sh`.

    ![casebashscript-2](https://github.com/user-attachments/assets/bb049437-da23-497b-9c20-c02ce380b31a)

     
    ![casebashscript-3](https://github.com/user-attachments/assets/860ce4c3-76b6-4fc2-9523-ef29f383f3d3)

3. Jalankan script menggunakan perintah: `./install_webserver.sh`.

   ![casebashscript-4](https://github.com/user-attachments/assets/aba86f6e-fe45-4fe6-930a-cad60b01fbf8)

   Jika yang di input selain angka 1 dan 2 muncul pesan tidak valid

   ![casebashscript-5](https://github.com/user-attachments/assets/ad484a4d-cf39-4480-aa8e-51972df5de84)


---


# Implementasi Firewall pada Linux Server dengan UFW

## Langkah-Langkah:

### 1. **Setup 2 Virtual Machine (Server A dan Server B)**
- Pastikan kita memiliki dua VM.
- **Server A** akan digunakan untuk mengakses **Server B**.
- **Server B** akan menjalankan layanan WebServer (misalnya Nginx).

![casedualvm-1](https://github.com/user-attachments/assets/a1e626fe-dc00-4c99-b45a-515146b32e11)


### 2. **Install UFW pada Kedua Server**
Pada Server A dan Server B, jalankan perintah berikut untuk menginstall UFW (jika belum terinstal):
`sudo apt update; sudo apt install ufw -y`

![casedualvm-2](https://github.com/user-attachments/assets/064c49d4-7db6-458d-8577-4372efec39ad)




### 3. **Konfigurasi WebServer pada Server B**
1. Install WebServer (misalnya Nginx) pada Server B:
   `sudo apt install nginx -y`

   ![casedualvm-3](https://github.com/user-attachments/assets/451336f9-c9c9-457e-9c68-6a1a89c638e7)

   
3. Pastikan WebServer berjalan:
   `sudo systemctl start nginx; sudo systemctl enable nginx`

   ![casedualvm-4](https://github.com/user-attachments/assets/b407eb15-1093-48af-9a13-6ae05284984b)


4. Periksa apakah WebServer aktif:
   `sudo systemctl status nginx`

   ![casedualvm-5](https://github.com/user-attachments/assets/fa819f04-9ddf-433c-bf15-ce1684432f74)




### 4. **Atur Firewall pada Server B untuk Mengizinkan Akses Hanya dari Server A**
1. Ketahui alamat IP dari Server A:
   `ip addr show`

   ![casedualvm-6](https://github.com/user-attachments/assets/0c9055a8-c0df-4dd0-9d23-425ddf426787)

   

3. Pada Server B, konfigurasikan UFW agar hanya mengizinkan koneksi HTTP (port 80) dari Server A:
   `sudo ufw allow from 192.168.1.10 to any port 80`
   
   ![casedualvm-7](https://github.com/user-attachments/assets/c0e2c39e-0996-4aef-b148-f6c219f4326d)

   

5. Blokir akses dari semua IP lain ke port 80:
   `sudo ufw deny 80`

   ![casedualvm-8](https://github.com/user-attachments/assets/cd8ec3b3-dff2-4909-a867-ae500468ebf7)


7. Aktifkan UFW pada Server B:
   `sudo ufw enable`

   ![casedualvm-9](https://github.com/user-attachments/assets/9483cf90-6fd5-48d6-98f1-892f4fe278b6)

   

9. Periksa aturan UFW yang sudah diterapkan:
   `sudo ufw status verbose`

   ![casedualvm-10](https://github.com/user-attachments/assets/da69ac71-73df-4b31-a2e4-5a2b732be657)




### 5. **Verifikasi**
- Dari Server A, coba akses WebServer pada Server B menggunakan browser atau `curl`:
  `curl http://192.168.1.20`

  ![casedualvm-11](https://github.com/user-attachments/assets/0b5037f6-f0b5-490a-b967-4fc51f7fd7af)


  

- Dari Server lain (bukan Server A), coba akses WebServer pada Server B. **Akses harus ditolak.**

  ![casedualvm-12](https://github.com/user-attachments/assets/484fed10-9f23-4186-96c2-9ac3fb2f1f51)




### 6. **Konfigurasi untuk Specific Protocols**
UFW memungkinkan pengaturan berdasarkan protokol (TCP atau UDP). Berikut adalah contoh aturan:

- **Mengizinkan akses pada port tertentu menggunakan TCP**:
  `sudo ufw allow 22/tcp`

- **Mengizinkan akses pada port tertentu menggunakan UDP**:
  `sudo ufw allow 53/udp`

- **Blokir protokol tertentu**:
  `sudo ufw deny 123/udp`



## Perbedaan TCP dan UDP

| **Fitur**                  | **TCP (Transmission Control Protocol)**               | **UDP (User Datagram Protocol)**               |
|----------------------------|-------------------------------------------------------|----------------------------------------------- |
| **Koneksi**                | Berbasis koneksi (connection-oriented).               | Tanpa koneksi (connectionless).                |
| **Kehandalan**             | Menjamin pengiriman data dengan acknowledgment.       | Tidak menjamin pengiriman data.                |
| **Kecepatan**              | Lebih lambat karena ada proses validasi data.         | Lebih cepat karena tidak ada validasi.         |
| **Penggunaan Bandwidth**   | Membutuhkan lebih banyak bandwidth.                   | Lebih hemat bandwidth.                         |
| **Aplikasi**               | Web browsing, email, transfer file (HTTP, FTP, SMTP). | Streaming, video call, game online (DNS, VoIP).|



















