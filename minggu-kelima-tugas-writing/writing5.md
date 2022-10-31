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
- Kedua komponen ini menghasilkan hal yang sama, namun class menggunakan state dan functional menggunakan state hooks
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
- Lifecycle secara harafiah dapat di artikan sebagai siklus hidup. Misal siklus hidup manusia. Pertama manusia akan dilahirkan, kemudian memasuki fase pertumbuhan, dan terakhir akan meninggal. Sama seperti manusia, setiap component di react js ternyata juga memiliki siklus hidup.
- 4 jenis lifecycle pada react antara lain
  - Initialization. Adalah sebuah siklus React Native untuk menset State dan Props sebelum aplikasi di jalankan
  - Mounting. Sebuah siklus ketika aplikasi baru saja di buka ada 2 jenis yaitu componentDidMount() ketika memuat aplikasi sebelum render dilakukan. componentWillMount yaitu siklus setelah render proses dilakukan. Tapi sekarang disarankan kamu menggunakan componentDidmount().
  - Updatating. Yaitu ketika kamu mengubah data yang telah di Mounting.
  - Unmount. Adalah proses menghancurkan atau mendestroy komponen yang sebelumnya di definisikan.
- Berikut contoh diagramnya 
![image](https://user-images.githubusercontent.com/76435776/198980306-42b0b39f-8342-4d07-8e9b-7b4b4c8f98aa.png)

### Styling pada React JS
- Ada 3 cara membuat styling di react
  - Impor external css di index.html
  - Import css di setiap komponen
  - Membuat inline css
- Cara pertama direkomendasikan jika kita ingin memuat css dari framework CSS seperti Bootstrap.
- Cara kedua lebih mudah digunakan jika kamu ingin memanajemen styling tiap komponen.
- Cara ketiga bisa digunakan dengan kekuranganya berupa penurunan performa dari file HTML kamu.
- Berikut contoh inline-styling pada .jsx
  ```jsx
  import React from "react";

  export default function ImageFeed(props) {
    return (
      <div style={{ maxHeight: "20rem", padding: "10px", margin: "10px" }}>
        <img
          style={{
            objectFit: "cover",
            width: "100%",
            height: "20rem",
          }}
          src={props.image}
        />
        <p>{props.description}</p>
      </div>
    );
  }
  ```

## React JS Lanjutan
### React Hooks
- Hooks adalah fitur baru yang dikenalkan pada reactJs pada tahun 2018
- Hooks dibuat dengan tujuan untuk memudahkan penggunaan functional components agar bisa menggunakan state, dan lifecycle lainnya.
- Hooks yang sering digunakakn adalah useState, dan useEffect
  - useState. Penggunaan useState sedikit berbeda dengan setState/state di class components, namun pengertianya sendiri sama dengan state biasa.
    - Berikut contoh penggunaan useState
      ```jsx
      import React from "react";
      function App (){
        const [nama, setNama] = useState("Ath Thaariq");
        return (
        <div className="App">
        <p>halo, saya {nama}</p>
        <button onClick = {() => setNama("Adz Zyad")}></button>
        </div>
        );
      }
      ```
    - Update State. State dapat kita ubah menggunakan variable kedua dari state hooks, kita dapat menggunakan onChange untuk melakukan Update State. Berikut cara penggunaannya
      ```jsx
      function App (){
        const [nama, setNama] = useState("Ath Thaariq");
        const [kota, setKota] = useState(null);

        return (
        <div className="App">
          <p>
            halo saya {nama}, saya tinggal di kota{kota}
          </p>
          <button onClick = {() => setNama("Adz Zyad")>Ubah Nama</button>
          <input type="text" onChange={(evt) => setKota(evt.target.value)} />
        </div>
        );
      }
      ```
  - useEffect. Penggunaan useEffect bisa dimasukan sebelum melakukan render, useEffect sendiri biasanya ditempatkan dibawah useState.
    - Nantinya, apa yang kita tuliskan dalam useEffect akan dijalankan setiap ```componentDidMount```, ```componentDidUpdate```dan ```componentWillUnmount```
    - Berikut contoh penggunaannya
      ```jsx
      import React from "react";
      function App (){
        const [nama, setNama] = useState("true");
        const [changed, setChanged] = useState(0);
        
        useEffect(() => {
          console.log(*ada oerubahan*);
          setChanged(changed + 1);
        }, [nama]);
        
        return (
          <div>
            <h1>Perubahan : {changed}</h1>
            <button onClick = {() => setNama("!nama")}>Ubah</button>
          </div>
        );
      }
      ```
    - Maka Outputnya setiap tombol ubah ditekan maka state nama akan berubah, lalu komponen akan di re-render sehingga memanggil useEffect
    - useEffect biasanya akan digunakan saat kita membuat suatu call API, karena API akan selalu di panggil saat komponen terbentuk, maka call API bisa dilakukan dalam useEffect
### PropTypes
- PropTypes adalah mekanisme yang memastikan bahwa nilai yang diteruskan adalah tipe data yang benar. Ini memastikan bahwa kita tidak menerima kesalahan di akhir aplikasi kita oleh konsol yang mungkin tidak mudah untuk ditangani.
- Untuk menginstall proptypes cukup lakukan command berikut pada terminal kita ```npm install prop-types```
- Berikut contoh penggunaan Prop-Types
  ```jsx
  import PropTypes from 'prop-types'

  function Header(props){
    return (
    <>
    <h2>Name : {props.char}</h2>
    <h2>Age : {props.age}</h2>
    </>
    );
  }

  Header.propTypes = {
    char: PropTypes.string,
    age: PropTypes.number,
  }
  ```
  - Dengan begini kita akan mendapatkan pesan error jika tidak sesusai dengan ekspektasi. Sehingga jika terjadi kesalahan kita dapat langsung mengetahuinya dan segera memperbaikinya
