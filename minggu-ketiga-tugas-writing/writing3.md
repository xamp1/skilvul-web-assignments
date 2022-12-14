# _**Tugas Rangkuman Minggu Ketiga**_

# Array dan Multidimensional Array
  - Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.
  - Contoh Array antara lain
```javascript
let productTeam = ['Product Manager', 'Back-End Web Developer', 'Front-End Developer'];
console.log(productTeam);
 ```
  - Mengakses array Ketika memasukkan nilai ke dalam sebuah array, atau sebuah nomor indeks atau subscript telah diberikan kepada tiap anggota array java, jadi program dan programmer dapat mengakses setiap nilai pada array apabila sudah dibutuhkan. Nilai sebuah indeks selalu dalam tipe integer, kemudiandimulai dari angka nol dan dilanjutkan ke angka berikutnya sampai akhir array. Sebagai sebuah catatan untuk kita bahwa indeks didalam array dimulai dari 0 sampai dengan (ukuranArray-1).
```javascript
//memberikan nilai 10 kepada elemen pertama array
ages[0] = 10;
//mencetak elemen array yang terakhir
System.out.print(ages[99]);
```
  - Mengupdate Array dapat menggunakan ```function update()``` Fungsi update digunakan untuk menambahkan elemen baru pada array dictionaries. Fungsi update merupakan fungsi yang melekat pada tipe data dictionaries. Karena fungsi update adalah bagian dari data bertipe dictionaries, sehingga penerapannya mirip dengan objek dan fungsinya pada bahasa pemrograman berbasis objek.
  - Const in Array
    - Jika menggunakan let, kita dapat mengubah array  dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
    - Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
    - Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const
  - Array Properties, Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype. Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.
    - Constructor akan mengembalikan fungsi yang membuat prototipe Array.
    - Length akan mengembalikan nilai dari jumlah panjang data suatu array.
    - Index 3 macam properti index yaitu IndexOf, findIndex, lastIndex
    - Prototype memungkinkan kita untuk menambahkan properti dan metode baru ke array.
  - Array Method, Array memiliki method atau biasa disebut built-in methods.
  - Contoh Array Built-In
    - .push() adalah method untuk menambahkan item  array pada urutan yang paling akhir.
    - .pop() adalah method yang menghapus item array index terakhir.
    - .shift() adalah method untuk menghapus item Array pada index pertama
    - .unshift() adalah method untuk menambahkan item Array pada index pertama
    - .sort() adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric
  - Looping pada array Looping adalah sebuah metode perulangan dimana bisanya perulangan tersebut akan menghasilakan sebuah data berurutan, misalkan looping angka numerik 1 sampai dengan 10 maka looping akan mencetak 1 2 3 4 5 6 7 8 9 10
    - Contoh Looping
```javascript
for (i = 1; i <= 10; i++){
 
}
```
  - Dari contoh script di atas hanya menampilkan angka 1 sampai dengan 10, karena di situ ada operator yang berjalan hanya ketika nilai i dibawah atau sama dengan nilai 10.
  - .forEach() adalah method untuk melakukan looping pada setiap elemen array. 
```javascript
const cars = ['tesla', 'honda', 'toyota'];
cars.forEach(element => {
console.log(element);
}); // output: 'tesla', 'honda', 'toyota'
```
  - .map melakukan perulangan/looping dengan membuat array baru.
```javascript
let arr = [1,2,3,4,5];

let doubled = arr.map(num => {
    return num * 2;
});
console.log(doubled);  // output: [2,4,6,8,10]
```
  - Multidimensional Array, bisa dianalogikan dengan array of array. Ada array didalam array.
```javascript
let inventory = [
    ['Kaos Polos' , 10],
    ['Jaket Hoodie' , 12],
    ['Topi' , 24],
    ['Celana' , 8],
];
console.log(inventory);
```
  - Akses index multidimensional array
```javascript
let inventory = [
    ['Kaos Polos' , 10],
    ['Jaket Hoodie' , 12],
    ['Topi' , 24],
    ['Celana' , 8],
];
console.log(inventory[1][0]);
//Output: Jaket Hoodie
```
  - Properti dan Method built-in pada Multidimensional Array
```javascript
let inventory = [
    ['Kaos Polos' , 10],
    ['Jaket Hoodie' , 12],
    ['Topi' , 24],
    ['Celana' , 8],
];

inventory.push(['Jaket Sweater', 7]);

console.log(inventory)
```
  - LOOPING FOR MULTIDIMENSIONAL ARRAY
