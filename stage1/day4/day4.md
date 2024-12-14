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
  ```bash
  cat file-name
  ```

- **Membuat file baru dan menambahkan teks**
  ```bash
  cat > file-name
  ```
  *Keterangan: Setelah menambahkan teks, keluar dengan menekan `Ctrl + C`.*

- **Menggabungkan dua file menjadi satu**
  ```bash
  cat file1 file2 > file3
  ```
  *Keterangan: Menggabungkan `file1` dan `file2` menjadi `file3`.*

### 2. sed
`sed` adalah singkatan dari *stream editor*. Gunanya untuk memanipulasi teks dasar pada file. Dengan `sed`, kita dapat mengganti teks dengan cepat.

#### Contoh Penggunaan:
- **Mengganti teks dalam file**
  ```bash
  sed -i 's/Hello/Holla/g' file3
  ```
  *Keterangan: Mengganti semua kata "Hello" menjadi "Holla" pada `file3`.*

### 3. grep
`grep` digunakan untuk mencari teks dalam file.

#### Contoh Penggunaan:
- **Mencari teks dalam file**
  ```bash
  grep Dumbways file3
  ```
  *Keterangan: Mencari kata "Dumbways" pada `file3`.*

- **Menghitung jumlah kemunculan kata**
  ```bash
  grep -c Dumbways file3
  ```
  *Keterangan: Menghitung jumlah kata "Dumbways" pada `file3`.*

- **Mencari kata di semua file dalam direktori**
  ```bash
  grep Dumbways *
  ```
  *Keterangan: Mencari semua file yang berisi kata "Dumbways".*

### 4. sort
`sort` digunakan untuk mengurutkan data, baik secara ascending maupun descending.

#### Contoh Penggunaan:
- **Mengurutkan data secara ascending**
  ```bash
  sort file4
  ```

- **Mengurutkan data secara descending**
  ```bash
  sort -r file4
  ```

### 5. echo
`echo` digunakan untuk mencetak string atau pesan ke stdout atau file.

#### Contoh Penggunaan:
- **Mencetak string ke layar**
  ```bash
  echo "Hello Dumbways!"
  ```

- **Menambahkan string ke file**
  ```bash
  echo "Hello Dumbways!" >> file3
  ```

- **Mengganti isi file dengan string baru**
  ```bash
  echo "Replace semua data" > file5
  ```
  *Keterangan: Menghapus semua data di `file5` dan menggantinya dengan "Replace semua data".*

  ---

## Dokumentasi Shortcut Text Editor Nano

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
  ```bash
  cat file-name
  ```

- **Membuat file baru dan menambahkan teks**
  ```bash
  cat > file-name
  ```
  *Keterangan: Setelah menambahkan teks, keluar dengan menekan `Ctrl + C`.*

- **Menggabungkan dua file menjadi satu**
  ```bash
  cat file1 file2 > file3
  ```
  *Keterangan: Menggabungkan `file1` dan `file2` menjadi `file3`.*

### 2. sed
`sed` adalah singkatan dari *stream editor*. Gunanya untuk memanipulasi teks dasar pada file. Dengan `sed`, kita dapat mengganti teks dengan cepat.

#### Contoh Penggunaan:
- **Mengganti teks dalam file**
  ```bash
  sed -i 's/Hello/Holla/g' file3
  ```
  *Keterangan: Mengganti semua kata "Hello" menjadi "Holla" pada `file3`.*

### 3. grep
`grep` digunakan untuk mencari teks dalam file.

#### Contoh Penggunaan:
- **Mencari teks dalam file**
  ```bash
  grep Dumbways file3
  ```
  *Keterangan: Mencari kata "Dumbways" pada `file3`.*

- **Menghitung jumlah kemunculan kata**
  ```bash
  grep -c Dumbways file3
  ```
  *Keterangan: Menghitung jumlah kata "Dumbways" pada `file3`.*

- **Mencari kata di semua file dalam direktori**
  ```bash
  grep Dumbways *
  ```
  *Keterangan: Mencari semua file yang berisi kata "Dumbways".*

### 4. sort
`sort` digunakan untuk mengurutkan data, baik secara ascending maupun descending.

#### Contoh Penggunaan:
- **Mengurutkan data secara ascending**
  ```bash
  sort file4
  ```

- **Mengurutkan data secara descending**
  ```bash
  sort -r file4
  ```

### 5. echo
`echo` digunakan untuk mencetak string atau pesan ke stdout atau file.

#### Contoh Penggunaan:
- **Mencetak string ke layar**
  ```bash
  echo "Hello Dumbways!"
  ```

- **Menambahkan string ke file**
  ```bash
  echo "Hello Dumbways!" >> file3
  ```

- **Mengganti isi file dengan string baru**
  ```bash
  echo "Replace semua data" > file5
  ```
  *Keterangan: Menghapus semua data di `file5` dan menggantinya dengan "Replace semua data".*

---

## Case Manipulasi Teks: Formula 1 Drivers

### Deskripsi
Anda bekerja di sebuah tim data analis untuk sebuah situs web yang menampilkan data pembalap Formula 1. Data pembalap disimpan dalam sebuah file teks `formula-one-drivers.md` dengan format berikut:

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
Gunakan perintah `sed` untuk mengganti teks pada kolom Tim:

```bash
sed -i 's/Red Bull Racing/Red Bull Racing Honda/g' formula-one-drivers.md
```

#### Penjelasan:
- **`-i`**: Mengedit file secara langsung.
- **`s/old/new/g`**: Mengganti semua kemunculan `old` ("Red Bull Racing") dengan `new` ("Red Bull Racing Honda").
- **`g`**: Global, untuk memastikan semua kemunculan dalam baris diganti.

### 2. Menghapus seluruh baris dengan posisi lebih dari 3
Gunakan `sed` untuk mencocokkan dan menghapus baris berdasarkan kolom Posisi (lebih dari 3):

```bash
sed -i '/,[4-9],/d' formula-one-drivers.md
```

#### Penjelasan:
- **`/pattern/d`**: Mencocokkan pola tertentu dan menghapus baris tersebut.
- **`,[4-9],`**: Mencari angka 4 hingga 9 yang berada di antara koma. Ini mencocokkan kolom Posisi untuk nilai lebih dari 3.
- **`-i`**: Mengedit file langsung.

### Hasil Akhir
Setelah menjalankan kedua perintah di atas, isi file `formula-one-drivers.md` akan menjadi:

```plaintext
ID,Nama,Tim,Posisi,Gaji
001,Lewis Hamilton,Mercedes,1,70000000
002,Max Verstappen,Red Bull Racing Honda,2,50000000
003,Sergio Perez,Red Bull Racing Honda,3,25000000
```











