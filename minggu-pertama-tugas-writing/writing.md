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
  - Terus buat commit, dan push perubahan ke branch hingga kita siap untuk meminta umpan balik.
  - Buat pull request untuk meminta masukan dari kolaborator tentang perubahan kita.
  - Saat membuat permintaan tarik, sertakan ringkasan perubahan dan masalah apa yang mereka pecahkan.
  - Alamat ulasan komentar. Reviewer harus meninggalkan pertanyaan, komentar, dan saran. Peninjau dapat mengomentari seluruh permintaan tarik atau menambahkan komentar ke baris tertentu.
  - Gabungkan pull request kita. Setelah permintaan tarik kita disetujui, gabungkan pull request kita. Ini akan secara otomatis menggabungkan branch kita sehingga perubahan kita muncul di branch default.
  - Hapus cabang kita. Setelah kita menggabungkan pull request kita, hapus branch kita. Ini menunjukkan bahwa pekerjaan di branch selesai dan mencegah kita atau orang lain menggunakan cabang lama secara tidak sengaja.
- ### Membuat Repository Git
  Untuk Membuat repository pada git dapat dilakukan dengan command git init <nama_repo>
- ### Melakukan Commit pada Git
  Untuk Melakukan Commit pada git dapat dilakukan dengan command git commit, dengan menambahkan -m pada command dapat memberikan pesan saat commit
- ### Mempublish aplikasi ke Github
  Untuk mempublish aplikasi pada git dapat dilakukan dengan command git push -u origin, lalu tambahkan master/main tergantung dengan branch yg repo kita miliki
- ### Cloning Github ke Local
  Untuk cloning github ke local pada git dapat diakukan dengan command git clone (link repo yang ingin di cloning)

## HTML
- ### HTML pada web development
  HTML adalah singkatan dari Hypertext Markup Language. HTML bersifat statis. HTML hanya bertugas menampilkan konten yang diminta oleh developer. HTML digunakan untuk menampilkan konten pada browser, mengelola serangkaian data dan informasi sehingga suatu dokumen dapat diakses dan ditampilkan di Internet.
- ### Tools HTML
  2 tools utama HTML antara lain code editor dan browser, adapun contoh code editor dan browser yang di anjurkan untuk html adalah Visual Studio Code, Dan Google Chrome
- ### HTML Sederhana
  ```html
  <html>
  <head>
  <title>
      Judul
    </title>
  <body>
      Isi body
    </body>
  </html>
  ```
