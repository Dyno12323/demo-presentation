# Text Manipulation

Manipulasi teks merupakan suatu kegiatan mengubah atau mengolah teks pada suatu file. Beberapa perintah yang biasa digunakan untuk memanipulasi teks

### `cat`

Perintah `cat` dapat digunakan untuk membuat file baru, menambahkan kata atau perintah kedalam file, ataupun menggabungkan isi file.

#### Membuat file baru menggunakan perintah `cat`

Perintah `cat` dapat digunakan untuk membuat file baru. Jalankan perintah `cat > nama-file` dan file akan terbuat di folder yang masih aktif. Ganti `nama-file` pada perintah tersebut menggunakan nama file yang diinginkan.

![gambar membuat file dengan printah cat]()

> **Catatan**

> Setelah menjalankan perintah `cat > nama-file`, isi file tersebut kemudian tekan `ctrl + c` untuk menyimpan.

#### Menambahkan kata pada suatu file dengan perintah `cat`

Untuk menambahkan kata pada suatu file, jalankan perintah `cat >> nama-file`. Jalankan perintahnya dan masukkan kata yang ingin di tambahkan. Setelah selesai, tekan `ctrl + c` untuk mengakhiri perintah. Pada perintah tersebut, `nama-file` menunjuk kepada nama file yang ingin dimodifikasi.

![gambar menambahkan kata dengan cat]()

#### Menggabungkan isi dari dua file menggunakan perintah `cat`

Untuk meggabungkan isi dari dua file kemudian menyimpannya menjadi file yang berbeda, jalankan perintah `cat file-1 file-2 > file-3`. Pada perintah tersebut, `file-1` dan `file-2` merupakan file yang ingin dijadikan satu isinya. Kemudian `file-3` merupakan nama file baru hasil penggabungan dari dua file.

![gambar menggabungkan 2 file]()

#### Mencari dan merubah kata tertentu dalam suatu file dengan perintah `sed`

Untuk mencari suatu kata pada file tertentu dan mengubah kata yang dicari menjadi kata yang lain, dapan menjalankan perintah `sed -i 's/Kata1/Kata2/g' nama-file`. Perintah `-i` menyatakan perubahan langsung diterapkan di file, `'s/` merupakan perintah untuk mengganti teks, `Kata1/` merupakan kata yang dicari dan ingin diganti, `Kata2/` kata yang ingin diterapkan, `g'` perubahan diterapkan ke seluruh teks yang sesuai.

![gambar]()
