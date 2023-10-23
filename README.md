<div align="center">
  <h3 align="center">PEMROGRAMAN MOBILE</h3>
  <h3 align="center">UTS</h3>
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="img/logo_polinema.png" alt="Logo" width="300" height="300">
  </a>

  <h3 align="center">Abiyasa Putra Prasetya</h3>
  <h3 align="center">3G - D4TI</h3>
  <h3 align="center">01</h3>
  <h3 align="center">2141720203</h3>
</div>

# Praktikum 5: Membangun Navigasi di Flutter

Tampilan akhir yang akan Anda buat

<p align="center">
  <img src="img/praktikum_5/1.png" alt="Alt text">
</p>

Pada praktikum 5 ini anda akan belajar mengenai pembangunan aplikasi bergerak multi halaman. Aplikasi yang dikembangkan berupa kasus daftar barang belanja. Pada aplikasi ini anda akan belajar untuk berpindah halaman dan mengirimkan data ke halaman lainnya. Gambaran mockup hasil akhir aplikasi dapat anda lihat pada gambar di atas (mockup dibuat sederhana, sehingga Anda mempunyai banyak ruang untuk berkreasi). Desain aplikasi menampilkan sebuah ListView widget yang datanya bersumber dari List. Ketika item ditekan, data akan dikirimkan ke halaman berikutnya.

<h3>Langkah 1: Siapkan project baru<h3>

Sebelum melanjutkan praktikum, buatlah sebuah project baru Flutter dengan nama belanja dan susunan folder seperti pada gambar berikut. Penyusunan ini dimaksudkan untuk mengorganisasi kode dan widget yang lebih mudah.

<p align="center">
  <img src="img/praktikum_5/2.png" alt="Alt text">
</p>

<h3>Langkah 2: Mendefinisikan Route<h3>

Buatlah dua buah file dart dengan nama home_page.dart dan item_page.dart pada folder pages. Untuk masing-masing file, deklarasikan class HomePage pada file home_page.dart dan ItemPage pada item_page.dart. Turunkan class dari StatelessWidget. Gambaran potongan kode dapat anda lihat sebagai berikut.

<p align="center">
  <img src="img/praktikum_5/3.png" alt="Alt text">
</p>

<h3>Langkah 3: Lengkapi Kode di main.dart<h3>

Setelah kedua halaman telah dibuat dan didefinisikan, bukalah file main.dart. Pada langkah ini anda akan mendefinisikan Route untuk kedua halaman tersebut. Definisi penamaan route harus bersifat unique. Halaman HomePage didefinisikan sebagai /. Dan halaman ItemPage didefinisikan sebagai /item. Untuk mendefinisikan halaman awal, anda dapat menggunakan named argument initialRoute. Gambaran tahapan ini, dapat anda lihat pada potongan kode berikut.

<p align="center">
  <img src="img/praktikum_5/4.png" alt="Alt text">
</p>

<h3>Langkah 4: Membuat data model<h3>

Sebelum melakukan perpindahan halaman dari HomePage ke ItemPage, dibutuhkan proses pemodelan data. Pada desain mockup, dibutuhkan dua informasi yaitu nama dan harga. Untuk menangani hal ini, buatlah sebuah file dengan nama item.dart dan letakkan pada folder models. Pada file ini didefinisikan pemodelan data yang dibutuhkan. Ilustrasi kode yang dibutuhkan, dapat anda lihat pada potongan kode berikut.

<p align="center">
  <img src="img/praktikum_5/5.png" alt="Alt text">
</p>

<h3>Langkah 5: Lengkapi kode di class HomePage<h3>

Pada halaman HomePage terdapat ListView widget. Sumber data ListView diambil dari model List dari object Item. Gambaran kode yang dibutuhkan untuk melakukan definisi model dapat anda lihat sebagai berikut.

<p align="center">
  <img src="img/praktikum_5/6.png" alt="Alt text">
</p>

<h3>Langkah 6: Membuat ListView dan itemBuilder<h3>

