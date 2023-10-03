# Deploy Configuration

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



## Database (Hanya dapat dilakukan oleh admin)
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
  
  ![Imgur](https://imgur.com/aVz5SQ7.png)

Dengan melakukan konfigurasi ini maka kita dapat mengguanakan Google Oauth pada web yg kita buat
