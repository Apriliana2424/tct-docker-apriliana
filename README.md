# Docker 
> By : Apriliana Puspitasari

> 163210008

> Komputerisasi Akuntansi

---

[Deploying First Container](https://www.katacoda.com/courses/docker/deploying-first-container)

1. Perintah untuk menemukan image:

![1,2,3](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/1.png)
![1,2,3](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/2.png)
![1,2,3](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/3.png)

2. Untuk memulai run container :

![4](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/4.png)

3. PS Docker dapat mengelompokkan semua kontainer yang sedang berjalan, image yang digunakan dimulai ditampung dan waktu aktif.

![5](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/5.png)

4. Menjalankan Redis dengan nama redisHostPort pada port 6379:

![6](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/6.png)

5. Menggunakan opsi -p 6379 yang dimungkinkan untuk mengekspos Redis tetapi pada port yang tersedia secara acak :

![7](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/7.png)

6. Port yang digunakan oleh Jane :

![8](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/8.png)

7. Daftar kontainer dengan beberapa informasi dan pemetaan port:

![9](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/9.png)

8. Menyimpan data dan log ke dalam direktori. 
Data apa pun yang perlu, disimpan di Host Docker, dan bukan di dalam kontainer, harus disimpan di / opt / docker / data / redis.

![10](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/10.png)

9. Melihat semua proses yang berjalan dalam sebuah direktori.

![11](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/11.png)

10. Mendapatkan akses ke shell bash di dalam direktori.

![12](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/12.png)

---

[Create nginx Static Web Server](https://www.katacoda.com/courses/docker/create-nginx-static-web-server)

1. Create DockerFile
> Dockerfile adalah daftar instruksi yang menjelaskan cara mengembangkan aplikasi. Image yang digunakan saat ini versi Alpine dari Nginx.

![13](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/13.png)

2. Buat Docker Image
> Parameter -t memungkinkan untuk menentukan nama yang baik untuk image dan tag, yang biasa digunakan sebagai nomor versi.

![14](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/14.png)

3. Melihat daftar image di host:

![15](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/15.png)

4. Menjalankan Image Docker dengan menambahkan parameter -p, karena dalam web server maka menggunakan port 80.

![16](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/16.png)

5. Mengakses hasil port 80 melalui curl docker.

![17](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/17.png)

---

[Base Image](https://www.katacoda.com/courses/docker/2)

1. Membuat Base image yang dapat dikonfigurasikan dan berjalan di sistem sebelum dapat diterapkan dalam file HTML.

Membuat Base Image : NGINX.
> Dockerfile adalah file teks sederhana dengan perintah pada setiap baris.

![18](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/18.png)

2. Meng-COPY untuk menyalin index.html ke dalam direktori bernama /usr/share/nginx/html.
> COPY <src> <dest> memungkinkan untuk menyalin file dari direktori yang berisi Dockerfile ke image kontainer.

![19](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/19.png)

3. Penggunaan Port 80 dalam web server ini.
> Menggunakan perintah EXPOSE <port> dapat memberitahu Docker port mana yang harus dibuka dan dapat dijalankan. 
Dapat juga untuk menggunakan beberapa port pada satu perintah, misalnya, EXPOSE 80 433 atau EXPOSE 7000-8000.

![20](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/20.png)

4. Default Commands
Perintah yang digunakan untuk menjalankan aplikasi setelah port 80 sudah dipilih. Perintah untuk menjalankan NGINX adalah nginx -g

![21](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/21.png)

5. Mengambil direktori yang terdapat DockerFile untuk dapat disimpan dalam Docker Engine.

![22,23](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/22.png)
![22,23](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/23.png)

6. Menjalankan image baru berdasarkan ID yang sudah dibuat.

![24](https://github.com/Apriliana2424/tct-docker-apriliana/blob/master/images/24.png)

---

> -d untuk mengeksekusi direktori dalam keadaan terpisah.