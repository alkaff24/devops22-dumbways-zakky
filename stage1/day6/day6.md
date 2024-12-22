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

Load balancing adalah bagian penting dari arsitektur sistem modern untuk memastikan pengalaman pengguna yang optimal dan menjaga keandalan layanan.




