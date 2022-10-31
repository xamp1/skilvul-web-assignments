# _Writing 5_
## React.js Dasar
### React JS & Kenapa React JS?
- React JS adalah framework view library javascript untuk membuat tampilan user interface pada website
- React JS itu Cepat. Membuat aplikasi front-end menjadi lebih cepat walaupun harus menjalankan bermacam data
- React JS itu Modular. Kita dapat menerapkan konsep modular pada javascript pada react js, react membagi 1 tampilan pada website menjadi komponen-komponen kecil.
- React JS itu Scalable. Dapat digunakan pada aplikasi bersekala kecil hingga besar dan kompleks
- React juga Populer. Kebanyakan perusahaan teknologi pun sudah menggunakan react js, jadi akan mudah untuk mencari pekerjaan baik freelance maupun startup.

### Instalasi & Cara Menjalankannya
- Untuk mengunakan React kita perlu menginstall node.js
- Lalu pergi ke https://create-react-app.dev/
- Karena kita sudah menginstall node.js maka npm secara otomatis akan tersintall
- Lalu pergi ke cmd pada file folder yang kita inginkan ```npm init react-app my-app ```
- Kita dapat mengakses react melalui ```localhost:3000``` atau pada yarn kita dapat menggunakan ```yarn start```

### Component pada React JS
- Komponen adalah bit kode yang independen dan dapat digunakan kembali. Mereka melayani tujuan yang sama seperti fungsi JavaScript, tetapi bekerja secara terpisah dan mengembalikan HTML. Terdapat dua jenis komponen antara lain, komponen Kelas dan komponen Fungsi
- Berikut cara penggunaan komponen pada React JS
  ```jsx
  import React from 'React'
  import HelloWorld from './HelloWorld';

  function App() {
    return (
    <div>
    <HelloWorld/>
    </div>
    )
  };

  export default App;
  ```

### JSX
