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
  - #### Contoh Media Query
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
    - #### Penggunaan Flexbox
