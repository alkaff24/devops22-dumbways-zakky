# Apa itu Git?

![gitlogo](https://github.com/user-attachments/assets/5a921eef-6e93-455e-8a24-ea5f63b33925)


**Git** adalah **sistem kontrol versi** (*version control system*) yang digunakan untuk melacak perubahan pada file, terutama dalam pengembangan perangkat lunak. Dengan Git, banyak orang dapat bekerja bersama pada satu proyek, mengelola perubahan, dan mengintegrasikan kontribusi mereka secara efisien.

## Fungsi Utama Git:
1. **Versi dan Riwayat**  
   Git menyimpan catatan setiap perubahan yang dibuat pada file, sehingga memudahkan untuk melihat riwayat modifikasi dan mengembalikan file ke versi sebelumnya jika diperlukan.

2. **Kolaborasi**  
   Banyak pengembang dapat bekerja pada proyek yang sama tanpa harus khawatir saling menimpa pekerjaan satu sama lain. Git menggabungkan perubahan dari banyak orang dengan cara yang terorganisasi.

3. **Branching dan Merging**  
   Git memungkinkan pengembang membuat cabang (*branch*) untuk mengerjakan fitur baru, memperbaiki bug, atau bereksperimen tanpa mengganggu kode utama. Setelah selesai, cabang tersebut bisa digabungkan kembali (*merge*) ke cabang utama.

4. **Penyimpanan Terdistribusi**  
   Tidak seperti sistem kontrol versi lainnya, setiap pengguna Git memiliki salinan lengkap dari repositori, sehingga pekerjaan tidak tergantung pada server pusat.

## Contoh Penggunaan Git:
1. **Pengembangan perangkat lunak**  
   Git digunakan untuk melacak kode sumber aplikasi oleh tim pengembang di seluruh dunia.
   
2. **Manajemen proyek**  
   Git dapat digunakan untuk melacak dokumen, catatan proyek, atau bahkan karya seni digital.

3. **Integrasi dengan platform seperti GitHub, GitLab, atau Bitbucket**  
   Platform ini memungkinkan pengembang menyimpan repositori Git mereka secara online, berkolaborasi, dan berbagi dengan mudah.

---

# Flow Cara Kerja Git

![gitworkflow](https://github.com/user-attachments/assets/afbb3e8d-9263-4b66-ac99-d91a5b9ebde1)


Berikut adalah alur kerja Git yang membantu dalam pengelolaan perubahan file dan kolaborasi proyek.

## 1. **Working Directory (Direktori Kerja)**
Di tahap ini, pengguna melakukan perubahan pada file proyek.  
- File bisa berupa *untracked* (belum dilacak oleh Git) atau *modified* (dimodifikasi).
- Semua pengeditan dilakukan di direktori kerja.

## 2. **Staging Area (Area Staging)**
Setelah perubahan selesai, file perlu ditambahkan ke *staging area*.  
- File yang ditambahkan berada dalam status *staged*.
- Area ini adalah tempat persiapan sebelum perubahan dikomit.

## 3. **Local Repository (Repositori Lokal)**
Perubahan dari *staging area* disimpan ke repositori lokal.  
- Komit menyimpan snapshot perubahan bersama pesan deskriptif yang menjelaskan perubahan tersebut.

## 4. **Branching (Pembuatan Cabang)**
Git memungkinkan Anda membuat cabang untuk mengerjakan fitur baru atau eksperimen tanpa memengaruhi cabang utama.  


## 5. **Merging (Penggabungan Cabang)**
Setelah pekerjaan selesai, cabang bisa digabungkan (*merge*) dengan cabang utama,  Ini memastikan perubahan baru terintegrasi ke versi stabil.


## 6. **Remote Repository (Repositori Jarak Jauh)**
Repositori jarak jauh memungkinkan kolaborasi melalui platform seperti GitHub, GitLab, atau Bitbucket.
- **Push:** Mengirim perubahan dari repositori lokal ke repositori jarak jauh.
- **Pull:** Mengambil pembaruan terbaru dari repositori jarak jauh.
- **Fetch:** Mengambil pembaruan tanpa langsung menggabungkannya ke cabang aktif.

## 7. **Kolaborasi**
Pengguna lain dapat mengunduh (*clone*) repositori untuk membuat kontribusi.  
- Perubahan bisa diajukan melalui *pull request* untuk ditinjau dan digabungkan.


## Alur Kerja Git (Ringkas):
  1. **Buat perubahan** di direktori kerja.
  2. **Tambahkan perubahan** ke *staging area*.
  3. **Commit perubahan** ke repositori lokal.
  4. **Push perubahan** ke repositori jarak jauh.
  5. **Pull pembaruan** dari repositori jarak jauh.
  6. Gunakan **branch** untuk pekerjaan paralel dan **merge** saat siap.

  Alur ini memastikan pengelolaan proyek yang terorganisasi, dengan kemampuan melacak setiap perubahan dan memfasilitasi kolaborasi tim secara efisien.


  ---

# Dasar Penggunaan Git

![git-terminal](https://github.com/user-attachments/assets/daac205d-da65-440d-bbee-686d4ebb838f)


## 1. **Git Installation**
Disini kita menggunakan VM linux maka kita tidak perlu install git. OS linux biasanya sudah tersedia git didalamnya,
karena yang menyiptakan OS linux beliau juga yang menyiptakan git yaitu bapak Linus Torvalds.

Maka dari itu kita lanjut ke verifikasi dan melihat version di git kita dengan perintah `git --version`.

![vmday3-1](https://github.com/user-attachments/assets/f586d556-80b7-41dd-a3d8-46457961d54b)



## 2. **Git Config**
Setelah instalasi, konfigurasikan identitas kita dengan perintah `git config --global user.name "Nama Kita"` dan `git config --global user.email "email@kita.com"`.

![vmday3-2](https://github.com/user-attachments/assets/71214957-8d55-4e7d-8a31-d11014212241)

Untuk melihat konfigurasi kita masukkan perintah `git config --list`.

![vmday3-3](https://github.com/user-attachments/assets/a576347a-a962-424c-86cd-8912c9a2bf01)



## 3. **SSH Key for GitHub**
**SSH key** berguna untuk mengintegrasikan antara repository local kita dengan platform github. 
Berikut perintah dan bagaimana cara untuk mengintegrasikan nya:

- Untuk mendapatkan **SSH key** kita dapat menggunakan perintah `ssh-keygen`.

  ![vmday3-4](https://github.com/user-attachments/assets/e181414e-582d-4f37-b305-470cfa832ec2)

- Jika kita sudah menjalankan perintah sebelumnya maka kita sudah berhasil untuk men-generate SSH key yang akan digunakan.
  Untuk lokasi SSH key yang sudah kita generate tadi berada di (.ssh/id_rsa.pub) lalu masukan perintah `cat .ssh/id_rsa.pub`.

  ![vmday3-5](https://github.com/user-attachments/assets/6ae6e43d-da17-45d4-aba0-2759ec6ffed7)
  

-  selanjutnya setelah kita melakukan copy SSH-key lalu memasukkannya kedalam config github dengan membuka https://github.com/settings/keys.

  ![vmday3-6](https://github.com/user-attachments/assets/2ad76bca-b34d-451f-9c31-6765426b9e4d)
  

- Setelah itu masukkan saja **SSH key** yang sudah kita copy tadi kebagian key. Jika sudah Langsung saja save dengan menge-klik bagian **Add SSH key**.

  ![vmday3-7](https://github.com/user-attachments/assets/f260d34a-399e-4cb3-a1e8-cd7b9c43ddca)

##


  ![vmday3-8](https://github.com/user-attachments/assets/a7229f06-29aa-4624-b69b-8dcd545a98b2)

- Jika kita sudah melakukan semua step di atas maka sudah berhasil meng-koneksikan local kita dengan Github.
  Untuk memastikan apakah sudah terkoneksi kita bisa menggunakan perintah `ssh -T git@github.com`.

  ![vmday3-9](https://github.com/user-attachments/assets/af092d18-f43c-4db9-8e9b-3e5c8d9407d7)


## 4. **Repository**
Membuat Repository Baru dengan perintah `git init`

![vmday3-10](https://github.com/user-attachments/assets/0ca453dd-0581-4b85-8ae0-80f8a7d98361)


## 5. **Git Ignore**
File .gitignore digunakan untuk mengabaikan file yang tidak ingin ditambahkan ke repositori.

![vmday3-11](https://github.com/user-attachments/assets/37082813-975a-4383-b0a5-7b935d289b37)


## 6. **Git Add dan Commit**
Menambahkan File:
- Tambahkan file spesifik:

  ![vmday3-12](https://github.com/user-attachments/assets/e7ed9325-4470-4cb2-acfc-61bd370615d9)

- Tambahkan semua file:

  ![vmday3-13](https://github.com/user-attachments/assets/8ce9e596-adcd-43f5-b9d9-789dcf4ca499)

Melakukan Commit:
- Simpan perubahan dengan pesan:

  ![vmday3-14](https://github.com/user-attachments/assets/cc916b1b-d929-43bc-9a2a-e4b1e7699bed)


## 7. **Git Remote**
Hubungkan repositori lokal dengan repositori jarak jauh:

![vmday3-15](https://github.com/user-attachments/assets/955b4194-7531-4f62-a559-7dce777819e3)

Lihat daftar repositori jarak jauh:

![vmday3-16](https://github.com/user-attachments/assets/77cbbdeb-360e-4b02-b9d0-67c1e95bf23a)


## 8. **Git Push**
Kirim perubahan ke repositori jarak jauh:

![vmday3-17](https://github.com/user-attachments/assets/8cb54cae-115d-4050-b1b7-d1c369e1e3e2)


## 9. **Git Branch**
Membuat Cabang Baru dan melihat semua branch:

![vmday3-18](https://github.com/user-attachments/assets/08ef94e7-4156-4ddd-8949-bc007db10fc4)

Berpindah ke Cabang:

![vmday3-19](https://github.com/user-attachments/assets/d470da91-906a-44cc-beb0-6f2255eb803c)


## 10. **Git Pull**
Ambil dan gabungkan pembaruan dari repositori jarak jauh:

![vmday3-20](https://github.com/user-attachments/assets/7fe5b48c-7f2a-41b5-afc9-4a80d7c34183)

## 11. **Git Merge**
Gabungkan perubahan dari cabang lain:

![vmday3-21](https://github.com/user-attachments/assets/f7fd6031-30b1-4272-b62c-c6186837d20d)

---

# **Case Git Konflik**
Ada 2 Developer yang sedang melakukan development aplikasi dari perusahaan A sebut saja Reyhan dan Teguh mereka kebetulan sedang mengerjakan suatu proyek yang sama, dan mereka sedang mengerjakan file yang sama index.html. Reyhan membuat perubahan pada file index.html dan melakukan commit: git add index.html;
git commit -m "fix: Typo on Description".  Teguh kebetulan juga membuat perubahan pada index.html dan melakukan commit: git add index.html ; git commit -m "feat: Header Adjustment". Kemudia disini ternyata Reyhan melakukan push ke repository. Teguh, yang belum melakukan push, mencoba untuk melakukan push ke repositori. Karena ternyata ada perubahan baru di remote yang belum dimiliki Teguh, Git menolak push Teguh dan memberi tahu bahwa ada konflik. Disini Teguh harus melakukan Fix Conflict tersebut agar perubahan yang di buat oleh Teguh dapat tersimpan ke dalam repositori app tersebut. lalu bagaimana cara menangani case yang dimiliki oleh Teguh?



  









  


  







  


  


