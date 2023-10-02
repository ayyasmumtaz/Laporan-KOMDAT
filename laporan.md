# KomGallery

## Deskripsi Singkat

KomGallery adalah aplikasi media sosial yang dirancang khusus untuk mahasiswa Ilmu Komputer di Universitas IPB. Ini berfungsi sebagai platform untuk berbagi foto dengan lancar di antara komunitas mahasiswa, memfasilitasi kolaborasi, dan memupuk rasa keterlibatan komunitas. Pengguna dapat mengunggah, memberi komentar, menyimpan, dan mengunduh foto, serta mengaitkan tautan yang relevan dengan setiap foto, memungkinkan manfaat tambahan seperti promosi acara dan sumber daya terkait.

## Technology Stack

Frontend KomGallery dikembangkan menggunakan HTML, CSS, dan JavaScript sebagai bahasa pemrograman inti. Untuk membangun antarmuka pengguna yang kuat dan interaktif, kami memilih kerangka kerja React.js. Dengan memanfaatkan kekuatan React.js, kami menggunakan konsep-konsep kunci seperti komponen, props, manajemen state, dan metode siklus hidup komponen untuk mengorganisir dan mengelola logika tampilan aplikasi dengan efisien. Selain itu, kami menggunakan kerangka kerja Tailwind CSS, yang mengikuti pendekatan utilitas pertama, memungkinkan kami untuk dengan mudah mengonfigurasi struktur tata letak dan menerapkan gaya CSS yang telah ditentukan sebelumnya untuk meningkatkan estetika visual dan responsivitas aplikasi.

Di bagian belakang, kami mengadopsi pendekatan CMS tanpa kepala dengan menggunakan Sanity. Sanity bertindak sebagai penyedia konten dan berfungsi sebagai repositori sentral untuk menyimpan berbagai konten aplikasi, termasuk foto yang diunggah oleh pengguna. Dengan memanfaatkan API JavaScript yang disediakan oleh Sanity, kami secara lancar berinteraksi dengan sistem manajemen konten untuk melakukan operasi CRUD (Create, Read, Update, Delete) yang penting, memastikan manajemen dan pengambilan konten yang efisien.

## User Authentication

Untuk memastikan akses yang aman dan manajemen pengguna, kami mengintegrasikan Otentikasi Google (OAuth) sebagai layanan pihak ketiga. Dengan memanfaatkan OAuth, pengguna dapat masuk ke KomGallery dengan aman menggunakan akun Google mereka, menghilangkan kebutuhan untuk manajemen otentikasi pengguna secara manual. Integrasi ini bergantung pada infrastruktur keamanan yang kuat yang disediakan oleh Google, memastikan otentikasi pengguna yang lancar, andal, dan sangat aman.

## Deployment

KomGallery di-deploy menggunakan Netlify, platform kuat untuk penyebaran berkelanjutan dan hosting. Proses penyebaran ini diatur dengan baik, memungkinkan penyebaran otomatis setiap kali perubahan diunggah ke repositori. Versi langsung dari KomGallery dapat diakses di https://komgallery.netlify.app, di mana pengguna dapat menjelajahi fitur dan fungsionalitasnya.

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

### instalasi dependencies
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




