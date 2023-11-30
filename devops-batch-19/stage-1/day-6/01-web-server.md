# Web Server

Web Server adalah perangkat lunak yang menyediakan layanan kepada pengguna melalui jaringan internet. Fungsi utama dari web server adalah menyajikan halaman web kepada klien yang mengaksesnya. Cara kerjanya adalah ketika web server menerima request dari klien maka web server akan memberi respon sesuai dengan permintaan klien.

![gambar]()

> Proses kerja web server

### Menjalankan Web Server menggunakan nginx

Nginx adalah salah satu dari macam-macam web server. Untuk menjalankan web server nginx, perangkat perlu terintall nginx. Jalankan perintah berikut secara berurutan.

    sudo apt update
    sudo apt install nginx
    sudo systemctl status nginx

> `sudo apt update` adalah perintah untuk memperbarui sistem
> 
> `sudo apt install nginx` adalah perintah untuk menginstall nginx
> 
> `sudo systemctl sattus nginx` adalah perintah untuk melihat status nginx

![gambar status nginx]()

Untuk mengecek berjalan tidaknya nginx, buka browser dan masukkan alamat `localhost`. 

![gambar localhost]()

### Perintah untuk mengelola layanan nginx

##### Memulai nginx

    sudo systemctl start nginx

Perintah tersebut digunakan untuk memulai layanan nginx untuk merespon permintaan yang datang ke server.

##### Menghentikan nginx

    sudo systemctl stop nginx

Perintah tersebut digunakan untuk menghentikan layanan nginx yang sedang berjalan.

##### Memuat ulang nginx (restart)

    sudo systemctl restart nginx

Perintah tersebut digunakan untuk menghentikan layanan Nginx, kemudian menyalakan kembali layanan Nginx.

##### Reload nginx

    sudo systemctl reload nginx

Perintah tersebut digunakan untuk memuat ulang konfigurasi tanpa menghentikan layanan. Perintah ini digunakan ketika melakukan perubahan pada file konfigurasi Nginx dan ingin menerapkan perubahan tersebut tanpa mempengaruhi koneksi yang sedang berjalan.

##### Enable nginx

    sudo systemctl enable nginx

Perintah tersebut mengatur agar memulai layanan nginx secara otomatis pada saat startup.

#### Disable nginx

    sudo systemctl disable nginx

Perintah tersebut mengatur agar layanan nginx tidak secara otomatis dijalankan ketika startup.
