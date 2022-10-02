# **Rangkuman Minggu Kedua**

# Scope
- Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.
- Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks.
- Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.

# Function
- Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
- Berikut contoh fungsi sederhana dalam Javascript
```javascript
console.log("Hello World!"); 
```
_Fungsi di atas akan menampilkan text "Hello World"_

# Errors & Debugging
- Error adalah objek serializable, sehingga dapat dikloning dengan structuredClone() atau disalin antara Pekerja menggunakan postMessage()
- Objek Error ditampilkan ketika kesalahan runtime terjadi. Objek Error juga dapat digunakan sebagai objek dasar untuk pengecualian yang ditentukan pengguna.
- kita dapat mengatasi error menggunakan ```try...catch``` construct
```javascript
try {
  throw new Error('Whoops!');
} catch (e) {
  console.error(`${e.name}: ${e.message}`);
}
```
# Data Type Built in Prototype & Method
- Data Type
  - Semua bahasa pemrograman memiliki struktur data bawaan, tetapi ini sering berbeda dari satu bahasa ke bahasa lainnya.
- String
  - Objek String digunakan untuk mewakili dan memanipulasi urutan karakter.
  - String berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks. Beberapa operasi yang paling sering digunakan pada string adalah memeriksa       - panjangnya, membangun dan menggabungkannya menggunakan operator string + dan +=, memeriksa keberadaan atau lokasi substring dengan metode indexOf(), atau mengekstrak substring dengan substring () metode.
- Number
  - Number adalah objek wrapper primitif yang digunakan untuk mewakili dan memanipulasi angka seperti 37 atau -9,25.
  - Konstruktor Number berisi konstanta dan metode untuk bekerja dengan angka. Nilai dari tipe lain dapat dikonversi ke angka menggunakan fungsi Number().
- Math
  - Math adalah objek bawaan yang memiliki properti dan metode untuk konstanta dan fungsi matematika. Math bukanlah objek fungsi.
  - Tidak seperti banyak objek global lainnya, Math bukanlah sebuah konstruktor. Semua properti dan metode Math bersifat statis. Anda merujuk ke pi konstan sebagai Math.PI dan Anda memanggil fungsi sinus sebagai Math.sin(x), di mana x adalah argumen metode. Konstanta didefinisikan dengan presisi penuh bilangan real dalam JavaScript.
- Primitive & Non Primitive
