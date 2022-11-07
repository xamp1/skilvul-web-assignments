# _Tugas Rangkuman Minggu Ke Enam_

## React Router
React Router adalah pustaka paling populer di React. Untuk menggunakan React Router di web, kita perlu menjalankan ```npm i react-router-dom``` untuk menginstal React Router.

### Konsep Routing Pada React JS
Library ini secara khusus menginstal versi DOM dari React Router. Jika kita menggunakan React Native, kita harus menginstal react-router-native sebagai gantinya. Selain satu perbedaan kecil ini, perpustakaan bekerja hampir persis sama.
- React Router bukan hanya tentang mencocokkan url ke fungsi atau komponen: ini tentang membangun antarmuka pengguna lengkap yang memetakan ke URL, sehingga mungkin memiliki lebih banyak konsep di dalamnya daripada yang biasa kita lakukan. 

#### Tiga pekerjaan utama React Router:
  - Subscribe dan memanipulasi History Stack
  - Mencocokkan URL dengan rute kita
  - Merender Nested UI dari kecocokan rute

#### Definisi
  - URL - URL dalam bilah alamat. Banyak orang menggunakan istilah "URL" dan "rute" secara bergantian, tetapi ini bukan rute di React Router, ini hanya URL.
  - Location - Ini adalah objek khusus React Router yang didasarkan pada objek window.location browser bawaan. Ini mewakili "di mana pengguna berada". Ini sebagian besar merupakan representasi objek dari URL tetapi memiliki sedikit lebih dari itu.
  - Location State - Nilai yang bertahan dengan lokasi yang tidak dikodekan dalam URL. Sama seperti hash atau parameter pencarian (data yang dikodekan dalam URL), tetapi disimpan tanpa terlihat di memori browser.
  - History Stack - Saat pengguna menavigasi, browser melacak setiap lokasi dalam tumpukan. Jika kita mengklik dan menahan tombol kembali di browser, Kita dapat melihat tumpukan riwayat browser di sana.
  - Client Side Routing (CSR) - Dokumen HTML biasa dapat ditautkan ke dokumen lain dan browser menangani tumpukan riwayat itu sendiri. Perutean Sisi Klien memungkinkan pengembang untuk memanipulasi tumpukan riwayat browser tanpa membuat permintaan dokumen ke server.
  - Segment - Bagian dari URL atau pola jalur antara / karakter. Misalnya, "/users/123" memiliki dua segmen.
  - Path Pattern - Ini terlihat seperti URL tetapi dapat memiliki karakter khusus untuk mencocokkan URL dengan rute, seperti segmen dinamis ("/users/:userId") atau segmen bintang ("/docs/*"). Itu bukan URL, itu adalah pola yang akan cocok dengan React Router.
  - Route Config - Rute Tree objek yang akan diberi peringkat dan dicocokkan (dengan bersarang) dengan lokasi saat ini untuk membuat cabang kecocokan rute.
  - Relative Link - Link  yang tidak dimulai dengan / akan mewarisi rute terdekat tempat mereka dirender. Ini memudahkan untuk menautkan ke URL yang lebih dalam tanpa harus mengetahui dan membangun seluruh jalur.
  - Match - Objek yang menyimpan informasi saat rute cocok dengan URL, seperti params url dan nama jalur yang cocok.

### Membuat Routing Pada React JS
Ada beberapa Jenis Routing, kita akan mencoba membuat 3 jenis routing, antara lain :
- Basic Routing
- Dynamic Routing
- Nested Routing

#### Membuat Basic Routing
Jalankan ```npm i react-router-dom``` untuk menginstal React Router. Setelah Kita memiliki library ini, ada tiga hal yang perlu Kita lakukan untuk menggunakan React Router.
- Siapkan router Kita
- Tentukan rute Kita
- Menangani navigasi

##### Mengkonfigurasi Router
Langkah termudah sejauh ini adalah menyiapkan router kita. Yang perlu Kita lakukan adalah mengimpor router khusus yang Kita butuhkan (BrowserRouter untuk web dan NativeRouter untuk Mobile) dan membungkus seluruh aplikasi Kita di router tersebut.
```jsx
import { Route, Routes } from "react-router-dom"
import { Home } from "./Home"
import { BookList } from "./BookList"

export function App() {
  return (
    <Routes>
      <Route path="/" element={<Home />} />
      <Route path="/books" element={<BookList />} />
    </Routes>
  )
}
```
##### Defining Routes
Langkah selanjutnya di React Router adalah menentukan rute Kita. Ini biasanya dilakukan di tingkat atas aplikasi Kita, seperti di komponen Aplikasi, tetapi dapat dilakukan di mana pun Kita mau.
- Mendefinisikan rute semudah mendefinisikan satu komponen Rute untuk setiap rute dalam aplikasi Kita dan kemudian menempatkan semua komponen Rute tersebut dalam satu komponen Rute. Setiap kali URL Kita berubah, React Router akan melihat rute yang ditentukan dalam komponen Routes Kita dan itu akan merender konten di elemen prop dari Route yang memiliki jalur yang cocok dengan URL. Dalam contoh di atas jika URL kita adalah /books maka komponen BookList akan dirender.

