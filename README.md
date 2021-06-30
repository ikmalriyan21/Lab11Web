# Praktikum 11,12,13: PHP Framework (Codeigniter)

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

Membuat Route Baru.Tambahkan kode berikut di dalam Routes.php





![input](https://github.com/ikmalriyan21/Lab11Web/blob/2be52def552b2ddb950166642b0d0e96f223c983/ci4/gambar/kode%20routes.png)

Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dengan perintah "php spark routes"





![input](https://github.com/ikmalriyan21/Lab11Web/blob/443e28036aec6c9bef3848d7d31e968f3a471989/ci4/gambar/hasil%20php%20spark%20routes.png)

Mengakses file about.php akan terlihat seperti berikut , karena tidak ada isinya.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ddf3d7d7dc4491f8b36a084c1a6c91be73323036/ci4/gambar/tampilan%20error%20page.png)

Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php





![input](https://github.com/ikmalriyan21/Lab11Web/blob/95ac6d3ec8f92a0d12bc2cf1ccafac25ad35a94f/ci4/gambar/codingan%20controller%20page.png)

Selanjutnya refresh Kembali browser, maka akan ditampilkan hasilnya yaitu halaman 
sudah dapat diakses.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/e577efa336d389722cbaaf037168063c46062ea9/ci4/gambar/hasil%20output%20dari%20controller%20page.png)

Tambahkan method baru pada Controller Page seperti berikut.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ff7ce046aedcc9ad47b2bfc5251ef19413c2f2c6/ci4/gambar/method%20baru%20controller%20page.png)

Dan ini hasilnya





![input](https://github.com/ikmalriyan21/Lab11Web/blob/7ec11606c74edd23b1a99e98882588d4d4f34cde/ci4/gambar/hasil%20output%20method%20baru%20controller%20page.png)

Buat file baru dengan nama about.php pada direktori view (app/view/about.php)





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ea773c07fb6ebb1972d21bf6eff6904f26f2ffff/ci4/gambar/codingan%20membuat%20view.png)

Ubah method about pada class Controller Page menjadi seperti berikut





![input](https://github.com/ikmalriyan21/Lab11Web/blob/eb9109a21ba5530d13c9f49c188c233fd1821a6c/ci4/gambar/codingan%20ubah%20method%20about.png)

Kemudian lakukan refresh pada halaman tersebut.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/c5459123b76e571c9324e06077b56d0d59cc468a/ci4/gambar/hasil%20output%20ubah%20method%20about.png)

Buat file css pada direktori public dengan nama style.css





![input](https://github.com/ikmalriyan21/Lab11Web/blob/e5fcdf20e4620808be556d837e0a7d0accf47d53/ci4/gambar/file%20css.png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php

File app/view/template/header.php





![input](https://github.com/ikmalriyan21/Lab11Web/blob/c3656f3b4d160628aa4bd115f693852ab99fa1ff/ci4/gambar/codingan%20header.png)

File app/view/template/footer.php





![input](https://github.com/ikmalriyan21/Lab11Web/blob/e48a8f518040f66d31e66c6237bcce5811f1ff74/ci4/gambar/codingan%20footer.png)

Kemudian ubah file app/view/about.php seperti berikut.





![input](https://github.com/ikmalriyan21/Lab11Web/blob/ea4fa77f5773043a0e1dc20015674981d7fc7d26/ci4/gambar/codingan%20ubah%20about.png)

Dan ini hasilnya





![input](https://github.com/ikmalriyan21/Lab11Web/blob/069f26b0fcc4c022a092cf9f000cde5672477367/ci4/gambar/hasil%20output%20layout%20sederhana.png)

# Pertanyaan dan Tugas
Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga 
semua link pada navigasi header dapat menampilkan tampilan dengan layout yang 
sama.

Membuat sourch code seperti berikut pada file app/Controllers






![input](https://github.com/ikmalriyan21/Lab11Web/blob/3e54e0b893747731ee77d7f2b37ebdfaa2f90967/ci4/gambar/tugas.png)

# Praktikum 12

Membuat table dan database.




![input](https://github.com/ikmalriyan21/Lab11Web/blob/ca6145204f95af2759512431b1123bb06a9a270d/ci4/screenshot/table%20php%20MyAdmin.png)

Konfigurasi koneksi database untuk menghubungkan dengan database server
dengan mensetting file .env




![input](https://github.com/ikmalriyan21/Lab11Web/blob/604e0cca90505cd2e14c7a2004e3778984ebef63/ci4/screenshot/koneksi%20database.png)

Membuat model untuk memproses data Artikel.




![input](https://github.com/ikmalriyan21/Lab11Web/blob/13b743fc0828da424cca0677e048c9dad3a57e92/ci4/screenshot/codingan%20membuat%20model.png)

Membuat Controller dengan nama Artikel.php




![input](https://github.com/ikmalriyan21/Lab11Web/blob/dc2bd02342528298f573ee2e31bacf76cdf889fe/ci4/screenshot/codingan%20membuat%20controller.png)

Membuat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file 
baru dengan nama index.php




![input](https://github.com/ikmalriyan21/Lab11Web/blob/f3ccb7f176d64d84ebc1b192ef331d6a5a9869e0/ci4/screenshot/membuat%20view.png)

Hasil Outputnya




![input](https://github.com/ikmalriyan21/Lab11Web/blob/13fbaa197ddfde31c8b816eade7f56d1dd254918/ci4/screenshot/hasil%20output%20portal%20berita.png)

Menambahkan data dari sql tabel ke dalam tabel artikel




















