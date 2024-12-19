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

- Sebelum install npm nya kita install downgrade dulu versi node nya ke v10 sesuai arahan dari repository baru setelah itu install       
  dependensi aplikasi `npm install`.

  ![depdumbflix-frontend-6](https://github.com/user-attachments/assets/e67211a1-f06a-4696-9dc8-e85952e10c51)

## Langkah 3 : Jalankan dan Akses Aplikasi
- Selanjutnya kita jalankan aplikasi nya dengan perintah `npm start` sesuai yang ada di dalam package.json

  ![depdumbflix-frontend-7](https://github.com/user-attachments/assets/6b1c5be6-f3bf-4b87-9327-00fef52db6df)

  ![homeworkhelpday5-1](https://github.com/user-attachments/assets/0dfef50a-6002-442e-8833-66a3af8f68d1)

- Setelah itu barulah kita buka di browser dan masukkan ip vm dan port 3000 tempat aplikasi itu berjalan `ip-vm-kita:3000`.

  ![depdumbflix-frontend-8](https://github.com/user-attachments/assets/76eb9803-8100-4e85-bf79-d517c7b38b49)


# Deploy Golang & Python dengan menampilkan nama masing-masing

## Langkah 1: Menyiapkan Golang dan Python
- Update dan install golang serta python di vm kita dengan perintah `sudo apt install -y golang python3-pip`.

  ![golangpython-1](https://github.com/user-attachments/assets/dac2a849-51be-4737-8528-8c48d444514f)

  ![golangpython-2](https://github.com/user-attachments/assets/6388b657-9178-4d78-b2aa-9a95faffc384)

- Verivikasi version golang dan python pip dengan perintah `go version` dan `pip --version`.

  ![golangpython-3](https://github.com/user-attachments/assets/304c2418-e016-4d3a-a858-6e59d4f366ba)

## Langkah 2: Buat Aplikasi Golang
- Buat direktori golang-app lalu buat file main.go.

  ![golangpython-4](https://github.com/user-attachments/assets/84e08dc7-7f7e-4acb-b642-0ec83ddaa422)

- Masukkan script ini kedalam file main.go:
  








  


  










