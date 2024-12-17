# Perbandingan Monolith vs Microservices

![mnl-vs-mcrsv](https://github.com/user-attachments/assets/23316523-af08-4d42-932d-a16bb0e5d97b)



Arsitektur aplikasi dapat dibagi menjadi dua pendekatan utama: **Monolith** dan **Microservices**. Keduanya memiliki kelebihan dan kekurangan yang dapat memengaruhi pengembangan, pengelolaan, dan skalabilitas aplikasi.

## Monolith
Aplikasi Monolith adalah aplikasi yang dibangun sebagai satu kesatuan. Semua komponen seperti antarmuka pengguna, logika bisnis, dan akses database tergabung dalam satu basis kode. Pendekatan ini lebih sederhana untuk dikembangkan dan di-*deploy* pada awalnya. Namun, seiring bertambahnya kompleksitas aplikasi, Monolith menjadi sulit untuk diskalakan dan dipelihara karena setiap perubahan kecil memengaruhi keseluruhan aplikasi.

## Microservices
Microservices adalah arsitektur yang memecah aplikasi menjadi layanan-layanan kecil yang berdiri sendiri. Setiap layanan memiliki fungsionalitas spesifik, dapat dikembangkan secara independen, dan sering kali menggunakan teknologi yang berbeda. Pendekatan ini memungkinkan skalabilitas yang lebih baik dan pengembangan paralel oleh tim yang berbeda. Namun, Microservices memerlukan pengelolaan yang lebih kompleks, termasuk komunikasi antar layanan dan orkestrasi.

## Perbandingan Singkat
- **Struktur**: Monolith bersifat monolitik, sedangkan Microservices terdistribusi.
- **Skalabilitas**: Monolith sulit diskalakan secara parsial, sedangkan Microservices mendukung skalabilitas layanan secara independen.
- **Keandalan**: Kegagalan pada Monolith memengaruhi seluruh sistem, sementara pada Microservices, kegagalan satu layanan tidak berdampak pada layanan lain.
- **Kompleksitas**: Monolith sederhana di awal tetapi menjadi kompleks saat skala meningkat. Microservices kompleks sejak awal namun lebih terkontrol untuk aplikasi besar.

## Kesimpulan
Monolith cocok untuk aplikasi kecil atau sederhana, sedangkan Microservices lebih ideal untuk aplikasi besar yang memerlukan fleksibilitas, skalabilitas, dan pengembangan paralel.



# Deploy Aplikasi dumbflix-frontend (NodeJS)

## Langkah 1 : Update dan Install nvm dan nodejs di dalam VM
- Update vm kita dengan perintah `sudo apt update` dan `sudo apt uprade`.

  ![depdumbflix-frontend-1](https://github.com/user-attachments/assets/cf536319-19ed-4acf-9cd1-70d6de05cd9c)

- Install nvm kita dengan mengambil link di github nvm : `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash`
  , jika sudah selesai kita masukan perintah `exec bash` untuk mengaktifkan nvm, lalu verivikasi versi nvm dengan perintah `mvm -v`, lalu   insta nodejs `nvm i 20`.

  ![depdumbflix-frontend-2](https://github.com/user-attachments/assets/68135681-c31d-4f02-9176-43d9597eef87)

  ![depdumbflix-frontend-3](https://github.com/user-attachments/assets/37e130d8-e967-4a27-80a4-e8c5a59525cb)

  ![depdumbflix-frontend-5](https://github.com/user-attachments/assets/52fcb3bf-9477-4d34-9eb0-6f2a6b45d6f3)



## Langkah 2 : Clone dan Konfigurasi Aplikasi
- Clone repository Dumbflix-Frontend `git clone https://github.com/dumbwaysdev/dumbflix-frontend.git` dan masuk direktorinya
  `cd dumbflix-frontend`.

  ![depdumbflix-frontend-4](https://github.com/user-attachments/assets/b707df29-d001-4dde-ad45-eeedfc9565d8)

- sebelum install npm nya kita install downgrade dulu versi node nya ke v10 sesuai arahan dari repository baru setelah itu install       
  dependensi aplikasi `npm install`.

  ![depdumbflix-frontend-6](https://github.com/user-attachments/assets/e67211a1-f06a-4696-9dc8-e85952e10c51)

  


  










