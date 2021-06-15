# Praktikum 11: PHP Framework (Codeigniter)

# Langkah-langkah Praktikum
# Persiapan
1. Persiapkan text editor misalnya VSCode
2. Buat folder baru dengan nama lab11_php_ci pada docroot webserver (htdocs)
3. Menggunakan XAMPP

Diperlukan konfigurasi pada webserver, mengaktifkan ekstensi PHP intl. Buka xampp control panel, pada bagian apache, klik config dan klik php.ini





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ec33be19a9c2c6247d1845418b450dfeef1eda13/ci4/gambar/xampp%20control%20panel.png)

Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan 
diaktifkan. Kemudian simpan kembali filenya





![input](https://github.com/ikmalriyan21/Lab11Web/blob/5cf85439470133e9784dbb321f3c2f388766a3d5/ci4/gambar/extension.png)

• Unduh Codeigniter dari website https://codeigniter.com/download
• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci. 
• Ubah nama direktory framework-4.x.xx menjadi ci4.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ef72d7155d3950d17692f9528e687012ef72ced2/ci4/gambar/welcome.png)

Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk 
mengakses CLI buka terminal/command prompt.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/0f4e411e3e67779bcac8e3f47694b7c4915580e6/ci4/gambar/menjalakan%20CLI.png)

Dan gunakan perintah untuk memanggil CLI Codeigniter "php spark"





![input](https://github.com/ikmalriyan21/Lab11Web/blob/b2425fdd6cf0dd7332960e5bf5941726682b51b7/ci4/gambar/php%20spark.png)

Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis 
errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi 
pada environment variable CI_ENVIRINMENT menjadi development.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/d83086099cfefacf3934941e54e6c88ca67fa4a4/ci4/gambar/production.png)

Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable 
CI_ENVIRINMENT menjadi development.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/c2f0e78862fc86159bf1fea01a15a5e1650695de/ci4/gambar/development.png)

Dan ini hasil errornya





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ed007fd1b6dc0b07327f59606c15fee1d7a7a6f3/ci4/gambar/parse%20error.png)

Contoh error yang terjadi. Untuk mencoba error tersebut, ubah kode pada file 
app/Controller/Home.php hilangkan titik koma pada akhir kode.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ccfb437e4991e8f65921f65e039e837a11c75e21/ci4/gambar/kode%20home%20titik%20koma.png)





![input](https://github.com/ikmalriyan21/Lab11Web/blob/f390a73da53c5f7bce0160a8c124822f11266b38/ci4/gambar/hasil%20kode%20home%20titik%20koma.png)

Pada Codeigniter, request yang diterima oleh file index.php akan diarahkan ke Router 
untuk meudian oleh router tesebut diarahkan ke Controller.

Router terletak pada file app/config/Routes.php





![input](https://github.com/ikmalriyan21/Lab11Web/blob/216c09278dac2267c338ce29214515c323f940dd/ci4/gambar/tempat%20codingan%20router.png)







