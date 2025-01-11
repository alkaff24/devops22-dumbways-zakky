# 1.Server

## Membuat pengguna baru untuk semua server kita
- pertama kita menaruh ssh-key dari cloud ke lokal kita di dalam direktori `ssh`. 

  ![server1](https://github.com/user-attachments/assets/528a1a55-df30-4394-98b6-34aaf08cac59)

- lalu kita masuk kedalam server kita di cloud dengan perintah `ssh -i file-ssh username@ip-server`.

  ![server2](https://github.com/user-attachments/assets/4aa17a05-946c-4a54-9295-66821043f245)

  ![server3](https://github.com/user-attachments/assets/5b7a59da-3c54-4eb2-9b0d-8f5e41bc4c61)

- Selanjutnya barulah kita membuat user baru di dalam server kita dengan perintah `sudo adduser username` serta kita memberi akses root
  pada user baru kita dengan perintah `sudo usermod -aG sudo username` dan masuk ke dalam user baru dengan perintah `sudo su username`.

  ![server4](https://github.com/user-attachments/assets/dfb97f6e-aede-46e6-bfb8-2538fc43a56c)

  ![server5](https://github.com/user-attachments/assets/e43d15c0-8ef2-4a80-bbec-d94f15014611)

##  Server dapat masuk dengan kunci SSH dan kata sandi 
- Langkah pertama kita merubah PasswordAuthentication pada file 60-cloudimg-settings.conf di dalam direktori `/etc/ssh/sshd_config.d`

  ![server6](https://github.com/user-attachments/assets/5170644b-0c51-41d7-b84f-7ed1ab3c0dcf)

- Berikutnya kita uncomment PubkeyAuthentication yes dan PasswordAuthentication yes pada file sshd_config di dalam direktori
  `/etc/ssh`.

  ![server7](https://github.com/user-attachments/assets/bd1b92f9-a173-4c5c-b3f3-676100f96a5f)

- Barulah kita bisa mengakses server dengan password kita yang ada di cloud dan juga bisa menggunakan ssh-key.

  ![server8](https://github.com/user-attachments/assets/7c3e04e5-3682-4b51-949c-f5a62cbc858c)

  ![server9](https://github.com/user-attachments/assets/81778fe5-18a3-466d-a90f-5a7a21b35b75)







  

