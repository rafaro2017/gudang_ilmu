# How to install Docker in Linux ( centos )
---
Docker dapat di pasang pada host environment Windows, Linux maupun MAC. Dengan fleksibilitasnya maka docker semakin populer di kalangan developer. Jika anda tertarik memasang docker pada environment yang anda miliki terutama linux Centos, maka panduan singkat ini dapat anda terapkan.

<br>

## Langkah - langkah yang dikerjakan
Anda hanya perlu melakukan sedikit langkah untuk memulai. Beberapa yang perlu dilakukan untuk memulai install docker pada environment linux (centos), diantaranya sebagai berikut :
### 1. Install paket yum-utils
>$ sudo yum install -y yum-utils
  
### 2. Menambahkan repository docker
>$ sudo yum-config-manager /\
>\> --add--repo \
>\> https://download.docker.com/linux/centos/docker-ce.repo [ENTER]
  
### 3. Jika repo sudah terpasang, maka selanjutnya lakukan installasi docker engine
>$ sudo yum install docker-ce docker-ce-cli containerd.io
<br>

### 4. Jika installasi berhasil, selanjutnya perlu mengaktifkan service docker terlebih dahulu
* Enable service
  * >$ sudo systemctl enable docker
  
* Start service
  * >$ sudo systemctl start docker
  
### NOTE : Untuk memastikan proses install dan service docker berhasil dijalankan, maka dapat menggunakan command berikut :
>$ sudo systemctl status docker
~~~
● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
     Active: active (running) since Mon 2020-12-14 08:14:42 UTC; 2s ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 2937 (dockerd)
      Tasks: 8
     Memory: 98.1M
     CGroup: /system.slice/docker.service
             └─2937 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock
~~~
  
## Troubleshoot 
### Jika terjadi konflik package pada saat installasi docker di Centos8, maka bisa menggunakan alternatif berikut :
>$ sudo dnf install docker-ce --nobest --allowerasing
  
# SELAMAT MENCOBA 

