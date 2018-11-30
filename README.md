# Docker 
> By : Apriliana Puspitasari
> 163210008
> Komputerisasi Akuntansi

---

[Deploying First Container](https://www.katacoda.com/courses/docker/deploying-first-container)

1. Perintah untuk menemukan image:

![1,2,3]()

2. Untuk memulai run container :

![4]()

3. PS Docker dapat mengelompokkan semua kontainer yang sedang berjalan, image yang digunakan dimulai ditampung dan waktu aktif.

![5]()

4. Menjalankan Redis dengan nama redisHostPort pada port 6379:

![6]()

5. Menggunakan opsi -p 6379 yang dimungkinkan untuk mengekspos Redis tetapi pada port yang tersedia secara acak :

![7]()

6. Port yang digunakan oleh Jane :

![8]()

7. Daftar kontainer dengan beberapa informasi dan pemetaan port:

![9]()

8. Menyimpan data dan log ke dalam direktori. 
Data apa pun yang perlu, disimpan di Host Docker, dan bukan di dalam kontainer, harus disimpan di / opt / docker / data / redis.

![10]()

9. Melihat semua proses yang berjalan dalam sebuah direktori.

![11]()

10. Mendapatkan akses ke shell bash di dalam direktori.

![12]()

---

[Create nginx Static Web Server](https://www.katacoda.com/courses/docker/create-nginx-static-web-server)

1. Create DockerFile
> Dockerfile adalah daftar instruksi yang menjelaskan cara mengembangkan aplikasi. Image yang digunakan saat ini versi Alpine dari Nginx.

![13]()

2. Buat Docker Image
> Parameter -t memungkinkan untuk menentukan nama yang baik untuk image dan tag, yang biasa digunakan sebagai nomor versi.

![14]()

3. Melihat daftar image di host:

![15]()

4. Menjalankan Image Docker dengan menambahkan parameter -p, karena dalam web server maka menggunakan port 80.

![16]()

5. Mengakses hasil port 80 melalui curl docker.

![17]()

---

[Base Image](https://www.katacoda.com/courses/docker/2)

1. Membuat Base image yang dapat dikonfigurasikan dan berjalan di sistem sebelum dapat diterapkan dalam file HTML.

Membuat Base Image : NGINX.
> Dockerfile adalah file teks sederhana dengan perintah pada setiap baris.

![18]()

2. Meng-COPY untuk menyalin index.html ke dalam direktori bernama /usr/share/nginx/html.
> COPY <src> <dest> memungkinkan untuk menyalin file dari direktori yang berisi Dockerfile ke image kontainer.

![19]()

3. Penggunaan Port 80 dalam web server ini.
> Menggunakan perintah EXPOSE <port> dapat memberitahu Docker port mana yang harus dibuka dan dapat dijalankan. 
Dapat juga untuk menggunakan beberapa port pada satu perintah, misalnya, EXPOSE 80 433 atau EXPOSE 7000-8000.

![20]()

4. Default Commands
Perintah yang digunakan untuk menjalankan aplikasi setelah port 80 sudah dipilih. Perintah untuk menjalankan NGINX adalah nginx -g

![21]()

5. Mengambil direktori yang terdapat DockerFile untuk dapat disimpan dalam Docker Engine.

![22,23]()

6. Menjalankan image baru berdasarkan ID yang sudah dibuat.

![24]()

---

> -d untuk mengeksekusi direktori dalam keadaan terpisah.