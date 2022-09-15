# **HOOKS**
> merupakan fitur yang dikenalkan di react js, untuk memudahkan pengguna functional components agar bisa menggunakan state, dan lifecycle lainnya. Hooks yang sering digunakan adalah useState dan useEffect.
> kelebihan pada saat penggunaa Hooks yaitu code akan terlihat lebih clean, pendek dan mudah dimengerti dan Hooks ini jauh lebih unggul dalam kemudahannnya.
## useState
> adalah salah satu basic Hooks yang dapat digunakan. useState berupa nilai variabel objek atau data apapun yang berada pada component.
contoh :
        import {useState} from "react";

        function App() {
            const [name, setName] = useSate("Umi");

            return (
                <>
                    <p>My name is {name} </p>
                </>
            )
        }

>dapat dilihat pada code diatas, untuk dapat menggunakan Hook, kita harus mengimport Hook useState dari React. dan menggunakan functional component yaitu App. setelah itu, membuat status dan memberikan nilai awal (status awal)yaitu "umi". Variabel sattus name dan set name sebagai fungsi untuk memperbarui nilai. 
## useEffect
> adalah efek pada setiap perubahan status. Secara default, proses ini berjalan setelah render pertama dan setiap kali status diperbarui.
contoh :
        import {useState, useEffect} from "react";

        function App() {
            const [count, setCount] = useState(0);
            
            useEffect(() => {
                console.log(`You have clicked the button ${count} times`)
            });

            return(
                <>
                    <button onClick={() => setCount(count + 1)}>Click me</button>
                </>
            )
        }
        export default App

> dapat dilihat pada gambar kita harus mengimport useState maupun useEffect terlebih dahulu. dimana dapat diperhatikan bahwa kita dapat menggunakan useEffect untuk mencapai berbagai effect seperti mengambil data dari API eksternal serta dapat mengubah DOM di component, dsb.

# **React Router**
> adalah sistem library standar yang di bangun di atas React dan di gunakan untuk membuat perutean (sederhannya) pada React Mengunakan React Router.
### Instalation React Router
        npm install react-router-dom@6
> Setelah melakukan penginstalan React Router, langkah selanjutnya mengimport react router didalam file index.js dengan konfigurasi sbb:
        
        import * as React from "react";
        import ReactDOM from "react-dom/client";
        import "./index.css";
        import App from "./App";
        import { BrowserRouter } from "react-router-dom";
        

        const root = ReactDOM.createRoot(
        document.getElementById("root")
        );
        root.render(
        <React.StrictMode>
            <BrowserRouter>
            <App />
            </BrowserRouter>
        </React.StrictMode>
        );

> selanjutnya pemanggilannya dilakukan di src/App.js dan ketikkan default markup dengan menggunakan beberapa route.

        import * as React from "react";
        import { Routes, Route, Link } from "react-router-dom";
        import "./App.css";
        import Home from './Home';

        function App() {
        return (
            <div className="App">
            <h1>Welcome to React Router!</h1>
            <Routes>
                <Route path="/" element={<Home />} />
            </Routes>
            </div>
        );
        }

> misalnya untuk menapilkan page home, terlebih dahulu lakukan import route dan componen yang akan digunakan. ketikkan perintah npm start untuk menjalankan website.

# **React Redux**
> Redux adalah salah satu state management.
## Installation Redux
        npm install redux react-redux redux-devtools-extension
> Langkah-langkah menggunakan Redux
- membuat folder dengan **store** didalam folder tersebut dibagi lagi 2 folder dan 1 file dantaranya:
    1. Folder **action** (sebuah function yang mereturn sebuah objek. objek tersebut memiliki sebuah property wajib yaitu type). pada folder ini ditambahkan index.js
    2. Folder **reducer** (sebuah fungsi yang tugsnya untuk mengolah state yang ad di store). pada folder ini ditambahkan index.js
    3. Folder **store.js** (tempat untuk menampung state).