```javascript
let inventory = [
    ['Kaos Polos' , 10],
    ['Jaket' , 12],
    ['Topi' , 24],
    ['Celana' , 8],
];
inventory.forEach((baris) => {
    baris.forEach((column) => {
        console.table(column);
    });
});
```
# Object
  - Apa itu Object
    - Object adalah entitas yang independen di mana ia memiliki metode dan properti. Nilai properti dapat berupa fungsi, dalam hal ini properti tersebut dikenal sebagai metode. dalam JavaScript kita tidak dapat mendeklarasikan angka, string, dan boolean sebagai objek.
    - Properti adalah data lengkap dari sebuah object.
    - Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.
  - Membuat sebuah object
```javascript
let person = {}; //disini person menjadi object yang kosong
```
  - Mengakses Object dan Property Object
```javascript
let person = {
    name : 'Ath Thaariq',
    age : 20,
    isVerified: true
}
console.log(person);
```
  - Update Object 
```javascript
let person = {
    name : 'Ath Thaariq',
    age : 20,
    isVerified: true
}
person.age = '21'
person.addres = 'Depok, Jawa Barat';
console.log(person);
```
  - Delete Object
```javascript
let person = {
    name : 'Ath Thaariq',
    age : 20,
    isVerified: true
}
delete person.age;
console.log(person);
```
  - Method disebut Jika value yang kita masukkan pada property berupa function.
  - Nested Object adalah Object yang berasal dari turunan object lainnya.
  - Passed by reference yakni mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.
  - Looping Object, jika ingin menampilkan seluruh object properti. Bisa menggunakan looping. Sehingga tidak perlu mengakses secara manual memanggil setiap propertinya.
  - Array of Object, berarti list/kumpulan/daftar object yang seragam. Dikatakan seragam karena objek yang berada dalam satu array pasti memiliki property yang sama.
# Recursive
  - Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
    - Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.
```javascript
function recursive(){
    // ...
    recursive();
    // ...
}
```
  - Ciri - ciri Rekursif antara lain adalah
    - Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
    - Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.
  - Contoh Rekursif
```javascript
function pow(x, n) {
    if (n = 1) {
        return x;
    } else {
        return x * pow(x, n - 1);
    }
}
console.log(pow(2, 3)); // Output: 8
```
# Web Storage
  - Web Storage adalah salah satu Web API yang dapat menyimpan data secara lokal pada sisi client. Berbeda dengan objek atau array, data yang disimpan pada objek atau array JavaScript bersifat sementara, dan akan hilang jika terjadi reload atau pergantian URL pada browser.
  - Local Storage & Session Storage
    - Object localStorage dan sessionStorage, adalah bagian dari API penyimpanan web, dan adalah dua alat hebat untuk menyimpan pasangan key/value secara lokal.
    - localStorage dan sessionStorage hampir identik dan memiliki API yang sama. Perbedaannya adalah bahwa dengan sessionStorage, data hanya bertahan sampai jendela atau tab ditutup. Dengan localStorage, data dipertahankan hingga pengguna secara manual menghapus cache browser atau hingga aplikasi web kita menghapus data.
  - Membuat Entry dapat dilakukan dengan method setItem()
```javascript
let key = 'Item 1';
localStorage.setItem(key, 'Value');
```
  - Membaca Entry dapat dilakukan dengan method getItem()
```javascript
let myItem = localStorage.getItem(key);
```
  - Mengupdate Entry dilakukan dengan method setItem() lagi menggunakan 2 argument, key yang ada dan key yang baru sebagai New Value
```javascript
let myItem = localStorage.setItem(key 'New Value');
```
  - Cookies
    - Cookie browser diperkenalkan ke web untuk menjaga informasi tetap tentang pengguna. Kasus penggunaan pertama adalah untuk memeriksa apakah pengguna telah mengunjungi situs web Netscape.
    - Cookie adalah string yang memiliki name field, value field dan atribut opsional tambahan. Nilainya adalah string dan kita dapat menyimpan apa pun yang menurut kita terbaik untuk aplikasi kita. _ _ga_ pada Google Analytics mungkin salah satunya Cookie paling umum.
    - Kita dapat memanipulasi Cookie Google Analytics dengan cara di bawah ini
```javascript
console.log(document.cookie)
document.cookie = "alligator=alligator_cookie_content;"
console.log(document.cookie)

const createCookie = (name, value) => document.cookie = name + '=' + value + ';'
const updateCookie = (name, value) => document.cookie = name + '=' + value + ';'
const deleteCookie = (name) => document.cookie = name + '=; Max-Age=-1;';
```
# Asynchronus
  - Asynchronous programming adalah teknik yang memungkinkan program kita untuk memulai tugas yang berpotensi berjalan lama dan masih dapat responsif terhadap peristiwa lain saat tugas itu berjalan, daripada harus menunggu sampai tugas itu selesai. Setelah tugas itu selesai, program kita disajikan dengan hasilnya.
    - Contoh Synchronous programming
