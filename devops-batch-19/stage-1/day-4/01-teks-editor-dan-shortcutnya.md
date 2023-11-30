# Teks Editor

Teks editor merupakan program komputer yang digunakan untuk membuat, mengedit, dan memformat teks. Beberapa contoh teks editor diantaranya : Notepad, Nano, Vim, Visual Studio Code, Sublime Text, dsb. Nano dan Vim sama-sama editor teks bawaan Linux. Teks editor Nano, biasanya digunakan untuk mengerjakan perubahan-perubahan kecil pada suatu file, sedangkan Vim biasanya digunakan untuk melakukan perubahan-perubahan yang lebih kompleks pada suatu file.

# Shortcut pada Teks Editor Nano

### Melihat versi Nano yang terpasang di perangkat

    nano --version

Perintah `nano --version` digunakan untuk melihat versi aplikasi Nano yang terinstal di perangkat.

![gambar versi nano](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-4/images/01-teks-editor-dan-shortcutnya/01-nano-version.png)

### Menginstall aplikasi Nano

    sudo apt-get install nano -y

Jika aplikasi Nano belum terpasang di perangkat, gunakan perintah `sudo apt-get install nano -y` untuk memasang aplikasi Nano ke perangkat.

![gambar install nano](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-4/images/01-teks-editor-dan-shortcutnya/02-install-apt-nano.png)

### Membuka file menggunakan aplikasi Nano

    nano nama-file.html

Untuk membuka file menggunakan aplikasi Nano, bisa menjalankan perintah `nano` diikuti `nama-file` yang ingin dibuka. 

![membuka file menggunakan nano](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-4/images/01-teks-editor-dan-shortcutnya/03.1-buka-file-dengan-nano.png)

![isi file](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-4/images/01-teks-editor-dan-shortcutnya/03.2-isi-file.png)

> **Catatan**

> Ketika menjalankan perintah `nano nama-file.html`, pastikan `nama-file` yang dituliskan ada di folder yang masih aktif. Jika tidak ada `nama-file` yang sama maka secara oromati akan dibuatkan file baru dengan nama yang diinputkan beserta ektensi yang diberikan.

### Shotcut ketika aplikasi Nano masih aktif

- `ctrl + o` : Menyimpan file yang sedang di edit, tanpa keluar dari aplikasi
- `ctrl + x` : Keluar dari aplikasi Nano
- `alt + u` : Undo
- `alt + e` : Redo
- `ctrl + k` : Cut
- `ctrl + u` : Copy
- `ctrl + t` : Paste
- `ctrl + a` : Menempatkan pointer untuk menulis ke bagian awal baris
- `ctrl + e` : Menempatkan pointer untuk menulis ke bagian akhir baris
- `ctrl + w` : Mencari kata atau karakter dalam teks
- `ctrl + r` : Menambahkan teks dari file yang dipilih
- `ctrl + n` : Menampilkan atau menyembunyikan nomor baris
- `ctrl + g` : Membuka menu bantuan. Berisi informasi tentang shortcut yang ada di aplikasi Nano
