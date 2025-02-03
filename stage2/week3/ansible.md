# Task Ansible

![ansible-logo](https://github.com/user-attachments/assets/907992c7-0732-4a3f-bb71-de8e232f94d8)

## Install Ansible
- Ikuti langkah install Ansible di link ini https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html

## Membuat file ansible.cfg
- Berikut file ansible.cfg :

  ![ansible1](https://github.com/user-attachments/assets/fef5d9f2-9414-4643-9660-e9af46305071)

## Membuat file inventory
- Berikut file inventory :

  ![ansible2](https://github.com/user-attachments/assets/0551bd6c-8e77-4cbd-8e15-d357560c4531)

## Membuat file group_vars/all
- Berikut file group_vars/all :

  ![ansible3](https://github.com/user-attachments/assets/fa40a346-ac9f-46ca-9203-3a6ae61948d3)

## Membuat file lolrandom1.yaml
- Berikut file lolrandom1.yaml :

  ![ansible4](https://github.com/user-attachments/assets/f79472c6-8b05-483a-b0cc-e39bae9893c6)

## Membuat file lolrandom2.yaml
- Berikut file lolrandom2.yaml :

  ![ansible5](https://github.com/user-attachments/assets/b80d2cf5-a03a-4dcb-a31d-7be82f8cc86e)

## Membuat file lolrandom3.yaml
- Berikut file lolrandom3.yaml :

  ![ansible6](https://github.com/user-attachments/assets/a07bed52-d29e-4ea7-837b-77436be371fe)

## Menjalankan ansible
- Menjalankan Setup User & SSH :
  `ansible-playbook lolrandom1.yaml`

- Menjalankan Menginstal Docker :
  `ansible-playbook lolrandom2.yaml`

- Menjalankan Deploy Frontend, Monitoring, Reverse Proxy, dan SSL :
  `ansible-playbook lolrandom3.yaml`




  

