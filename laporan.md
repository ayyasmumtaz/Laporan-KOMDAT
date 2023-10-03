# KomGallery

![Imgur](https://i.imgur.com/cv5aRu6.png)

## Deskripsi Singkat

KomGallery adalah aplikasi media sosial yang dirancang khusus untuk mahasiswa Ilmu Komputer di Universitas IPB. Ini berfungsi sebagai platform untuk berbagi foto dengan lancar di antara komunitas mahasiswa, memfasilitasi kolaborasi, dan memupuk rasa keterlibatan komunitas. Pengguna dapat mengunggah, memberi komentar, menyimpan, dan mengunduh foto, serta mengaitkan tautan yang relevan dengan setiap foto, memungkinkan manfaat tambahan seperti promosi acara dan sumber daya terkait.

#### Fitur
- Login menggunakan akun Google
- Menunggah foto dengan judul, deskripsi, kategori, dan link(opsional).
- Memberi komentar, menyimpan, dan mengunduh foto yang sudah diunggah ke website.
- Profil pengguna yang menampilkan foto yang diunggah dan foto yang disimpan.
- Filter gambar sesuai kategori.
- Pencarian gambar efisien berdasarkan judul atau deskripsi.
- UI interaktif.

## Technology Stack

Frontend KomGallery dikembangkan menggunakan HTML, CSS, dan JavaScript sebagai bahasa pemrograman inti. Untuk membangun antarmuka pengguna yang kuat dan interaktif, kami menggunakan framework React.js. Dengan memanfaatkan React.js, kami menggunakan fitur-fitur seperti reusable component, routing, state management, dan metode component lifecycle untuk mengorganisir dan mengelola logika tampilan aplikasi dengan efisien. Selain itu, kami menggunakan framework Tailwind CSS, yang mengikuti pendekatan utilitas pertama, memungkinkan kami untuk dengan mudah mengonfigurasi struktur tata letak dan menerapkan gaya CSS yang telah ditentukan sebelumnya untuk meningkatkan estetika visual dan responsivitas aplikasi.

Di bagian Backend, kami mengadopsi pendekatan headless CMS dengan menggunakan Sanity. Sanity bertindak sebagai penyedia konten dan berfungsi sebagai repositori sentral untuk menyimpan berbagai konten aplikasi, termasuk foto yang diunggah oleh pengguna. Dengan memanfaatkan API JavaScript yang disediakan oleh Sanity, kami secara lancar berinteraksi dengan sistem manajemen konten untuk melakukan operasi CRUD (Create, Read, Update, Delete) sehingga memastikan manajemen dan pengambilan konten yang efisien.

## User Authentication

Untuk memastikan akses yang aman dan manajemen pengguna, kami mengintegrasikan Otentikasi Google (OAuth) sebagai layanan pihak ketiga. Dengan memanfaatkan OAuth, pengguna dapat masuk ke KomGallery dengan aman menggunakan akun Google mereka sehingga menghilangkan kebutuhan untuk manajemen otentikasi pengguna secara manual. Integrasi ini bergantung pada infrastruktur keamanan yang disediakan oleh Google agar dapat memastikan otentikasi pengguna yang lancar, andal, dan sangat aman.

## Deployment

KomGallery di-deploy menggunakan Netlify, yaitu platform besar untuk hosting dan juga deployment berkelanjutan. Proses deployment ini diatur dengan baik, sehingga memungkinkan deployment otomatis setiap kali ada perubahan yang diunggah ke repositori. Versi langsung dari KomGallery dapat diakses di https://komgallery.netlify.app, di mana pengguna dapat menjelajahi fitur dan fungsionalitasnya.

## Getting Started

### Instalasi
#### System Requirement

- Windows, MacOS atau Linux
- `nodejs` latest version
- `npm` latest version
- Code Editor ex. Visual Studio Code

#### Proses Instalasi

- Buat direktori untuk menampung file
  ```
  mkdir nama-direktori
  cd nama-direktori
  ```
  
- Clone Komgallery kedalam direktori yang sudah dibuat menggunakan Git-Bash
  ```
  git clone https://github.com/ayyasmumtaz/Komgallery.git
  ```
  
- Buka direktori di code editor yang anda gunakan

### Instalasi dependencies

- Buka terminal pada code editor
  
- Pindah ke direktori frontend
  ```
  cd frontend
  ```
  
- Instalasi React.js dan Tailwind css
  
  - Create React App
  ```
  npx create-react-app ./
  ```
  
  - Install Tailwind css
  ```
  npm install -D tailwindcss
  ```
  
  untuk lebih lanjut kunjungi: https://tailwindcss.com/docs/guides/create-react-app
  
- Install necessary dependencies
  ```
  npm install @sanity/client @sanity/image-url react-google-login react-icons react-loader-spinner react-masonry-css react-router-dom uui
  ```
  
- Start React App di localhost:3000
  ```
  npm start
  ```

![Imgur](https://i.imgur.com/ogfqQym.png)


# Deploy dan Konfigurasi

## Hosting
Web Komgallery di hosting menggunakan Netlify, berikut adalah step step yang dilakukan:

- Buat Folder Build
  - Buka terminal pada direktori folder web di code editor
  - Pindah ke direktori frontend
    ```
    cd frontend
    ```
  - Buat folder Production Build
    ```
    npm run build
    ```
    
- Netlify
  - Buka bagian deploy manually di Netlify
  - Drag and drop file Production Build
    
    ![Imgur](https://imgur.com/Qd0cH5W.png)
    
  - Web sudah bisa di akses, disini kita bisa mengubah nama domain sesuai dengan keinginan

    ![Imgur](https://imgur.com/EFaMrhK.png)



## Database
Web Komgallery menggunakan Content Management System yaitu Sanity, berikut merupakan konfigurasi database agar bisa digunakan:
- Masuk dan Login pada web sanity
- Buka Admin Dashboard Komgallery pada sanity
- Pilih Page API, klik tombol add CORS origin dan masukan nama domain dari web yang kita buat, sebagi contoh `https://komgallery.netlify.app/`, pilih allow credentials dan klik save
  
![Imgur](https://imgur.com/aVz5SQ7.png)

Dengan melakukan hal ini web yang kita buat dapat menerima maupun mengirim data pada database menggunakan API dari Sanity

## Google Authentication

Web Komgallery menggunakan Google OAuth sebagai media login untuk user, agar fitur ini dapat digunakan berikut adalah cara cara yang harus dilakukan:
- Masuk dan login ke Goolgle Cloud API & Services
- Klik project Komgallery dan masuk kebagian credentials
- Tambahkan url `https://komgallery.netlify.app/` pada authorized javascript origin dan authorized javascript URIs
  
![Imgur](https://imgur.com/XgcDplg.png)

Dengan melakukan konfigurasi ini maka kita dapat mengguanakan Google Oauth pada web yg kita buat


## Kelebihan
## Kekurangan






