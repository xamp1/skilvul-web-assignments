# _Tugas Rangkuman Minggu Keempat_</p>
## Git & Github Lanjutan
  - ### Git Branch
    Branch adalah bifurkasi dari kondisi kode yang membuat alur baru bagi evolusinya. Branch ini dapat dipararelkan ke Git branch lain yang kita buat. Branch umum digunakan saat kita akan menambahkan fitur baru atau memperbaiki bug. Penggunaan branch bertujuan agar perubahan tidak mengganggu file master.
    - #### Membuat Branch dapat dilakukan seperti berikut:
      ```
      git branch nama-branch
      ```
    - #### Mengganti atau berpindah Branch dapat dilakukan seperti berikut:
      ```
      git checkout nama-branch
      ```
    - #### Menggabungkan Branch dapat dilakukan seperti berikut:
      ```
      git merge nama-branch
      ```
    - #### Menggabungkan Branch dapat dilakukan seperti berikut:
      ```
      git merge nama-branch
      ```
    - #### Menghapus Branch dapat dilakukan seperti berikut:
      ```
      git branch -d nama-branch
      ```
  - ### Pull Request
    Pull Request adalah suatu permintaan untuk menggabungkan (merge) kode yang kita modifikasi dengan repositori utama atau repositori lain.
    - #### Melakukan Pull Request dapat dilakukan dengan langkah-langkah berikut:
      ```
      - Login Git.
      - Baca Aturan Berkontribusi.
      - Buat Repository.
      - Tambahkan File ke Repository.
      - Fork dan Clone Repository.
      - Lakukan Modifikasi.
      - Push Kontribusi.
      - Membuat Pull Request.
      ```
    - #### Menerima Pull dapat dilakukan dengan langkah-langkah berikut:
      ```
      - Buka repository Github
      - Pilih tab Pull Request
      - Pilih pull request yang akan diterima
      - Klik tombol Merge Pull Request
      - Klik tombol Confirm Merge
      ```
    - #### Mengatasi terjadinya konflik
    Konflik pada github biasanya terjadi karena perubahan kode pada line yang sama dan dilakukan oleh dua orang berbeda. adapun konflik lainnya yaitu konflik pada local repository berikut cara mengatasinya
    - #### Mengatasi konflik yang terjadi pada github
      ```
      - Buka repository Github
      - Pilih tab Pull Request
      - Pilih pull request yang akan diterima
      - Klik tombol Resolve Conflicts
      - Atur perubahan kode yang dilakukan oleh kedua orang tersebut
      - Klik tombol Mark as Resolved
      - Klik tombol Commit Merge
      ```
    - #### Mengatasi terjadinya konflik pada repository local
      ```
      - Buka repository lokal
      - Lakukan Pull
      - Lakukan perubahan kode yang dilakukan oleh kedua orang tersebut
      - Lakukan commit perubahan kode
      - Push perubahan kode ke Github
      ```
  - ### Berkolaborasi Dengan Orang Lain
    - #### Mengundang orang lain
      ```
      - Buka repository Github
      - Pilih repsitory
      - Pilih tab Settings
      - Pilih tab Collaborators
      - Ketik username orang yang akan diundang
      - Klik tombol Add Collaborator
      ```
    - #### Bergabung dengan orang lain
      ```
      - Pilih repository Github
      - Klik tombol Fork
      - Pilih akun Github yang akan dijadikan tempat fork repository
      - Klik tombol Fork Repository
      ```
## Responsive Web Design
RWD atau Responsive Web Design adalah sebuah teknik atau metode bagi web designer untuk membuat suatu layout website yang dapat menyesuaikan diri sesuai dengan ukuran layar pengguna. Secara singkat RWD bertujuan untuk membuat desain website dapat di akses oleh device manapun (Universal)
  - ### Tools Untuk Membuat Website Responsive
    Salah satu tools yang dapat digunakan untuk Membuat website responsif dapat menggunakan Bootstrap. Bootstrap adalah framework CSS gratis dan open-source yang ditujukan untuk pengembangan web front-end yang responsif dan mobile-first. Ini berisi template desain berbasis HTML, CSS dan JavaScript untuk tipografi, formulir, tombol, navigasi, dan komponen antarmuka lainnya. Bootstrap menyediakan toolkit dari berbagai elemen yang Anda butuhkan untuk membangun situs web responsif dan memungkinkan kita memilih dan memilih elemen yang ingin kita sertakan di halaman Anda untuk membuat prototipe menjadi intuitif.
  - ### Viewport
    Viewport merupakan area yang dapat dilihat oleh pengguna kita pada halaman website. Ukuran viewport bervariasi berdasarkan peranti. Ukuran viewport pada sebuah peranti mobile, lebih kecil dibandingkan dengan layar komputer.
    - #### Menambahkan Viewport pada html
      ```html
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      ```
  - ### Satuan Relatif CSS
      - ```em``` Relatif terhadap ukuran font elemen (2em berarti 2 kali ukuran font saat ini)
      - ```ex``` Relatif terhadap x-height dari font saat ini (jarang digunakan)
      - ```ch``` Relatif terhadap lebar "0" (nol)
      - ```rem``` Relative to font-size of the root element
      - ```vw``` Relatif terhadap 1% dari lebar viewport*
      - ```vh``` Relatif terhadap 1% dari ketinggian viewport*
      - ```vmin``` Relatif terhadap 1% dari area pandang* dimensi yang lebih kecil
      - ```vmax``` Relatif terhadap 1% dari viewport* dimensi yang lebih besar
      - % Relatif terhadap elemen induk
  - ### Media Query