```javascript
const name = 'Ath Thaariq';
const greeting = `Hello, my name is ${name}!`; //Deklarasi name sebagai string, dan mendeklarasikan string lain bernama "greeting" yang menggunakan name
console.log(greeting); //Menampilkan greeting ke konsol JavaScript.
// "Hello, my name is Ath Thaariq!"
```
  - Take note di sini bahwa browser secara efektif melangkah melalui program satu baris pada satu waktu, dalam urutan yang kami tulis. Pada setiap titik, browser menunggu baris untuk menyelesaikan pekerjaannya sebelum melanjutkan ke baris berikutnya. Ini harus dilakukan karena setiap baris tergantung pada pekerjaan yang dilakukan pada baris sebelumnya. Jadi itu membuat ini menjadi Synchronous Program
  - Asynchronous - Promise
    - Sebuah Janji singkatnya: ???Bayangkan kamu masih kecil. Ibumu berjanji padamu bahwa dia akan membelikanmu telepon baru minggu depan.??? Kita tidak tahu apakah kita akan mendapatkan telepon itu sampai minggu depan. Apakah Ibu benar-benar dapat membelikan telepon baru, atau tidak. Itu adalah sebuah janji. Sebuah janji memiliki tiga keadaan. Antara lain: 
    - Pending: Janji itu ditunda
    - Fulfilled: Janji itu terpenuhi
    - Rejected: Janjinya di lupakan atau tidak di terima
  - berikut contoh programnya
```javascript
var isMomHappy = false;

// Promise
var willIGetNewPhone = new Promise(
    function (resolve, reject) {
        if (isMomHappy) {
            var phone = {
                brand: 'Samsung',
                color: 'black'
            };
            resolve(phone); // fulfilled
        } else {
            var reason = new Error('mom is not happy');
            reject(reason); // reject
        }

    }
);
```
  - Asynchronous - Async Await
    - Async/Await merupakan sebuah syntax khusus yang digunakan untuk bekerja dengan Promise agar lebih nyaman dan mudah untuk digunakan.
    - Contoh Async Functio
 ```javascript
 async function myFunction() {
  // ini adalah async function
}
 ```
  - API and HTTP Request
    - Application Programming Interfaces (API) adalah konstruksi yang tersedia dalam bahasa pemrograman untuk memungkinkan pengembang membuat fungsionalitas yang kompleks dengan lebih mudah. Mereka mengabstraksikan kode yang lebih kompleks dari kita, menyediakan beberapa sintaks yang lebih mudah untuk digunakan sebagai gantinya.
    - HTTP Request adalah dimana server membaca apa yang dikirimkan oleh client melalui aplikasi web server. HTTP Response yaitu dimana server akan merespon permintaan yang telah dikirimkan oleh client.
  - JSON atau JavaScript Object Notation. Adalah format untuk berbagi data. Seperti namanya, JSON berasal dari bahasa pemrograman JavaScript, tetapi tersedia untuk digunakan oleh banyak bahasa termasuk Python, Ruby, PHP, dan Java. JSON biasanya diucapkan seperti nama ???Jason.???
  - Contoh object json
```javascript
{
  "first_name" : "Ath Thaariq",
  "last_name" : "Adz Zyad",
  "location" : "Depok",
  "online" : true,
  "followers" : 987 
}
```
  - Asynchronous - Fetch
    - Fetch API menyediakan JavaScript Interface untuk mengakses dan memanipulasi bagian protokol, seperti permintaan dan tanggapan. Ini juga menyediakan metode fetch() global yang menyediakan cara mudah dan logis untuk mengambil sumber daya secara asinkron di seluruh jaringan.
    - Contoh simple request fetch 
```javascript
fetch('http://example.com/movies.json')
  .then((response) => response.json())
  .then((data) => console.log(data));
```
   - Di sini kita mengambil file JSON di seluruh jaringan dan mencetaknya ke konsol. Penggunaan paling sederhana dari fetch() membutuhkan satu argumen ??? jalur ke sumber daya yang ingin kita ambil ??? dan tidak secara langsung mengembalikan badan respons JSON tetapi sebaliknya mengembalikan janji yang diselesaikan dengan objek Respons.
