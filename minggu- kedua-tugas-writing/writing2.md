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
- Fungsi di atas akan menampilkan text "Hello World"

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
# Data Type, Method, Property
-
