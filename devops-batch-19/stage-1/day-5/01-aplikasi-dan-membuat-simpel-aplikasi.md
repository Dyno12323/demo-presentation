# Aplikasi dan Membuat Aplikasi Sederhana

Aplikasi adalah program komputer yang menjalankan perintah tertentu dan hasilnya biasanya digunakan oleh pengguna. Aplikasi sederhana merupakan aplikasi yang memiliki fungsi tertentu dan tidak kompleks, serta memiliki tujuan spesifik yang mudah dipahami.

## Membuat Aplikasi Sederhana dengan NodeJS

Untuk dapat membuat aplikasi sederhana menggunakan nodejs, tentu perngkat harus terinstall nodejs. Jalankan perintah berikut untuk mengintall nodejs di perangkat.

    sudo apt update

> Melakukan pembaruan sistem yang ada di perangkat

    sudo apt install software-properties-common apt-transport-https ca-certificates gnupg2 curl build-essential

> Memasang dependensi yang diperlukan

![gambar install dependensi](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-5/images/nodejs-install-depedensi.png)

    curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg

> Mengunduh resource

    sudo apt-get install nodejs -y

> Menginstall nodejs

![gambar install nodejs](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-5/images/nodejs-instal-nodejs.png)

Setelah proses instalasi selesai, jalankan perintah `node --version` untuk melihat versi nodejs yang terinstall. Untuk memulai membuat aplikasi sederhana, buatlah file dengan ektensi `.js` dan ketikkan kode berikut.

    const http = require('http');
    const port = 3000;
    
    const server = http.createServer((req, res) => {
      res.writeHead(200, {'Content-Type': 'text/plain'});
      res.end('Halo. Saya sedang belajar DevOps\n');
    });
    
    server.listen(port, () => {
      console.log(`Listening Port ${port}`);
    });

> Kode tersebut akan membuat laman http sederhana yang menampilkan pesan "Halo. Saya sedang belajar DevOps"

Simpan dan jalankan di terminal dengan menjalankan perintah `node nama-file.js`. Untuk melihat hasilnya, buka browser dan masukkan alamat `localhost:3000`

![gambar hasil koding](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-5/images/nodejs-hasil-koding.png)

## Membuat aplikasi sederhana menggunakan bahasa Go (Golang)

Untuk memulai membuat aplikasi sederhana menggunakan bahasa Go, perangkat mesti terinstall bahasa pemrogaman Go. Berikut cara install bahasa go menggunakan terminal.

    sudo apt update
    sudo apt install golang

> Pastikan perangkat sudah up to date dengan menjalankan perintah `sudo apt update` selanjutnya install Golang menggunakan perintah `sudo apt install golang`

![gambar install golang](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-5/images/golang-install-golang.png)

Untuk melihat versi go yang terinstall di perangkat, jalankan perintah `go version`. Selanjutnya buatlah file dengan ektensi `.go` untuk mulai membuat aplikasi sederhana menggunakan golang. Masukkan kode berikut pada file yang dibuat.

    package main
    import "fmt"
    func main() {
        fmt.Println("Halo. Saya sedang belajar Devops")
    }

> Kode tersebut akan menampilkan pesan "Halo. Saya sedang belajar DevOps" ke terminal.

Simpan dan jalankan di terminal dengan menjalankan perintah `go run nama-file.go`.

![gambar menjalankan file golang](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-5/images/golang-menjalankan-file-golang.png)

## Membuat aplikasi sederhana menggunakan bahasa Pyton

Secara default bahasa pemrogaman python sudah terinstall di perangkat. Untuk melihat python yang terinstall, jalankan perintah `python3 --version`. Untuk mulai membuat aplikasi, pertama install packege manager python3 menggunakan perintah `sudo apt install python3-pip` dan `pip install flask` secara berurutan.

![gambar install pip](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-5/images/python-instal-pip.png)

Setelah packegenya terinstall, buat file dengan ekstensi `.py` kemudian masukkan kode berikut

    from flask import Flask
    app = Flask(__name__)
    @app.route("/")
    def variabel1():
        return "Halo. Saya sedang belajar DevOps"
    if __name__ == "__main__":
        app.run()

> Kode tersebut akan membuat laman http sederhana yang menampilkan pesan "Halo. Saya sedang belajar DevOps"

Simpan dan jalankan di terminal dengan menjalankan perintah `python3 nama-file.py`. Untuk melihat hasilnya, buka browser dan masukkan alamat `localhost:5000`

![gambar-hasil-koding](https://github.com/Dyno12323/devops-batch-19/blob/master/devops-batch-19/stage-1/day-5/images/python-hasil-koding.png)
