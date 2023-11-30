# Reverse Proxy

Reverse proxy adalah web server yang berada di antara klien dan server tempat menyimpan data. Reverse proxy berfungsi diantaranya menyembunyikan infrastruktur server, load balancing, dan caching.

### Membuat konfigurasi reverse proxy

Masuk ke folder nginx kemudian buat pengaturan baru. Caranya buat folder baru kemudian masuk ke folder baru tersebut dan buat file baru dengan ektensi `.conf`

    cd /etc/nginx
    sudo mkdir konfigurasi-rp
    cd konfigurasi-rp
    sudo touch reverse-proxy.conf

![gambar file baru]()

Masukkan kode berikut ke dalam file yang baru dibuat

    server { 
        server_name domainsaya.xyz; 
      
        location / { 
                 proxy_pass http://127.0.0.1:3000;
        }
    }

Penjelasan mudah dari kode di atas adalah, ketika ada yang meminta request ke `domainsaya.xyz` maka request akan diteruskan ke `127.0.0.1:3000`. Setelah selesai menuliskan kode tersebut, keluar dari folder dan buka file `nginx.conf` untuk melanjutkan konfigurasi.

![gambar konfig nginx]()

Pergi ke bagin bawah sampai pada `virtual host configs` untuk memasukkan pengaturan yang dibuat tadi.

![gambar konfigurasi virtual host]()

Lakukan pengecekan dengan menjalankan kode `sudo nginx -t`. Jika tidak terjadi error restart nginx dengan menjalankan perintah `sudo systemctl restart nginx`. 

![gambar tes syntax]()

Agar domain yang dibuat tadi dapat dipanggil, maka harus membuat virtual host. Edit file bernama `hosts` yang ada di folder `etc`. Karena belum memiliki ip public, ubah localhost dengan nama domain yang tadi dibuat. 

![gambar membuat virtual host]()

Setelah selesai buka browser dan buka domain yang tadi dibuat. Muncul bad gateway karena memang belum ada laman yang berjalan di localhost port 3000.

![gambar bad gateway]()

Untuk melihat apakah pengaturan benar-benar berhasil, coba unduh aplikasi berbasis web dan lakukan pengaturan sesuai dokumentasinya. Ketika merefresh domain yang dikonfigurasi tadi maka laman akan termuat.

    git clone https://github.com/dumbwaysdev/dumbflix-frontend.git

> Tautan aplikasi baerbasis web yang digunakan untuk ujicoba

![gambar uji coba]()
