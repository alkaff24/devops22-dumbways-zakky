# Apa Itu DevOps?

**DevOps** adalah kolaborasi dari **Development** dan **Operation** yang bertugas sebagai penghubung antara divisi **Development (Programmer)** dan **Operation (Infrastructure Server)**. Tujuan utamanya adalah untuk beradaptasi dengan cepat terhadap pembaruan maupun perubahan suatu produk, serta menghilangkan hambatan komunikasi antara tim Development dan Operation. Dengan demikian, proses **Deployment** menjadi lebih konsisten dan lancar.

![devops](https://github.com/user-attachments/assets/965946ae-c492-42d0-af19-d9ff6f68e919)

## Alur dan Fungsi Pekerjaan Seorang DevOps

Pekerjaan DevOps merupakan pekerjaan yang terus-menerus dengan alur kerja sebagai berikut:

1. **Plan**  
   Proses perencanaan untuk seluruh alur kerja yang dibutuhkan sebelum developers mulai menulis kode program.

2. **Code**  
   Tahap di mana developers mulai menulis kode yang dibutuhkan untuk membuat suatu produk.

3. **Build**  
   Aplikasi yang siap masuk ke tahap pengujian akan di-build untuk mengetahui apakah kode tersebut masih terdapat error atau sudah layak masuk ke divisi tester.

4. **Test**  
   Merupakan tahap pengujian fungsional aplikasi secara internal. Jika terdapat masalah fungsionalitas, akan dilaporkan ke tim developer untuk diperbaiki.

5. **Release**  
   Setiap perubahan kode yang telah melewati serangkaian pengujian dan dinyatakan lolos akan dirilis sebagai versi baru dari produk tersebut.

6. **Deploy**  
   Versi release yang telah dibuat akan digunakan untuk dijalankan di server, sehingga dapat diakses oleh publik.

7. **Operate**  
   Setelah aplikasi dijalankan di server, aplikasi tersebut dapat digunakan secara publik. Tim memastikan tidak ada masalah saat aplikasi diakses baik melalui HP maupun komputer.

8. **Monitor**  
   Tim Operations melakukan pemantauan infrastruktur, sistem, dan aplikasi untuk memastikan produk berjalan dengan lancar.

## Tujuan Proses DevOps
DevOps bertugas untuk membuat seluruh proses di atas menjadi otomatis agar:
1. **Mempercepat proses release ke publik.**  
2. **Menurunkan tingkat kegagalan pada rilisan terbaru.**  
3. **Mempersingkat waktu perbaikan.**

   
# Membuat Virtual Machine (VM) Ubuntu dengan Multipass di Windows

Berikut adalah langkah-langkah untuk membuat virtual machine berbasis Ubuntu menggunakan Multipass di Windows.



## Langkah 1: Install Multipass
1. **Download Multipass**  
   Unduh installer Multipass dari situs resmi Multipass: [https://multipass.run](https://multipass.run).

2. **Install Multipass**  
   Jalankan installer yang telah diunduh dan ikuti petunjuk untuk menyelesaikan proses instalasi.



## Langkah 2: Verifikasi Instalasi
1. Buka **Command Prompt** atau **PowerShell**.  
2. Jalankan perintah berikut untuk memastikan Multipass telah terinstal dengan benar:
   
   ![vm1 1](https://github.com/user-attachments/assets/0a3e2168-45ce-4427-8fb1-0616a4757f39)

    Jika instalasi berhasil, versi Multipass akan ditampilkan.


## Langkah 3: Buat Virtual Machine Ubuntu
1. Gunakan perintah berikut untuk membuat VM berbasis Ubuntu:
   
     ![vm1 2](https://github.com/user-attachments/assets/e3e9fc0d-4a95-467a-a633-34f1569920c6)

2. Contoh: Membuat VM dengan nama my-jack berbasis Ubuntu 22.04:
3. Tunggu beberapa saat hingga VM selesai dibuat. Jika image Ubuntu belum ada, Multipass akan otomatis mengunduhnya.


## Langkah 4: Akses Virtual Machine
1. Gunakan perintah berikut untuk mengakses VM yang telah dibuat:
   
     ![vm1 3](https://github.com/user-attachments/assets/6fa9754f-d292-4d45-899b-83b7398af886)


2. Anda sekarang berada di dalam VM berbasis Ubuntu dan dapat mulai menggunakannya.



# Cara Menginstal Apache2 WebServer di Virtual Machine (VM) yang Dibuat dengan Multipass

Ikuti langkah-langkah berikut untuk menginstal Apache2 WebServer ke dalam Virtual Machine (VM) yang telah dibuat dengan Multipass:

## Langkah 1: Akses Virtual Machine

- Jika kita belum masuk ke dalam VM, gunakan perintah berikut untuk mengaksesnya:
  
  ![vm2 1](https://github.com/user-attachments/assets/690007b6-7535-41d8-9598-29b728440e87)


## Langkah 2: Update Repositori Paket

- Sebelum menginstal Apache2, pastikan repositori paket di VM sudah diperbarui. Jalankan perintah berikut:

  ![vm2 2](https://github.com/user-attachments/assets/d59ab93a-1410-453b-b347-bcc58c093881)


## Langkah 3: Install Apache2

- Setelah repositori paket diperbarui, install **Apache2** **WebServer** dengan perintah:

  ![vm2 3](https://github.com/user-attachments/assets/945b4079-5413-4985-8e43-6c5275b850f3)



## Langkah 4: Verifikasi Instalasi

- Setelah proses instalasi selesai, kita dapat memverifikasi apakah Apache2 sudah berjalan dengan baik menggunakan perintah:

  ![vm2 4](https://github.com/user-attachments/assets/a02fa4a1-108d-4e54-8935-a483a1aa87a1)



## Langkah 5: Akses Web Server

- Untuk memastikan bahwa Apache2 berjalan dengan benar, buka browser dan ketik alamat IP dari VM Ubuntu kita. kita dapat mendapatkan alamat IP dengan perintah:

  ![vm2 5](https://github.com/user-attachments/assets/147c0ad1-e188-450d-9eff-b3f017874b72)

  
- Pada browser, buka alamat IP tersebut (misalnya, http://ip-vm-kita), dan kita akan melihat halaman default Apache2 yang menunjukkan bahwa web server berhasil diinstal.

  ![vm2 6](https://github.com/user-attachments/assets/c491d01a-7bd6-4f78-a97a-ba106a3fa188)




 

  
  


   


   

    

  

