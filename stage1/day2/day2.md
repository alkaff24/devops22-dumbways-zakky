# Perintah - Perintah di Linux

Berikut adalah daftar perintah Linux yang sering digunakan beserta penjelasan dan contoh implementasinya.



## 1. **sudo**
`sudo` adalah perintah untuk memungkinkan menjalankan program sebagai pengguna lain (biasanya root) atau melakukan update.

 ![vm3 1](https://github.com/user-attachments/assets/1a57614a-4d9a-4aec-b255-be0fbe09a7ed)


## 2. **mkdir**
`mkdir` digunakan untuk membuat directory.

![vm3 2](https://github.com/user-attachments/assets/1c3ee3df-ce9b-47e6-8b4d-df8c4cba9520)


## 3. **ls**
`ls` digunakan untuk melihat daftar file dan directory.

![vm3 3](https://github.com/user-attachments/assets/176759cd-0cd8-4554-980e-1355c36a42ec)


## 4. **ls -la**
`ls -la` digunakan untuk melihat semua daftar file, termasuk yang tersembunyi, beserta detailnya.

![vm3 4](https://github.com/user-attachments/assets/572af670-2c42-467e-ac3e-acb9c3ce1778)



## 5. **cd**
`cd`  digunakan untuk masuk ke dalam directory.

![vm3 5](https://github.com/user-attachments/assets/63412bf6-602a-4b11-8a52-143891a3d117)



## 6. **cd ..**
`cd ..`  digunakan untuk keluar dari directory saat ini.

![vm3 6](https://github.com/user-attachments/assets/2aaa5d7e-6e7b-4917-85ed-5937bb634494)




## 7. **touch**
`touch`  digunakan untuk membuat file kosong baru.

![vm3 7](https://github.com/user-attachments/assets/0e52fe70-a4bd-4a87-8043-c407d1b14f9c)





## 8. **cp**
`cp`  digunakan untuk meng-copy file atau directory.

![vm3 8](https://github.com/user-attachments/assets/047d95f3-50a1-43d7-9732-70fb4b042ee8)



## 9. **mv**
`mv`  digunakan untuk memindahkan atau mengubah nama file/directory.

![vm3 9](https://github.com/user-attachments/assets/2ed94c1f-8db7-4ba2-a47e-5f9034b9e45c)



## 10. **echo**
`echo`  digunakan untuk menampilkan string atau menyisipkan teks ke file.

![vm3 10](https://github.com/user-attachments/assets/ce022033-e7a5-4fbf-a674-065c35124cd4)



## 11. **cat**
`cat`  digunakan untuk melihat isi file.

![vm3 11](https://github.com/user-attachments/assets/dbf3a6de-067e-4a66-a1d0-19b8ad58ab6b)



## 12. **find**
` find`   digunakan untuk mencari file atau directory.

![vm3 12](https://github.com/user-attachments/assets/f9721ad2-ad2f-431f-9444-4b5a45d41cc2)

## 13. **grep**
`grep` digunakan untuk mencari teks di file.

![vm3 13](https://github.com/user-attachments/assets/ae585fc6-88eb-40bf-b26f-b3148016acc1)


## 14. **chmod**
`chmod` digunakan untuk mengubah permission file/directory.

![vm3 14](https://github.com/user-attachments/assets/abee77a0-6b44-4063-8d2f-64b86b305116)



## 15. **chown**
`chown` digunakan untuk mengubah kepemilikan file/directory.

![vm3 15](https://github.com/user-attachments/assets/c58cb67d-ac1c-4100-ab26-3085e9ebac8f)





## 16. **history**
`history` digunakan untuk melihat riwayat perintah yang dijalankan.

![vm3 16](https://github.com/user-attachments/assets/e5bb8602-08ab-4cd2-b610-0b96cf2f2fde)




## 17. **ping**
`ping` digunakan untuk memeriksa koneksi internet.

![vm3 17](https://github.com/user-attachments/assets/3ca7a6cf-767c-48a6-8c5a-e9ecff894c23)




## 18. **wget**
`wget`  digunakan untuk mengunduh file.

![vm3 18](https://github.com/user-attachments/assets/94ab15c8-2b04-4019-8fc2-4b88bf3d36a0)




## 19. **unzip**
`unzip` digunakan untuk mengekstrak file zip, install unzip terlebih dahulu untuk menjalankan nya `sudo apt install unzip`.

![vm3 19](https://github.com/user-attachments/assets/b94be661-64c0-4849-ade4-4b69871bc77b)






## 20. **zip**
`zip`  digunakan untuk mengarsipkan/mengompres file/directory.

![vm3 20](https://github.com/user-attachments/assets/fdd8b6dc-fcfb-462c-b0b1-3cfd6cb614e7)







## 21. **adduser**
`adduser`  digunakan untuk membuat user baru.

![vm3 21](https://github.com/user-attachments/assets/b70790f9-cab3-4626-b003-0878ceec7bee)







## 22. **usermod**
`usermod`   digunakan untuk menambahkan user ke grup tertentu.

![vm3 22](https://github.com/user-attachments/assets/0aa3c7fa-6121-428b-a2b4-eb10890618a1)






## 23. **sudo su**
`sudo su`   digunakan untuk masuk sebagai root atau berpindah user.

![vm3 23](https://github.com/user-attachments/assets/e3fca02a-b3a4-436d-8db2-b01b04fa2ae3)







## 24. **rm**
`rm`   digunakan untuk menghapus file.

![vm3 24](https://github.com/user-attachments/assets/51b5d043-78c2-4258-ba7a-f24d77396980)





---





# Perbedaan IP Private & Public, serta IP Dynamic & Static

### Perbedaan IP Private dan IP Public



![ip-publicvsip-private](https://github.com/user-attachments/assets/ae3edd62-10b7-44e6-85af-bdda0d766af3)



**IP Private** adalah alamat IP yang digunakan dalam jaringan lokal (LAN) untuk komunikasi antar perangkat di dalam jaringan tersebut. IP ini tidak dapat diakses langsung dari internet dan digunakan untuk perangkat seperti komputer, printer, atau perangkat IoT di rumah atau kantor. Contohnya adalah rentang alamat IP seperti **192.168.x.x** atau **10.x.x.x**. IP Private ini secara otomatis disediakan oleh router dan tidak memerlukan biaya tambahan.

Di sisi lain, **IP Public** adalah alamat IP yang digunakan untuk mengidentifikasi perangkat secara global di internet. IP Public memungkinkan perangkat untuk diakses langsung melalui internet, seperti pada server web atau layanan online. Alamat IP ini diberikan oleh penyedia layanan internet (ISP) dan biasanya memerlukan biaya tambahan. IP Public digunakan untuk kebutuhan yang memerlukan akses internet langsung dan dapat dilihat oleh pengguna lain di internet.

Secara singkat, IP Private berfungsi untuk komunikasi internal dalam jaringan lokal, sementara IP Public digunakan untuk komunikasi di jaringan internet global.



### Perbedaan IP Dynamic dan IP Static

![staticvsdynamic](https://github.com/user-attachments/assets/bc1553bf-ff72-440f-81b9-c2a593eeefe6)



**IP Dynamic** adalah alamat IP yang diberikan secara otomatis oleh server DHCP (Dynamic Host Configuration Protocol). Alamat IP ini bersifat sementara dan dapat berubah setiap kali perangkat terhubung ke jaringan atau setelah masa "lease time" IP habis. IP Dynamic sering digunakan pada perangkat seperti komputer pribadi atau smartphone karena lebih fleksibel dan tidak memerlukan konfigurasi manual. IP Dynamic juga biasanya lebih aman, karena perubahan alamat IP membuat perangkat sulit dilacak.

Sebaliknya, **IP Static** adalah alamat IP yang tetap dan tidak berubah. Alamat ini dikonfigurasi secara manual oleh administrator jaringan atau diberikan oleh ISP. IP Static biasanya digunakan untuk server web, CCTV, atau perangkat yang memerlukan koneksi jarak jauh karena stabilitasnya. Namun, karena bersifat tetap, IP Static lebih rentan terhadap ancaman jika tidak dilindungi dengan baik.

Dalam penggunaan sehari-hari, IP Dynamic cocok untuk perangkat yang tidak memerlukan koneksi permanen, sementara IP Static lebih ideal untuk aplikasi yang membutuhkan alamat IP tetap, seperti hosting situs web atau server.


### Kesimpulan

- **IP Private** digunakan untuk komunikasi dalam jaringan lokal, sedangkan **IP Public** digunakan untuk identifikasi perangkat secara global di internet.  
- **IP Dynamic** lebih fleksibel dan berubah-ubah, sedangkan **IP Static** bersifat tetap dan cocok untuk aplikasi yang memerlukan stabilitas koneksi.