- ### Live Server HTML
  untuk melakukan live server cukup dengan klik tombol live server pada vs code 
  ![live-server](https://user-images.githubusercontent.com/76435776/192291769-276b2072-f7f1-467b-8209-4eea4cd5ff88.png)

- ### Tag HTML yang populer
  - Tag HTML: Ini adalah akar dari dokumen HTML yang digunakan untuk menentukan bahwa dokumen tersebut adalah HTML.
  ```html
  <html> Statements... </html>
  ```
  - Tag head: Tag head digunakan untuk memuat semua elemen kepala dalam file HTML. Ini berisi judul, gaya, meta, ... dll.
  ```html
  <head> Statements... </head>
  ```
  - Tag Body: Ini digunakan untuk mendefinisikan tubuh dokumen HTML. Ini berisi gambar, tabel, daftar, ... dll.
   ```html
  <head> Statements... </head>
  ```
- ### Semantic HTML
  HTML semantik atau markup semantik adalah HTML yang memperkenalkan makna ke halaman web bukan hanya presentasi, contoh tag semantic antara lain
  - h1, h2, h3, h4, h5, dan h6 — kita dapat menggunakan tag heading untuk membuat font lebih besar dan lebih tebal, tetapi jika teksnya bukan heading, gunakan properti CSS font-weight dan font-size sebagai gantinya.
  ```html
  <h1> -- <h6>
  ```
- ### Tahap Deployment
  tahap penyebaran aplikasi agar orang lain bisa melihat website yang telah kita buat, deployment website bisa menggunakan netlify, cukup drag and drop folder website dan netlify akan langsung memprosesnya, dapat juga menggunakan github cukup hubungkan github dengan netlify
  
  
  ## CSS
- ### CSS pada web development
  Cascading Style Sheets (CSS) adalah bahasa style sheet yang digunakan untuk menggambarkan presentasi dokumen yang ditulis dalam bahasa markup seperti HTML atau XML.
- ### CSS ke dalam html
  kita bisa menyisipkan css ke dalam html melalui link
  ```html
  <link rel="stylesheet" href="mystyle.css">
  ```
- ### Sintaks dasar CSS
  contoh sintaks dasar css
  ```css
  p {
  color: red;
  text-align: center;
  }
  ```
  dengan menggunakan sintaks di atas maka akan mengubah warna teks menjadi merah dan rata tengah
- ### Styling CSS
  kita dapat melakukann styling CSS dengan 3 cara antara lain
  - Internal
  - External
  - Inline
  berikut contoh styling inline pada html
  ```html
    <!DOCTYPE html>
  <html>
  <head>
  <style>
  h1 {
    color: blue;
    font-family: verdana;
    font-size: 300%;
  }
  p {
    color: red;
    font-family: courier;
    font-size: 160%;
  }
  </style>
  </head>
  <body>

  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>

  </body>
  </html>
  ```
- ### Responsive web CSS
  Merancang Untuk Pengalaman Terbaik Untuk Semua Pengguna. Halaman web dapat dilihat menggunakan banyak perangkat berbeda: desktop, tablet, dan ponsel. Halaman web Anda akan terlihat bagus, dan mudah digunakan, apa pun perangkatnya.
  Membuat web responsive dapat menggunakan metode viewport
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```
  - Ini memberikan petunjuk kepada browser tentang cara mengontrol dimensi dan penskalaan halaman.
  - Bagian width=device-width mengatur lebar halaman untuk mengikuti lebar layar perangkat (yang akan bervariasi tergantung pada perangkat).
  - Bagian initial-scale=1.0 menyetel tingkat zoom awal saat halaman pertama kali dimuat oleh browser.
- ### Flexbox
  Flexbox adalah cara untuk mengatur layout. Flexbox memiliki kemampuan untuk menyesuaikan layout secara otomatis. kita dapat menggunakan flexbox untuk menyelaraskan elemen kita:
  ```css
  #container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
  padding: 10px;
  }
  ```


  ## Algoritma dan Struktur Data
- ### Perbedaan antara Algoritma dan Data Structures
  - Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk menyelesaikan suatu masalah
  - Struktur data adalah cara penyimpanan, pengorganisasian, dan pengaturan data di dalam media penyimpanan komputer sehingga data tersebut dapat digunakan secara efisien.
- ### Kenapa Algoritma dan Data Structure
  - Programming itu adalah algoritma dan struktur data
  - Data struktur digunakan untuk mengelola/manajemen sebuah data Dan Algoritma yang akan menyelesaikan suatu permasalahan menggunakan data tersebut.
- ### Algoritma Sederhana
  contoh algoritma sederhana dapat dimulai dari kehidupan kita sehari hari contohnya algoritma saat mengecas hp
  - Jika ponsel telah menandakan kekurangan daya segera ambil charger.
  - Selanjutnya pasang cas ponsel ini pada stop kontak atau colokan, pastikan pasang dengan benar.
  - Bila telah menunjukkan penambahan daya silahkan tunggu hingga penuh dengan menjalankan aktivitas lain.
- ### Algoritma ke dalam bahasa pemrograman
  - Mulai
  - Deklarasikan variable a,b,c
  - Read isi a,b,c
  - Tambahkan a dengan b lalu masukkan ke c
  - Tampilkan c
  - Stop
  ```javascript
  var a,b,c;
  a = prompt ("Angka Pertama");
  b = prompt ("Angka Kedua");
  c = Angka(a) + Angka(b);
  console.log(c);
  alert("Result = " + c);
  ```
- ### Big O Notation
  Adalah sebuah cara atau metode untuk melakukan analisa terhadap sebuah algoritma pemrograman terhadap waktu eksekusi. Tentang seberapa efisien dan kompleksitas barisan kode dalam dimensi waktu.
- ### Menyelesaikan suatu masalah untuk diselesaikan melalui program
  Pada program di bawah Kita hanya akan mengambil data yang hanya habis dibagi dua saja
  ```javascript
  const angka = [1, 2, 3, 4, 5, 6, 7, 8, 9];
  
  const filteredArray = angka.filter((item) => {return item % 2 === 0});

  console.log(filteredArray) // -> [2, 4, 6, 8]
  ```
  konstanta angka 1 - 9, lalu {return item % 2 === 0}, maka tampilkan 2,4,6,8
- ### Algoritma dengan JavaScript
  ```javascript
  var a,b,c;
  a = prompt ("Angka Pertama");
  b = prompt ("Angka Kedua");
  c = Angka(a) + Angka(b);
  console.log(c);
  alert("Result = " + c);
  ```
  - a = Angka pertama
  - b = Angka kedua
  - c = trigger
- ### Struktur Data dengan JavaScript
  ```javascript
  var buah = ["Apel", "Jeruk", "Manggis"];
  ```
  Apel, Jeruk, dan Manggis terhitung sebagai data dalam algoritma di atas 