Media query adalah teknik CSS yang diperkenalkan di CSS3. Media Query menggunakan aturan @media untuk menyertakan blok properti CSS hanya jika kondisi tertentu benar.
Media query memiliki dua jenis yaitu min-width dan max-width.
  - Contoh Media Query
    ```css
    @media only screen and (max-width: 600px){
    body {
    background-color: lightblue;
    }
    }
    ```
    Jika browser window 600px atau lebih kecil, maka background color akan menjadi lightblue
- ### Flexbox & Grid
    - Flexbox merupakan sebuah mode pengaturan atau konsep layout pada CSS yang digunakan untuk mengatur elemen atau container beserta item didalamnya pada halaman web.
    - Grid adalah jenis layout yang dimana peletakan barang berada dalam baris-baris panjang pada sebuah toko. Penggunaan grid layout adalah pilihan yang tepat jika Anda ingin konsumen mampu menjelajahi seluruh isi toko dengan mengalir di antara rak-rak barang tersebut.
    - #### Contoh Penggunaan Flexbox
      ```html
      <div class="flex-container">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      </div>
      ```
      Flex Container dengan 3 Flex Item
    - #### Contoh Penggunaan Grid
      ```css
      .menu {
      width: 25%;
      float: left;
      }
      .main {
      width: 75%;
      float: left;
      }
      ```
      Membuat kelas menu selebar 25% dan main 75%
## Bootstrap
Bootstrap adalah framework front-end gratis yang cukup populer di kalangan developer saat ini, khususnya yang bekerja di bidang desain web. Framework ini mudah digunakan dan membantu developer bekerja lebih cepat tanpa harus menulis kode HTML, CSS, dan JavaScript secara manual.Selain itu, Bootstrap merupakan framework yang fleksibel dan mampu membantu hampir semua proses web development front-end. Fitur terbaiknya adalah template desain yang mengoptimalkan performa halaman web di semua ukuran layar. Tujuan dan fungsi Bootstrap adalah untuk membuat website responsive dan mobile-first. Jadi, semua elemen antarmuka website dipastikan bisa bekerja secara optimal di semua ukuran layar, baik desktop maupun perangkat seluler.
  - ### Menggunakan Bootstrap
    ```html
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    ```
    Dengan melakukan link seperti yang di atas kita sudah dapat menggunakan Bootstrap
  - ### Layout Pada Bootstrap
    - #### Breakpoint
      Breakpoints adalah titik di mana terjadi perubahan aturan. Bootstrap memiliki 5 Breakpoint antara lain:
      ```scss
      $grid-breakpoints: (
      xs: 0,
      sm: 576px,
      md: 768px,
      lg: 992px,
      xl: 1200px,
      xxl: 1400px
      );
      ```
      Setiap breakpoint dipilih untuk menampung container dengan lebar kelipatan 12 dengan nyaman. Breakpoint juga mewakili subset ukuran perangkat umum dan dimensi area pandang—tidak secara khusus menargetkan setiap kasus penggunaan atau perangkat. Sebaliknya, rentang memberikan fondasi yang kuat dan konsisten untuk dibangun di hampir semua perangkat.
    - #### Container
      Containers adalah element layout yang paling dasar pada bootstrap. Wadah adalah elemen tata letak paling dasar di Bootstrap dan diperlukan saat menggunakan sistem grid default kita. Wadah digunakan untuk menampung, melapisi, dan (terkadang) memusatkan konten di dalamnya. Meskipun container dapat disarangkan, sebagian besar tata letak tidak memerlukan container nested.
      ```html
      <div class="container-sm">lebar 100% hingga titik putus kecil</div>
      <div class="container-md">lebar 100% hingga breakpoint sedang</div>
      <div class="container-lg">lebar 100% hingga breakpoint besar</div>
      <div class="container-xl">lebar 100% hingga breakpoint ekstra besar</div>
      <div class="container-xxl">lebar 100% hingga breakpoint ekstra besar</div>
      ```
  - ### Content pada Bootstrap
    
    - #### Images
      Dokumentasi dan contoh untuk mengikutsertakan gambar ke dalam perilaku responsif (sehingga tidak pernah menjadi lebih besar dari elemen induknya) dan menambahkan gaya ringan ke dalamnya—semua melalui kelas.
      - Contoh Penggunaan Responsive Images
        ```html
        <img src="..." class="img-fluid" alt="...">
        ```
        Gambar di Bootstrap dibuat responsif dengan .img-fluid. Ini berlaku max-width: 100%; dan tinggi: otomatis; ke gambar sehingga skala dengan elemen induk.
## Components
Komponen bootstrap berkisar dari alert, button, badge, card hingga berbagai komponen lainnya.
  - ### Card
    Card adalah wadah konten yang fleksibel dan dapat diperluas. Ini mencakup opsi untuk header dan footer, berbagai konten, warna latar belakang kontekstual, dan opsi tampilan yang kuat. Jika Anda terbiasa dengan Bootstrap 3, kartu menggantikan panel, sumur, dan thumbnail lama kami. Fungsi serupa untuk komponen tersebut tersedia sebagai kelas pengubah untuk kartu.
      - #### Contoh Penggunaan Card
        ```html
        <div class="card" style="width: 18rem;">
        <img src="..." class="card-img-top" alt="...">
        <div class="card-body">
          <h5 class="card-title">Judul Kartu</h5>
          <p class="card-text">Beberapa contoh teks cepat untuk membangun judul kartu dan membuat sebagian besar konten kartu.</p>
          <a href="#" class="btn btn-primary">Tampilkan Lebih</a>
        </div>
        </div>
        ```
    