Untuk menampilkan ListView pada praktikum ini digunakan itemBuilder. Data diambil dari definisi model yang telah dibuat sebelumnya. Untuk menunjukkan batas data satu dan berikutnya digunakan widget Card. Kode yang telah umum pada bagian ini tidak ditampilkan. Gambaran kode yang dibutuhkan dapat anda lihat sebagai berikut.

<p align="center">
  <img src="img/praktikum_5/7.png" alt="Alt text">
</p>

<p align="center">
  <img src="img/praktikum_5/8.png" alt="Alt text">
</p>

Output:

<p align="center">
  <img src="img/praktikum_5/run1.png" alt="Alt text">
</p>

<h3>Langkah 7: Menambahkan aksi pada ListView<h3>

Item pada ListView saat ini ketika ditekan masih belum memberikan aksi tertentu. Untuk menambahkan aksi pada ListView dapat digunakan widget InkWell atau GestureDetector. Perbedaan utamanya InkWell merupakan material widget yang memberikan efek ketika ditekan. Sedangkan GestureDetector bersifat umum dan bisa juga digunakan untuk gesture lain selain sentuhan. Pada praktikum ini akan digunakan widget InkWell.

Untuk menambahkan sentuhan, letakkan cursor pada widget pembuka Card. Kemudian gunakan shortcut quick fix dari VSCode (Ctrl + . pada Windows atau Cmd + . pada MacOS). Sorot menu wrap with widget... Ubah nilai widget menjadi InkWell serta tambahkan named argument onTap yang berisi fungsi untuk berpindah ke halaman ItemPage. Ilustrasi potongan kode dapat anda lihat pada potongan berikut.

<p align="center">
  <img src="img/praktikum_5/9.png" alt="Alt text">
</p>

# Tugas Praktikum 2

1. Untuk melakukan pengiriman data ke halaman berikutnya, cukup menambahkan informasi arguments pada penggunaan Navigator. Perbarui kode pada bagian Navigator menjadi seperti berikut.

<p align="center">
  <img src="img/praktikum_5/10.png" alt="Alt text">
</p>

2. Pembacaan nilai yang dikirimkan pada halaman sebelumnya dapat dilakukan menggunakan ModalRoute. Tambahkan kode berikut pada blok fungsi build dalam halaman ItemPage. Setelah nilai didapatkan, anda dapat menggunakannya seperti penggunaan variabel pada umumnya.

<p align="center">
  <img src="img/praktikum_5/11.png" alt="Alt text">
</p>

3. Pada hasil akhir dari aplikasi belanja yang telah anda selesaikan, tambahkan atribut foto produk, stok, dan rating. Ubahlah tampilan menjadi GridView seperti di aplikasi marketplace pada umumnya.

<p align="center">
  <img src="img/praktikum_5/12.png" alt="Alt text">
</p>

<p align="center">
  <img src="img/praktikum_5/13.png" alt="Alt text">
</p>

Output:

<p align="center">
  <img src="img/praktikum_5/rungrid.png" alt="Alt text">
</p>

Isi Grid View:

<p align="center">
  <img src="img/praktikum_5/run2.png" alt="Alt text">
</p>

4. Silakan implementasikan Hero widget pada aplikasi belanja Anda dengan mempelajari dari sumber ini: https://docs.flutter.dev/cookbook/navigation/hero-animations

<p align="center">
  <img src="img/praktikum_5/14.png" alt="Alt text">
</p>

5. Sesuaikan dan modifikasi tampilan sehingga menjadi aplikasi yang menarik. Selain itu, pecah widget menjadi kode yang lebih kecil. Tambahkan Nama dan NIM di footer aplikasi belanja Anda.

Home Page:

<p align="center">
  <img src="img/praktikum_5/15.png" alt="Alt text">
</p>

<p align="center">
  <img src="img/praktikum_5/16.png" alt="Alt text">
</p>

Output:

<p align="center">
  <img src="img/praktikum_5/run3.png" alt="Alt text">
</p>

Item Page:

<p align="center">
  <img src="img/praktikum_5/17.png" alt="Alt text">
</p>

<p align="center">
  <img src="img/praktikum_5/18.png" alt="Alt text">
</p>

<p align="center">
  <img src="img/praktikum_5/run4.png" alt="Alt text">
</p>