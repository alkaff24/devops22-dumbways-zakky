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







  


  


