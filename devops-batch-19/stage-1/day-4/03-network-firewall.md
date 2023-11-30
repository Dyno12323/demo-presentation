# Network Firewall

Firewall merupakan sistem keamanan yang melindungi komputer dari ancaman yang ada di jaringan internet. Firewall biasanya digunakan untuk melakukan penyaringan lalu lintas data, mengizinkan ataupun memblokir akses ke situs web, dan juga memantau lalu lintas jaringan. 

#### UFW (Uncomplicated Firewall)

Uncomplicated Firewall merupakan firewall sederhana yang ada pada os linux. UFW digunakan untuk melakukan pengaturan firewall. Perintah yang biasa digunakan untuk mengtur firewall menggunakan UFW

    sudo apt install ufw

Digunakan untuk melakukan instalasi aplikasi UFW

    sudo ufw enable

Mengaktifkan UFW

    sudo ufw allow 80/tcp

Menambahkan aturan : menizinkan lalu lintas TCP pada port 80

    sudo ufw status

Menampilkan aturan yang sudah di aktifkan


