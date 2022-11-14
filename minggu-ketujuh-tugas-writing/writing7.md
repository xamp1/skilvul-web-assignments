# _Tugas Rangkuman Minggu Ke 7_

## React Context
React Context menyediakan cara untuk meneruskan data melalui pohon komponen tanpa harus meneruskan prop secara manual di setiap level.

React Context dirancang untuk berbagi data yang dapat dianggap “global” untuk pohon komponen React, seperti pengguna terautentikasi saat ini, tema, atau bahasa pilihan.

Membuat Context baru dapat menggunakan fungsi berikut:
```jsx
export const LocaleContext = React.createContext('en');
```
### Provider
Komponen Provider digunakan untuk membungkus komponen dalam pohon yang memerlukan akses ke nilai dari Context. Seperti contoh berikut:
```jsx
import React from 'react';

export const LocaleContext = React.createContext();

class LocaleProvider extends React.Component {
  constructor(props) {
    super(props);

    this.changeLocale = () => {
      this.setState(state => {
        const newLocale = state.locale === 'en' ? 'fr' : 'en';
        return {
          locale: newLocale
        };
      });
    };

    this.state = {
      locale: 'en',
      changeLocale: this.changeLocale
    };
  }

  render() {
    return (
      <LocaleContext.Provider value={this.state}>
        {this.props.children}
      </LocaleContext.Provider>
    );
  }
}

export default LocaleProvider;
```
Perhatikan bagaimana komponen LocaleProvider hanyalah pembungkus tipis di sekitar komponen Penyedia konteks kita. Nilai konteks diteruskan ke penyedia menggunakan prop nilai dan kemudian Kita merender anak-anak LocaleContext.
### Consumer
Komponen Consumer menggunakan pola penyangga render dan mengharapkan fungsi sebagai penyangga turunannya yang akan menerima nilai dari Contextnya. Kita kemudian dapat mengakses nilai Context dan memanggil metode yang tersedia.
### Menggunakan Context untuk State Management
```jsx
// UserDetailsProvider.js

import { createContext, useState } from 'react';

export const userDetailsContext = createContext();

const UserDetailsProvider = (props) => {
    const [userDetails, setUserDetails] = useState();

    return (
        <userDetailsContext.Provider value={[userDetails, setUserDetails]}>
            {props.children}
        </userDetailsContext.Provider>
    );
};

export default UserDetailsProvider;
```
Pada kode di atas, kita telah menggunakan api createContext untuk membuat userDetailsContext. Sekarang, konteksnya telah dibuat, jadi kita perlu membuat penyedia.

Dalam fungsi UserDetailsProvider, Kita membuat penyedia untuk userDetailsContext. <contextname.Provider> adalah sintaks umum untuk membuatnya. Harap perhatikan prop nilai di sini. Prop nilai akan selalu digunakan untuk meneruskan status bersama ke bawah. Dalam hal ini, kita meneruskan fungsi state dan setState ke bawah. Ini karena, meskipun setiap komponen memperbarui status, status global dapat diperbarui yang akan tersedia untuk semua komponen.

Sekarang konteks dan penyedia kita dibuat. Mari tambahkan penyedia ke aplikasi. Ini adalah langkah yang paling penting, karena akan membuat penyedia tersedia untuk semua komponen. Oleh karena itu, mari bungkus komponen aplikasi kita di dalam penyedia ini. Komponen aplikasi kita akan terlihat seperti ini:
```jsx
//App Component

import { BrowserRouter, Switch, Route } from 'react-router-dom';
import { RouteWithSubRoutes } from './utils/shared';
import UserDetailsProvider from './context/UserDetailsProvider';
import routes from './Routes';

function App() {
    return (
        <BrowserRouter>
            <Switch>
                // As login do not require the userDetails state, keeping it outside.
                <Route path='/' component={Login} exact />
                // All other routes are inside provider
                <UserDetailsProvider>
                    {routes.map((route) => (
                        <RouteWithSubRoutes key={route.key} {...route} />
                    ))}
                </UserDetailsProvider>
            </Switch>
        </BrowserRouter>
    );
}

export default App;
```
Dalam kode ini, data tidak akan diambil oleh komponen aplikasi. Catatan, di sini kita hanya menambahkan komponen di dalam UserDetailsProvider yang sebenarnya membutuhkan status ini.
```jsx
// Profile.js

import { useEffect, useState, useContext } from 'react';
import { getUser } from '../../utils/api';
import { userDetailsContext } from '../../context/UserDetailsProvider';

const Profile = ({ email }) => {

    const [userDetails, setUserDetails] = useContext(userDetailsContext);
    const [loading, setLoading] = useState(false);

    const handleGetUser = async () => {
        try {
            setLoading(true);
            let response = await getUser(email);
            setUserDetails(response.data);
        } catch (error) {
            console.log(error);
        }
        setLoading(false);
    };

    useEffect(() => {
        if (!userDetails) {
            handleGetUser();
        }
    }, []);

    return <div className='bg-gray-gray1 h-full'>// do something</div>;
};

export default Profile;
```
Jika kita perhatikan, useContext terlihat mirip dengan useState. Dan nanti kita akan menggunakannya sama seperti useState, Oleh karena itu, setiap kali fungsi setUserDetails dipanggil, perubahan status akan efektif di seluruh aplikasi, menghemat terlalu banyak pengeboran penyangga.
## React Testing
