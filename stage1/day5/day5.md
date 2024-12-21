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


---

# Deploy Golang, Python dan nodejs dengan menampilkan nama masing-masing

## Langkah 1: Menyiapkan Golang, Nodejs dan Python
- Update dan install golang serta python di vm kita dengan perintah `sudo apt install -y golang python3-pip`.

  ![golangpython-1](https://github.com/user-attachments/assets/dac2a849-51be-4737-8528-8c48d444514f)

  ![golangpython-2](https://github.com/user-attachments/assets/6388b657-9178-4d78-b2aa-9a95faffc384)

  ![depdumbflix-frontend-2](https://github.com/user-attachments/assets/68135681-c31d-4f02-9176-43d9597eef87)

  ![depdumbflix-frontend-5](https://github.com/user-attachments/assets/52fcb3bf-9477-4d34-9eb0-6f2a6b45d6f3)

- Verivikasi version golang dan python pip dengan perintah `go version`, `node -v` dan `pip --version`.

  ![golangpython-3](https://github.com/user-attachments/assets/304c2418-e016-4d3a-a858-6e59d4f366ba)

  ![depdumbflix-frontend-5](https://github.com/user-attachments/assets/52fcb3bf-9477-4d34-9eb0-6f2a6b45d6f3)

## Langkah 2: Buat Aplikasi Golang
- Buat direktori golang-app lalu buat file main.go.

  ![golangpython-4](https://github.com/user-attachments/assets/84e08dc7-7f7e-4acb-b642-0ec83ddaa422)

- Masukkan script ini kedalam file main.go:
  ```plaintext
  package main
  
  import (
      "fmt"
      "net/http"
  )
  
  func handler(w http.ResponseWriter, r *http.Request) {
      fmt.Fprintf(w, "Halo, nama saya Muhammad Jusuf Zakky. Ini adalah aplikasi Golang!")
  }
  
  func main() {
      http.HandleFunc("/", handler)
      fmt.Println("Server Golang berjalan di port 8080")
      http.ListenAndServe(":8080", nil)
  }
  
  ```

  ![golangpython-5](https://github.com/user-attachments/assets/2345c4b9-3bbd-4443-a382-2030875f1666)

- Jalankan aplikasi dengan perintah `go run main.go` dan akses aplikasi ke browser `ip-vm-kita:8080`.

  ![golangpython-6](https://github.com/user-attachments/assets/ad20e928-28d4-4a31-b11d-6f941a5c468a)

  ![golangpython-7](https://github.com/user-attachments/assets/8ad0ee16-cd5c-4fbc-9919-a4f8c535f2a9)


## Langkah 3: Buat Aplikasi Python
- Buat direktori python-app serta file app.py dan kita harus install flask dengan perintah `pip3 install flask`.

  ![golangpython-8](https://github.com/user-attachments/assets/97ab7f41-98aa-43ea-9775-211231eb0a64)

  ![golangpython-9](https://github.com/user-attachments/assets/f3437b01-319d-4d7f-ae41-4fbc5c30d3a3)


- Masukkan script ini ke dalam file app.py:

  ```plaintext
  from flask import Flask
  
  app = Flask(__name__)
  
  @app.route('/')
  def home():
      return "Halo, nama saya Muhammad Jusuf Zakky. Ini adalah aplikasi Python!"
  
  if __name__ == '__main__':
      app.run(host='0.0.0.0', port=5000)
  ```

  ![golangpython-10](https://github.com/user-attachments/assets/07e39129-ec16-4a57-9649-52a404a72c24)

- Jalankan aplikasi dengan perintah `python3 app.py` dan akses aplikasi ke browser `ip-vm-kita:5000`.

  ![golangpython-11](https://github.com/user-attachments/assets/fa0b94d5-9054-474f-b900-1283c1eb370f)

  ![golangpython-12](https://github.com/user-attachments/assets/1b9c8ab4-e369-493a-9728-9879ba705d0d)

## Langkah 4: Buat Aplikasi Nodejs Menggunakan Expressjs
- Buat direktori simple-app-node lalu memasukkan perintah `npm init -y` lalu instal npm dan expressjs `npm install express --save`

  ![gonodepy-1](https://github.com/user-attachments/assets/ad6e2140-aa7e-4ee1-898d-21af7c664aff)

  ![gonodepy-2](https://github.com/user-attachments/assets/5faf9807-e221-4e38-b6a9-43afc23afabf)

- Masukkan script ini kedalam file index.js:

  ```plaintext
  const express = require("express");
  const app = express();
  const port = 3001;
  
  app.get("/", (req, res) => {
    res.send("Halo, nama saya Muhammad Jusuf Zakky. Ini adalah aplikasi express js");
  });
  
  app.listen(port, () => {
    console.log(`Example app listening on port ${port}`);
  });
  
  ```

  ![gonodepy-3](https://github.com/user-attachments/assets/3c3b519e-df64-4a3d-af42-52e0d68fb69d)

- Jalankan aplikasi dengan perintah `node index.js` dan akses aplikasi ke browser `ip-vm-kita:3001`.

  ![gonodepy-4](https://github.com/user-attachments/assets/13620323-b34c-4b24-8ec6-2a1044f2c7d3)

  ![gonodepy-5](https://github.com/user-attachments/assets/f85a201b-f7db-43bf-ab1a-655422ded16d)


---

# Deploy Aplikasi dumbflix-frontend (NodeJS)

## Langkah 1: Clone dan Konfigurasi Aplikasi
- Clone repository Dumbflix-Frontend `git clone https://github.com/dumbwaysdev/dumbflix-frontend.git` dan masuk direktorinya
  `cd dumbflix-frontend`.

  ![depdumbflix-frontend-4](https://github.com/user-attachments/assets/b707df29-d001-4dde-ad45-eeedfc9565d8)

- Sebelum install npm nya kita install downgrade dulu versi node nya ke v10 sesuai arahan dari repository baru setelah itu install       
  dependensi aplikasi `npm install`.

  ![depdumbflix-frontend-6](https://github.com/user-attachments/assets/e67211a1-f06a-4696-9dc8-e85952e10c51)

## Langkah 2 : Jalankan dan Akses Aplikasi
- Selanjutnya kita jalankan aplikasi nya dengan perintah `npm start` sesuai yang ada di dalam package.json

  ![depdumbflix-frontend-7](https://github.com/user-attachments/assets/6b1c5be6-f3bf-4b87-9327-00fef52db6df)

  ![homeworkhelpday5-1](https://github.com/user-attachments/assets/0dfef50a-6002-442e-8833-66a3af8f68d1)

- Setelah itu barulah kita buka di browser dan masukkan ip vm dan port 3000 tempat aplikasi itu berjalan `ip-vm-kita:3000`.

  ![depdumbflix-frontend-8](https://github.com/user-attachments/assets/76eb9803-8100-4e85-bf79-d517c7b38b49)
  
# Deploy Aplikasi dumbflix-frontend Dengan Menggunakan Node v14

## Merubah Versi Node ke v14
- Masukkan perintah `nvm use 14` lalu install depedencies nya `npm instal`

  ![dumbv14-1](https://github.com/user-attachments/assets/ad72ae70-55c4-471f-b692-651c82cd7320)


- Setelah itu jalan kan dengan perintah `npm start` lanjut kita mengakses di browser kita `ip-vm-kita:3000`.

  ![dumbv14-2](https://github.com/user-attachments/assets/0874c2b6-9dfc-492e-9931-e810142b47a9)

  ![dumbv14-3](https://github.com/user-attachments/assets/145e712a-52bc-4239-9d16-a752c11eeb6a)

---


# Implementasi Penggunaan PM2 Agar Aplikasi Dapat Berjalan di Background
## Install pm2 
- Jalankan perintah `npm i pm2 -g`.

  ![pm2i](https://github.com/user-attachments/assets/fc2d26f7-4510-4766-ac7d-772e57b21ee7)



## Simple App Node
- Untuk menjalankan aplikasi Node.js menggunakan PM2, gunakan perintah `pm2 start index.js --name simple-app-node`, setelah itu masukkan   perintah `pm2 startup` dan `pm2 save`.

  ![pm2node-1](https://github.com/user-attachments/assets/b60c68e5-d723-4f59-bd90-52844013ea8e)

- Selanjutnya kita mencoba keluar dari vm kita dan mencoba di browser.

  ![pm2node-2](https://github.com/user-attachments/assets/ab5a0922-45f4-4fa5-8cfc-5da4c2e29bfc)

## python-app
- Untuk menjalankan aplikasi python-app menggunakan PM2, gunakan perintah `pm2 start python3 app.py --name python-app`, setelah itu        masukkan   perintah `pm2 startup` dan `pm2 save`.

  ![pm2py-1](https://github.com/user-attachments/assets/50babf9c-ea76-48b5-b40e-245c90ed78d8)

- Selanjutnya kita mencoba keluar dari vm kita dan mencoba di browser.

  ![pm2py-2](https://github.com/user-attachments/assets/66d5585d-8399-4255-a900-9d07ec9faaca)

## dumbflix-frontend
- Untuk menjalankan aplikasi dumbflix-frontend menggunakan PM2, gunakan perintah
  `pm2 start npm --name dumbflix-frontend -- start`, setelah itu masukkan   perintah `pm2 startup` dan `pm2 save`.

  ![pm2dumbfe-1](https://github.com/user-attachments/assets/f68be7f9-791c-46be-9eaa-b829e82dcc73)

  ![pm2dumbfe-2](https://github.com/user-attachments/assets/cf326ee7-3939-4585-aa50-1ff7658421a3)



- Selanjutnya kita mencoba keluar dari vm kita dan mencoba di browser.

  ![pm2dumbfe-3](https://github.com/user-attachments/assets/9df57468-5774-4396-bb41-82f91e40e4d9)


  



  

  

  



  



  








  


  