##### Handling Navigation
Langkah terakhir untuk React Router adalah menangani navigasi. Biasanya dalam sebuah aplikasi Kita akan menavigasi dengan tag jangkar, tetapi React Router menggunakan komponen Tautan kustomnya sendiri untuk menangani navigasi. Komponen Tautan ini hanyalah pembungkus di sekitar tag jangkar yang membantu memastikan semua perutean dan rendering ulang bersyarat ditangani dengan benar sehingga Kita dapat menggunakannya seperti halnya tag jangkar biasa.
```jsx
import { Route, Routes, Link } from "react-router-dom"
import { Home } from "./Home"
import { BookList } from "./BookList"

export function App() {
  return (
    <>
      <nav>
        <ul>
          <li><Link to="/">Home</Link></li>
          <li><Link to="/books">Books</Link></li>
        </ul>
      </nav>

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/books" element={<BookList />} />
      </Routes>
    </>
  )
}
```
#### Membuat Dynamic Routing
Fitur yang paling sederhana dan paling umum di React Router adalah menangani Route Dynamic.
```jsx
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/books" element={<BookList />} />
  <Route path="/books/:id" element={<Book />} />
</Routes>
```
Rute terakhir pada contoh di atas adalah rute dinamis yang memiliki parameter dinamis ```:id```. Dalam case ini, Dynamic Route Kita akan mencocokkan URL apa pun yang dimulai dengan /book dan diakhiri dengan beberapa nilai. Misalnya, /books/1, /books/bookName, dan /books/all semuanya akan cocok dengan Dynamic Route kita.

#### Membuat Nested Routing
Dalam contoh di atas, kita memiliki tiga rute yang dimulai dengan /books sehingga kita dapat menyarangkan rute-rute tersebut di dalam satu sama lain untuk membersihkan rute kita.
```jsx
import { Routes, Route } from "react-router-dom"
import { BookList } from "./pages/BookList"
import { Book } from "./pages/Book"
import { NewBook } from "./pages/NewBook"
import { BookLayout } from "./BookLayout"

export function BookRoutes() {
  return (
    <Routes>
      <Route element={<BookLayout />}>
        <Route index element={<BookList />} />
        <Route path=":id" element={<Book />} />
        <Route path="new" element={<NewBook />} />
        <Route path="*" element={<NotFound />} />
      </Route>
    </Routes>
  )
}
```
Membuat komponen baru untuk menyimpan Nested Route Kita, komponen ini harus memiliki komponen Route dan di dalam komponen Route itu harus semua komponen Route yang Kita cocokkan dengan Route induk. Dalam kasus kami, kami memindahkan semua Route /books kami ke komponen BookRoute ini. Kemudian di Route induk Kita perlu menentukan Rute yang memiliki jalur yang sama dengan jalur yang dibagikan oleh semua Rute bersarang Kita. Dalam kasus kami itu adalah /books. Yang penting, bagaimanapun, adalah Kita harus mengakhiri jalur Rute induk Kita dengan * jika tidak, itu tidak akan cocok dengan rute anak dengan benar.

Pada dasarnya, kode yang telah kita tulis mengatakan bahwa setiap kali sebuah rute dimulai dengan /book/ itu harus mencari di dalam komponen BookRoutes untuk melihat apakah mereka adalah Rute yang cocok. Ini juga mengapa kami memiliki rute * lain di BookRoutes sehingga kami dapat memastikan jika URL kami tidak cocok dengan salah satu BookRoutes, itu akan merender komponen NotFound dengan benar.

## State Managemenet Redux
Redux dikenalkan sebagai "Kontainer yang Dapat Diprediksi untuk Aplikasi JS." 
  
### Konsep Redux Pada React JS
Untuk menggunakan Redux kita perlu menjalankan ```npm install @reduxjs/toolkit react-redux``` untuk menginstall redux.

