# **Rangkuman Minggu Pertama**
## Unix Command Line
- ### Shell
  Shell adalah program yang digunakan untuk komunikasi antara user dan sistem operasi dan memberi perintah kepada sistem.
- ### CLI (Command Line Interface)
  jenis shell yang berbasis teks.
- ### Terminal
  terminal adalah penghubung antara user dan komputer, yang mewadahi shell.
- ### File System Structure
  cara sistem operasi mengatur file dan direktori dalam bentuk pohon(tree) filesystem mengatur bagaimana data disimpan di dalam sebuah system.
- ### Command
  - pwd (print working directory), untuk melihat current working directory
  - dir (directory), untuk melihat isi sebuah directory
  - cd (change directory), untuk berpindah directory
  - ls (list), untuk melihat isi files
  - touch, untuk membuat file directory
  - cp (copy), untuk menyalin file directory
  - mv (move), untuk memindahkan atau merename file directory
  - rm (remove), untuk menghapus file directory
  
## Git & Github Dasar
- ### Mengapa Git & Github adalah tools yang wajib digunakan?
  sebagai tools yang dapat mempermudah hidup karena dengan github kita bisa berkolaborasi dengan programmer lain
- ### Perbedaan Git & Github
  - Git adalah version controler digunakan untuk menyimpan, tracking, dan manajemen perubahan pada code yang kita buat saat pengembangan suatu aplikasi.
  - Github adalah penyedia layanan git
- ### Alur kerja dari Git dan Github
  - Pertama Buat branch/cabang di repository. Nama branch yang pendek dan deskriptif agar kolaborator dapat melihat pekerjaan yang sedang berlangsung secara sekilas.
  - Di branch, buat perubahan yang diinginkan pada repository.
  - Commit dan push perubahan ke branch. Berikan setiap commit pesan deskriptif untuk membantu kita dan kontributor masa depan memahami perubahan apa yang ada di commit.
- ### Membuat Repository Git
  Untuk Membuat repository pada git dapat dilakukan dengan command git init <nama_repo>
- ### Melakukan Commit pada Git
  Untuk Melakukan Commit pada git dapat dilakukan dengan command git commit, dengan menambahkan -m pada command dapat memberikan pesan saat commit
- ### Mempublish aplikasi ke Github
  Untuk mempublish aplikasi pada git dapat dilakukan dengan command git push -u origin, lalu tambahkan master/main tergantung dengan branch yg repo kita miliki
- ### Cloning Github ke Local
  Untuk cloning github ke local pada git dapat diakukan dengan command git clone (link repo yang ingin di cloning)
