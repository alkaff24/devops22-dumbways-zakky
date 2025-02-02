# Task Terraform

![terraform-logo](https://github.com/user-attachments/assets/c1d232db-193c-4c19-9905-01887359e554)

## Instal Terrafform
- https://developer.hashicorp.com/terraform/install , install Terraform dengan mengikuti langkah di link ini.

## Install AWS cli
- Jalankan perintah berikut di terminal:
  
  ```plaintext
  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
  unzip awscliv2.zip
  sudo ./aws/install
  ```

## AWS configure cli
- Setelah instalasi, jalankan `aws configure`.
- Masukkan kredensial AWS yang diperoleh dari IAM :

  
```plaintext
  AWS Access Key ID [None]: xxxxxxxxxxxxxxxxx
  AWS Secret Access Key [None]: xxxxxxxxxxxxxxxxxxxxxxxxxx
  Default region name [None]: ap-southeast-1
  Default output format [None]: json
```

![terraform-1](https://github.com/user-attachments/assets/a1bad55d-d858-48a8-87f4-b3cc8cdd1ce0)


## Struktur file terraform 
- Berikut strukturnya :

  ```plaintext
  Automation  
  |  
  | Terraform  
  └── aws  
      ├── main.tf          # Konfigurasi utama (instance, EBS, EIP)  
      ├── providers.tf     # Konfigurasi provider AWS  
      ├── outputs.tf       # Output penting (IP, instance ID, dll.)  
      ├── vpc.tf           # Konfigurasi VPC dan subnet  
      ├── security.tf      # Aturan firewall (security group)  
      ├── storage.tf       # Konfigurasi block storage (EBS)  
  ```

## Membuat file main.tf
- Berikut file main.tf :
  
  ![terraform-2](https://github.com/user-attachments/assets/155c35a9-b348-4c8f-9c6d-7c905287dbbe)


## Membuat file providers.tf
- Berikut file providers.tf :

  ![terraform-3](https://github.com/user-attachments/assets/42b25f5a-515e-4447-9a50-5ecc79fbb8b8)


## Membuat file outputs.tf
- Berikut file outputs.tf :

  ![terraform-4](https://github.com/user-attachments/assets/4d1a09f7-c650-4209-a226-9e064bb187d8)


## Membuat file vpc.tf
- Berikut file vpc.tf :

  ![terraform-5](https://github.com/user-attachments/assets/4785b9f0-c72c-4baf-80ae-bf33ce6fb678)


## Membuat file security.tf 
- Berikut file security.tf :

  ![terraform-6](https://github.com/user-attachments/assets/dc89eed4-e995-4019-b052-d249e8dcda64)


## Membuat file storage.tf
- Berikut file storage.tf :

  ![terraform-7](https://github.com/user-attachments/assets/b737542d-93fe-451c-8c5e-8dc0a536fd09)


## Menjalankan Terraform
- Jika semua kebutuhan konfigurasi sudah siap maka kita jalan perintah-perintah berikut :
  ```plaintext
  terraform init
  terraform plan
  terraform apply -auto-approve
  ```

- Terraform berhasil membuat 2 buah server :

  ![terraform-8](https://github.com/user-attachments/assets/f53e6bc7-8f60-4460-ac98-8bc2eb2537b1)






  








