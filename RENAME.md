### PENGGUNAAN GIT 


### APA ITU GIT ?
* Git adalah salah satu sistem pengontrol versi (Version ControlSystem) pada proyek perangkat lunak yang diciptakan oleh Linux Torvalds.
* Pengontrol versi bertugas mencatat setiap perubahan pada fileproyek yang dikerjakan oleh banyak orang maupun sendiri.
* Git dikenal juga dengan distributed revision control (VCS terdistribusi),artinya penyimpanan database Git tidak hanya berada dalam satutempat saja.


### INSTALASI GIT
* Download **Git**, buka website resminya Git `(git-scm.com)`.
* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.
* Selamat, Git sudah terinstal di Windows. Untuk mencobanya,silahkan buka **CMD** atau **PowerShell**, kemudian ketik perintah

``git --version``

![Git version](https://user-images.githubusercontent.com/72736573/96331989-d382df00-108b-11eb-8745-bfabdace483a.PNG)



### Menambahkan Global Config
* Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi ``user.name dan user.email``
* konfigurasi ini bisa dilakukan untuk global repostiry atau individual repository.

* apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi kegagalan saat menjalankan perintah `git commit`

* Config Global Repository

`$ git config --global user.name “nama_user"`

`$ git config --global user.email “nama_user”`

![User name](https://user-images.githubusercontent.com/72736573/96332055-32e0ef00-108c-11eb-99dc-c82fe7183131.PNG)

### Perintah Dasar Git

* `git init`, perintah untuk membuat repository local
* `git add`, perintah untuk menambahkan file baru, atau perubahan pada file pada staging sebelum proses commit.
* `git commit`, perintah untuk menyimpan perubahan kedalam database git.
* `git push -u origin master`, perintah untuk mengirim perubahan pada repository local menuju server repository.
* `git clone [url]`, perintah untuk membuat working directory yang diambil dari repositry sever.
* `git remote add origin [url]`, perintah untuk menambahkan remote server/reopsitory server pada local repositry ``(working directory)``
* `git pull`, perintah untuk mengambil/mendownload perubahan terbaru dari server repository ke local repository


### Membuat Reposiory Local

* Buka direktory aktif, misal: **d:\labs_pemrograman1** (buka menggunakan Windows Explorer)
* klik kanan pada direktory aktif tersebut, dan pilih menu **Git Bash**, sehingga muncul git bash commad
* Buat direktory project praktikum pertama dengan nama **latihan1**
``$ mkdir latihan1
$ cd latihan1``
* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah **cd** ``(change directory)``
* direktory aktif menjadi: **d:\labs_pemrograman1\latihan1


### Membuat Reposiory Local

* Jalankan perintah **git init**, untuk membuat repository local.
`$ git init`
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .**git**
* Pada direktori tersebut, semua perubahan pada `working directory` akan disimpan.


### Menambahkan File baru pada repository

* Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository)
* disini kita akan coba buat satu file bernama README.md (text file)
`$ echo “# Latihan 1” >> README.md`
* File **README.md** berhasil dibuat.



### Menambahkan File baru pada repository

* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
`$ git add README.md`
* File **README.md** berhasil ditambahkan.

![git add](https://user-images.githubusercontent.com/72736573/96332142-b8fd3580-108c-11eb-8098-1abe3f1373e2.PNG)



### `Commit` (Menyimpan perubahan ke database)

* Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah git commit -m “komentar commit”
`$ git commit -m “File pertama saya”`
* Perubahan berhasil disimpan.

![git commit](https://user-images.githubusercontent.com/72736573/96332278-185b4580-108d-11eb-8bc6-bd635d806dd6.PNG)



### Membuat repository server

* Server reopsitory yang akan kita gunakan adalah (http://github.com)
* Anda harus membuat akun terlebih dahulu.
* Pada laman github, klik tombol start a project, atau
* Dari menu (icon +) klik New Repository

![membuat repository](https://user-images.githubusercontent.com/72736573/96332322-80119080-108d-11eb-823a-5bdde3104ab0.PNG)



### Membuat repository server

* Isi nama repositorynya, misal: labpy1.
* lalu klik tombol Create repository


### Menambahkan Remote Repository

* Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user.
* Untuk menambahkan remote repository server, gunakan perintah **git remote add origin [url]**
`$ git remote add origin https://github.com/rizkyy/Latihan-git.git`


### Push (Mengirim perubahan ke server)

* Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.
`$ git push -u origin master`
* Perintah ini akan meminta memasukkan username dan password pada akun github.com

![push](https://user-images.githubusercontent.com/72736573/96332376-d383de80-108d-11eb-8aa9-b24ae8b99af6.PNG)



### Melihat hasilnya pada server repository

* Buka laman github.com, arahkan pada repositorinya.
* Maka perubahan akan terlihat pada laman tersebut.

![Screenshot (41)](https://user-images.githubusercontent.com/66506609/95936958-eafa6780-0e00-11eb-85fa-262b7f92ef40.png)


### Clone Repository

* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory).
* Untuk melakukan cloning, gunakan perintah `git clone [url]`

![Screenshot (59)](https://user-images.githubusercontent.com/66506609/96254417-76c9ea80-0fdf-11eb-8af2-15adba4f4c33.png)

### Kegunaan file README.md

* Apabila kita menggunakan github, untuk memberikan penjelasan awal pada project yang kita buat, maka dapat menggunakan sebuah file yang bernama README.md
* Pada file tersebut kita dapat membuat dokumentasi awal dari setiap project yang kita buat untuk memberikan penjelasan atau sekedar cara penggunaan dari aplikasi yang kita kembangkan.
* Penulisan file README.md berbasis teks, dan untuk pemformatannya menggunakan Markdown format.
* untuk lebih jelasnya, dapat anda pelajari cara penggunaan markdown pada url berikut: https://guides.github.com/features/mastering-markdown/



### Author : Helmi Salasfazri
![giphy-preview](https://user-images.githubusercontent.com/66506609/96253867-8bf24980-0fde-11eb-841c-8b8a6ba0171f.gif)