Kita dapat menggunakan Redux untuk mengelola data pada halaman JavaScript sederhana. Tidak ada perpustakaan lain yang diperlukan. Ini juga bagus karena tidak ada penyiapan yang terlibat jika Kita hanya ingin menjelajah. Redux didasarkan pada Flux. Arsitektur aplikasi untuk membangun antarmuka pengguna yang mendukung aliran data searah.

### Menggunakan React Redux
Redux sendiri adalah pustaka mandiri yang dapat digunakan dengan lapisan atau kerangka kerja UI apa pun, termasuk React, Angular, Vue, Ember, dan vanilla JS. Meskipun Redux dan React umumnya digunakan bersama-sama, mereka tidak tergantung satu sama lain.

Jika Kita menggunakan Redux dengan kerangka kerja UI apa pun, Kita biasanya akan menggunakan pustaka "UI binding" untuk mengikat Redux bersama kerangka kerja UI Kita, daripada berinteraksi langsung dengan toko dari kode UI Kita.

#### Membuat Redux Store
Buatlah file bernama src/app/store.js. Impor API configureStore dari Redux Toolkit. Kita akan mulai dengan membuat toko Redux kosong, dan mengekspornya:
```jsx
import { configureStore } from '@reduxjs/toolkit'

export default configureStore({
  reducer: {},
})
```
Ini membuat toko Redux, dan juga secara otomatis mengonfigurasi ekstensi Redux DevTools sehingga Kita dapat memeriksa toko saat development.

#### Provide Redux ke React
Setelah Store dibuat, kita dapat membuatnya tersedia untuk komponen React kita dengan meletakkan React Redux <Provider> di sekitar aplikasi kita di src/index.js. Impor toko Redux yang baru saja kita buat, letakkan <Provider> di sekitar <App> Kita, dan teruskan Store sebagai prop:
```jsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import './index.css'
import App from './App'
import store from './app/store'
import { Provider } from 'react-redux'

// As of React 18
const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(
  <Provider store={store}>
    <App />
  </Provider>
)
```
#### Redux State Slice
Tambahkan file baru bernama src/features/counter/counterSlice.js. Dalam file itu, impor createSlice API dari Redux Toolkit.

Membuat slice memerlukan nama string untuk mengidentifikasi slice, nilai status awal, dan satu atau lebih fungsi Reducer untuk menentukan bagaimana status dapat diperbarui.
```jsx
import { createSlice } from '@reduxjs/toolkit'

export const counterSlice = createSlice({
  name: 'counter',
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      // Redux Toolkit memungkinkan kita untuk menuliskan logika mutasi dalam redux
      state.value += 1
    },
    decrement: (state) => {
      state.value -= 1
    },
    incrementByAmount: (state, action) => {
      state.value += action.payload
    },
  },
})

// Action dibuat untuk setiap kasus fungsi Reducer
export const { increment, decrement, incrementByAmount } = counterSlice.actions

export default counterSlice.reducer
```

#### Tambahkan Slice Reducer ke Store
Selanjutnya, kita perlu mengimpor fungsi Reducer dari irisan penghitung dan menambahkannya ke Store kita. Dengan mendefinisikan bidang di dalam parameter reduksi, kami memberi tahu Store untuk menggunakan fungsi Reducer irisan ini untuk menangani semua pembaruan ke status itu.
```jsx
import { configureStore } from '@reduxjs/toolkit'
import counterReducer from '../features/counter/counterSlice'

export default configureStore({
  reducer: {
    counter: counterReducer,
  },
})
```

#### Gunakan Redux State dan Actions dalam React Components
Sekarang kita dapat menggunakan React Redux Hooks agar komponen React dapat berinteraksi dengan Store Redux. Kita dapat membaca data dari penyimpanan dengan useSelector, dan mengirim tindakan menggunakan useDispatch. Buat file src/features/counter/Counter.js dengan komponen <Counter> di dalamnya, lalu impor komponen tersebut ke App.js dan render di dalam <App>.
```jsx
import React from 'react'
import { useSelector, useDispatch } from 'react-redux'
import { decrement, increment } from './counterSlice'
import styles from './Counter.module.css'

export function Counter() {
  const count = useSelector((state) => state.counter.value)
  const dispatch = useDispatch()

  return (
    <div>
      <div>
        <button
          aria-label="Increment value"
          onClick={() => dispatch(increment())}
        >
          Increment
        </button>
        <span>{count}</span>
        <button
          aria-label="Decrement value"
          onClick={() => dispatch(decrement())}
        >
          Decrement
        </button>
      </div>
    </div>
  )
}
```
### Menggunakan Redux Thunk
