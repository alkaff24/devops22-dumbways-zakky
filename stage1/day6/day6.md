# Apa itu Web Server?

![webserver](https://github.com/user-attachments/assets/d9711b6d-bbc6-4180-8de9-69775a8c7e57)

**Web server** adalah perangkat lunak atau perangkat keras yang bertugas untuk menerima permintaan (requests) dari klien, seperti browser web, dan memberikan respons (responses) berupa halaman web, file, atau data lainnya. Web server menggunakan protokol HTTP (Hypertext Transfer Protocol) atau HTTPS (HTTP Secure) untuk berkomunikasi.

Secara sederhana, web server berfungsi sebagai "perantara" antara pengguna yang ingin mengakses informasi di internet dan data yang tersimpan di server.


## Cara Kerja Web Server

Berikut adalah proses kerja sebuah web server:

1. **Permintaan dari Klien**:
   - Klien, seperti browser (Chrome, Firefox, dll.), mengirim permintaan HTTP ke web server.
   - Permintaan ini bisa berupa URL tertentu, seperti `http://example.com/index.html`.

2. **Penerimaan dan Pemrosesan Permintaan**:
   - Web server menerima permintaan dan memprosesnya.
   - Pemrosesan ini melibatkan pencarian file atau menjalankan skrip tertentu (misalnya, PHP atau Python) untuk menghasilkan konten dinamis.

3. **Pengembalian Respons**:
   - Web server mengirimkan respons berupa file statis (HTML, CSS, gambar, dll.) atau konten dinamis yang dihasilkan oleh aplikasi.
   - Jika permintaan tidak dapat diproses (misalnya, file tidak ditemukan), server memberikan kode status seperti 404 (Not Found).

4. **Pengiriman Data ke Klien**:
   - Data dikirim kembali ke klien, yang kemudian ditampilkan oleh browser sebagai halaman web.

---

## Gambaran Cara Kerja Web Server

Berikut adalah ilustrasi sederhana bagaimana web server bekerja:

1. **Browser Klien**:  
   - Pengguna memasukkan URL di browser, misalnya `http://example.com`.

2. **DNS Resolving**:  
   - Browser meminta DNS untuk mengonversi domain (`example.com`) ke alamat IP server.

3. **Koneksi ke Web Server**:  
   - Browser mengirim permintaan HTTP ke alamat IP server melalui port (biasanya 80 untuk HTTP dan 443 untuk HTTPS).

4. **Pemrosesan Permintaan**:  
   - Web server memproses permintaan berdasarkan URL dan aturan yang telah ditentukan (misalnya, mencari file `index.html`).

5. **Pengiriman Respons**:  
   - Web server mengirimkan data yang diminta ke browser.


## Diagram Alur Cara Kerja Web Server

```plaintext
Browser Klien
     │
     └─> Permintaan HTTP ke Web Server
           (via DNS → IP Address)
                 │
                 └─> Web Server
                       │
      (Cari File / Jalankan Aplikasi Backend)
                       │
                 └─> Respons HTTP
                       │
                 └─> Browser Menampilkan Konten
```


## Contoh Web Server Populer

- **Apache HTTP Server**: Salah satu web server open-source paling populer.
- **Nginx**: Terkenal karena performa tinggi dan efisiensi dalam menangani banyak koneksi.
- **Microsoft IIS (Internet Information Services)**: Web server bawaan Windows.
- **LiteSpeed**: Web server yang cepat dan kompatibel dengan banyak aplikasi.
- **Caddy**: Web server modern dengan konfigurasi minimal.


---

# Membuat Konfigurasi Revese Proxy

## Reverse Proxy untuk aplilkasi dumbflix-frontend dan implementasi penggunaan pm2
- Pertama-tama masuk ke folder nginx setelah itu buat suatu directory baru telebih dahulu, Setelah itu masuk ke directory yang sudah    
  kalian buat, setelah itu buat `file.conf`.
  
  ![rproxy-1](https://github.com/user-attachments/assets/52b3c085-3639-46a0-b4c2-8e05259cefea)

  ![rproxy-2](https://github.com/user-attachments/assets/4abaa63b-0eef-466c-b1e1-64ce32fee889)

- Masukkan script berikut:
  
  ``` plaintext
  server { 
    server_name zakky.xyz; 
  
    location / { 
             proxy_pass http://ip-vm-kita:3000;
    }
  }
  
   ```
  ![rproxy-3](https://github.com/user-attachments/assets/f50222b2-3494-4a41-b7fe-79c7fc729d0d)


- Selanjutnya keluar dari directory `jack`, masuk ke dalam file `nginx.conf` dan pergi ke-bagian include. Setelah itu masukan lokasi 
  dari directory yang berisi konfigurasi yang sudah kita buat tadi.

  ![rproxy-4](https://github.com/user-attachments/assets/4b25fc75-65a7-4eac-a821-c2ef075f5bc0)

  ![rproxy-5](https://github.com/user-attachments/assets/87a5ab9a-154d-4b63-b221-b71a7dc174c0)

- kemudian pastikan untuk melakukan pengecekan konfigurasi dengan menjalankan perintah 'sudo nginx -t`, Jika sudah kita  
  melakukan reload Nginx kita `sudo systemctl reload nginx`.

  ![rproxy-6](https://github.com/user-attachments/assets/7373607c-c3d2-4176-8e22-2fa78aeb6449)

- kita akan membuat sebuah virtual host. Untuk membuat virtual host kita harus masuk ke local server kita di windows
  setelah itu masuk ke dalam file hosts , lalu masukkan IP server kita selanjutnya masukkan nama domain.

  ![rproxy-7](https://github.com/user-attachments/assets/7562d28a-0515-4082-9238-cf70980b5f5d)

- Jika sudah sekarang coba buka web browser kita setelah itu coba akses nama domain.

  ![rproxy-8](https://github.com/user-attachments/assets/cbae07bb-7d35-47f8-9e44-685608800483)

  Vm/sever tempat kita menyimpan aplikasi sudah di logout (my-jack) dan tetap bisa jalan di browser, ini membuktikan pm2 sudah berjalan.
    

---

# Apa itu Load Balancing?

![loadbalace](https://github.com/user-attachments/assets/a9f594ec-b4f9-4e82-903d-e0100d7bb9d0)


**Load balancing** adalah proses mendistribusikan lalu lintas jaringan atau beban kerja aplikasi secara merata ke beberapa server. Tujuan utamanya adalah memastikan kinerja optimal, meningkatkan ketersediaan, dan mencegah kegagalan sistem akibat kelebihan beban pada satu server.


## Fungsi Utama Load Balancer
1. **Meningkatkan Kinerja**: Membagi beban secara merata sehingga setiap server dapat bekerja secara efisien.
2. **Toleransi Kegagalan**: Memastikan layanan tetap berjalan meskipun salah satu server mengalami masalah.
3. **Skalabilitas**: Mendukung penambahan server baru untuk menangani peningkatan beban lalu lintas.


## Cara Kerja Load Balancer
1. **Permintaan dari Klien**: Load balancer menerima semua permintaan yang masuk dari pengguna atau klien.
2. **Distribusi Permintaan**: Load balancer mendistribusikan permintaan ke server yang paling sesuai, berdasarkan algoritma tertentu.
3. **Pengembalian Respons**: Server yang dipilih memproses permintaan dan mengirimkan respons ke klien melalui load balancer.

---

## Jenis-Jenis Load Balancer
1. **Hardware Load Balancer**: Perangkat fisik yang dirancang khusus untuk load balancing, biasanya digunakan dalam skala besar.
2. **Software Load Balancer**: Aplikasi yang berjalan di server untuk menyediakan fungsi load balancing, seperti Nginx atau HAProxy.
3. **Cloud Load Balancer**: Layanan yang disediakan oleh platform cloud, seperti AWS Elastic Load Balancer atau Google Cloud Load Balancing.


## Algoritma Load Balancing
1. **Round Robin**: Permintaan diarahkan secara bergiliran ke server.
2. **Least Connections**: Permintaan diarahkan ke server dengan koneksi aktif paling sedikit.
3. **IP Hashing**: Permintaan diarahkan berdasarkan hash dari alamat IP klien.



## Keuntungan Load Balancing
- Meningkatkan kinerja aplikasi.
- Menjamin ketersediaan layanan (high availability).
- Mengoptimalkan penggunaan sumber daya server.
- Mendukung pertumbuhan bisnis dengan skalabilitas yang fleksibel.

Load balancing adalah bagian penting dari arsitektur sistem modern untuk memastikan pengalaman pengguna yang optimal dan menjaga 
keandalan layanan.

---

#  implementasi loadbalancing kepada aplikasi  dumbflix-frontend.

## menyiapkan vm baru lalu install nvm, node, dan cloning dumbflix-frontend
- menyiapkan vm baru

  ![lb-1](https://github.com/user-attachments/assets/4073cefa-fe54-4cb9-b35b-c1ac9edc9e35)

- install nvm,node dan npm, tetapi sebelum install kita melakukan update dan upgrade terlebih dahulu

  ![lb-2](https://github.com/user-attachments/assets/fa8a8dbd-f23c-4c37-8b14-21e5c68b7a17)

  ![lb-3](https://github.com/user-attachments/assets/6eb53b58-8123-48f8-a5cd-21a63526c021)

  ![lb-4](https://github.com/user-attachments/assets/be5f3b45-33f6-489b-8939-d7f0815ede08)

- menjalankan dumbflix-frontend dan mencoba nya di browser.

  ![lb-5](https://github.com/user-attachments/assets/0b339d3e-fb4f-4bb2-9cfc-6f3251d78370)

  ![lb-6](https://github.com/user-attachments/assets/3758415a-a229-4d45-a1da-a79dfe62faad)


## Membuat Konfigurasi Load Balancing
- Pertama-tama kita masuk ke dalam konfigurasi reverse proxy yang sudah kita buat sebelumnya.

  ![lb-7](https://github.com/user-attachments/assets/64a2443c-eef6-46c4-8988-a0e579c5d128)

- Tambahkan konfigurasi ke dalam file domen.conf. Kita akan tambahkan beberapa konfigurasi berikut:

  ```plaintext
  upstream domain { 
       server 172.29.56.104:3000;
       server 172.29.62.29:3000;
   }
   server { 
       server_name zakky.xyz; 
     
       location / { 
                proxy_pass http://domain;
       }
   }
   
  ```
  
  ![lb-8](https://github.com/user-attachments/assets/342f96cc-1395-4904-bcbe-645c6fd55624)

- Jika sudah sekarang kita cek apakah konfigurasi yang sudah kita buat tadi error atau tidak, lalu kita reload nginx kita karena kita 
  sudah menambahkan suatu konfigurasi baru di dalam file reverse proxy kita.

  ![lb-9](https://github.com/user-attachments/assets/7c4cf437-ce9b-4a96-bbfd-7a7cc7544210)

- Jika sudah sekarang  buka web browser kita setelah itu coba akses nama domain.

  ![lb-10](https://github.com/user-attachments/assets/6aad94bc-a600-4d94-8072-23ee8c8d01a2)



  

  






  


  




