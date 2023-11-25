# Inisiasi Github

Agar dapat menjalankan aplikasi github di perangkat komputer, tentunya perlu menginstall aplikasi github terlebih dahulu. Aplikasi github dapat diinstall melalui sofware manager atau menggunakan command di terminal. Sebelum melakukan istallasi github, pastikan sistem pada pada perangkat komputer sudah up to date. Untuk melakukannya, dapat menjalankan perintah `sudo apt update` dan `sudo apt upgrade`

![gambar sudo apt update](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-3/images/01-sudo-apt-update.png)

*Gambar 2.1 : Perintah `sudo apt update`*

![gambar sudo apt upgrate](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-3/images/02-sudo-apt-upgrade.png)

*Gambar 2.2 : Perintah `sudo apt upgrade`*


Perintah `sudo apt update` digunakan untuk mencari software dan aplikasi yang perlu untuk diperbarui, sedangkan perintah `sudo apt upgrade` digunakan untuk memasang pembaruan.  Langkah selanjutnya adalah memasang aplikasi github. Untuk melakukannya, dapat memasukkan perintah `sudo apt install apt git`

*gambar sudo apt install git*

Pastikan aplikasi github sudah terpasang di perangkat. Untuk melakukannya, jalankan perintah `git --version`. Perintah ini digunakan untuk mengetahui versi dari github yang terpasang di perangkat yang digunakan.

*gambar git --version*


# Konfigurasi Github

Langkah pertama agar dapat mulai bekerja menggunakan aplikasi github, pastinya melakukan konfigurasi aplikasi tersebut. Hal ini perlu dilakukan agar semua perubahan-perubahan yang dilakukan dapat terbaca oleh sistem. Hal pertama yang harus disapkan sebelum melakukan konfigurasi github adalah akun. Akun github bisa dibuat di laman https://github.com 

*gambar laman utama github*

Untuk memulai konfigurasi aplikasi github, dapat menjalankan perintah `git config --global user.name “username”` dan `git config --global user.email “alamat email”`. Pada perintah pertama, ganti `“username”` menggunakan username yang sudah terdaftar di github. Pada perintah kedua, ganti `“alamat email”` menggunakan email yang terdaftar di github. Selanjutnya untuk melihat daftar konfigurasi yang ada pada repositori lokal, dapat menggunakan perintah `git config --list`

*gambar git config dan list*

Langkah berikutnya adalah menghubungkan repositori lokal pada perangkat komputer dengan platform github. Untuk melakukannya diperlukan secure shell (SSH) yang berfungsi untuk menghubungkan dua perangkat melalui jaringan yang aman. Untuk mendapatkan SSH-key dapat menjalankan perintah `ssh-keygen`

*gambar ssh-keygen*

Tunggu hingga proses selesai, perangkat akan membuat file tersembunyi bernama `.ssh` yang secara default berada di home. Buka file dengan nama `id_rsa.pub` dan salin isi file tersebut.

*gambar id_rsa.pub*

Masuk ke akun github, dan pergi ke menu pengaturan kemudian pilih menu SSH and GPG Keys.

*gambar*

Di dalam menu SSH and GPG Keys, pilih opsi new SSH Key dan lengkapi formulirnya.

*gambar*

Setelah selesai mengisi formulir, jalankan perintah `ssh -T git@github.com` di terminal untuk memastikan perangkat benar-benar terhubung dengan platform github.

*cek koneksi*


# Membuat Repositori Github

Repositori merupakan tempat penyimpanan file dan semua riwayat perubahannya dari sebuah proses pengembangan perangkat lunak. Untuk membuat repositori, pilih menu new reopsitory pada platform github dan lengkapi formulirnya.

*gambar*

Salin alamat repositori yang diberi, nantinya akan diminta waktu menjalankan perintah `remote`. Sekarang, jalankan perintah `git init`, untuk membuat repositori lokal, akan tetapi repositori yang terbuat adalah repositori kosong tanpa file dan folder.

*gambar git init*

Selanjutnya jalankan perintah `mkdir “nama folder”`  atau `touch “nama file”`. Perintah `mkdir` digunakan untuk membuat folder baru, dan perintah `touch` digunakan untuk membuat file baru.

*gambar mkdir dan touch*

Supaya semua perubahan yang dilakukan di repositori lokal dapat terbaca oleh sistem, selanjutnya jalankan printah `git remote add “nama remote” “alamat SSH”`. `alamat SSH` didapatkan setelah membuat repositori di platform Github. Untuk menampilkan daftar remote yang terhubung jalankan perintah `git remote -v`

*gambar git remote add dan statusnya*

Untuk melihat perubahan apa saja yang dilakukan di repositori lokal dan belum terbaca oleh sistem Github, jalankan perintah `git status`. Dari gambar berikut terdapat informasi berupa, pengguna berada di branch master dan terdapat file yang belum terbaca oleh sistem Github

*gambar git status*

Supaya perubahan yang dilakukan pada repositori lokal dapat terbaca oleh sistem Github, jalankan perintah `git add “nama file”` untuk menambahkan file ke tahapan staging, atau jalankan perintah `git add .` untuk menambahkan semua folder dan file yang yang ada di folder yang masih aktif ke tahapan staging.

*gambar git add file*

Setelah file masuk ke tahap staging, jalankan perintah `git commit -m “pesan”`. Perintah ini digunakan untuk memberi pesan kepada komunitas atau pengembang lain tentang suatu perubahan yang dilakukan terhadap suatu file.

*gambar git commmit*

Setelah menjalankan perintah `git add` dan `git commit`, selanjutnya jalankan perintah `git push “nama remote” “nama branch”`. Perintah ini digunakan untuk mengupload file dan folder ke sistem Github.
> *catatan sebelum menjalankan perintah `git push` baiknya jalankan perintah `git status` dan `git remote -v` untuk melihat nama remote dan juga nama branch.*

*gambar git push*

Untuk melihat apakah repositori lokal benar-benar sudah terupload ke sistem Github, pengguna dapat melihatnya di laman github dan masuk ke menu your repositories.

*gambar*
