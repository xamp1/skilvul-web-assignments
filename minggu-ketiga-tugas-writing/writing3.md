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

# Object
# Recursive
# Web Storage
# Asynchronus
