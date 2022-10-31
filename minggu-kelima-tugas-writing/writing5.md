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
- Cara membuat komponen pada project sebagai berikut
  - Buatlah sebuah project, atau buka project yang telah dibuat pada code editor
  - Lalu jalankan React JS
  - Buat folder Components
  - Buat file dengan nama HelloWorld. Nama file harus menggunakan HurufBesar di awal dan kata selanjutnya
- Berikut penggunaan komponen pada React JS
  ```jsx
  import React from 'React'
  import HelloWorld from './HelloWorld';

  function App() {
    return (
    <div>
    <HelloWorld/>
    </div>
    );
  };

  export default App;
  ```

### JSX
- JSX adalah syntax extension pada javascript
- JSX dikembangkan untuk digunakan pada React JS
- JSX perlu dicompile untuk menjadi Javascript, maka sebelum ditampilkan pada browser JSX akan di compile menjadi Javascript terlebih dahulu
- Kita dapat menggunakan HTML didalam file extension .js menggunakan JSX
- Setiap JSX hanya bisa memiliki 1 parent element. untuk mengatasinya kita dapat menggunakan tag `<div>` ataupun fragment `<>`
- Berikut contoh penggunaannya
  ```jsx
  import React from 'React'

  function HelloWorld() {
   return (
   <>
   <h1>First Element</h1>
   <h1>Second Element</h1>
   </>
   );
  };

  export default HelloWorld;
  ```

### Perbedaan Class Component dan Functional Component
- Komponen berbasis kelas React layaknya roti dan mentega dari sebagian besar aplikasi web modern yang dibangun menggunakan ReactJS. Komponen-komponen ini adalah kelas sederhana (terdiri dari beberapa fungsi yang menambahkan fungsionalitas ke aplikasi). Semua komponen berbasis kelas adalah kelas anak untuk kelas Komponen dari ReactJS.
  ```jsx
  import React from "react";

  class App extends React.Component {
    render() {
      return <h1>Kelas Komponen</h1>;
    }
  }

  export default App;
  ```
- Komponen fungsional adalah beberapa komponen umum yang akan ditemui saat bekerja di React. Ini adalah fungsi JavaScript. Kita dapat membuat komponen fungsional untuk React dengan menulis fungsi JavaScript.
  ```jsx
  const Saya()=> {
    return <h2>Hi, Saya Ath Thaariq!</h2>;
  }
  ```

### State & Props
- State & Props adalah hal yang berhubungan dengan Stateless dan Stateful Component
- Stateless berarti tidak memiliki state. Hanya memiliki props
- Statefull berarti memiliki state dan bisa mengirim state tersebut ke component.
- Secara singkat state adalah data lokal. Props Digunakan agar component memiliki data yang dinamis dan dikirim dari component lain
- Berikut contoh penggunaannya
  - Contoh penggunaan state
    ```jsx
    class Test extends React.Component {    
        constructor() {    
            this.state = {      
                id: 1,      
                name: "test"    
            };  
        }    

        render() {    
            return (      
                <div>        
                  <p>{this.state.id}</p>        
                  <p>{this.state.name}</p>      
                </div>    
            );  
        }
    }
    ```
  - Pass data menggunakan props
    ```jsx
    class ParentComponent extends Component {    
        render() {    
            return (        
                <ChildComponent name="First Child" />    
            );  
        }
    }

    const ChildComponent = (props) => {    
        return <p>{props.name}</p>; 
    };
    ```

### Lifecycle Methods
