Tugas 7
1. 
  a. StatelessWidget adalah widget yang tidak memiliki "state" yang dapat berubah setelah widget tersebut dibuat. Dengan kata lain, widget ini tidak bisa memperbarui tampilannya saat data berubah ataupun saat ada interaksi dari user. StatelessWidget cocok digunakan untuk elemen UI yang statis atau tidak akan berubah selama aplikasi berjalan, seperti ikon, teks, atau layout yang tidak perlu merespons perubahan.
  b. StatefulWidget adalah widget yang memiliki "state," yaitu data yang dapat berubah saat aplikasi berjalan, sehingga widget dapat merespons perubahan tersebut dan memperbarui tampilannya. StatefulWidget cocok digunakan untuk elemen UI yang membutuhkan interaksi atau harus memperbarui tampilannya berdasarkan input pengguna, seperti tombol, form input, animasi, dan lainnya yang berubah seiring waktu.
  c. Perbedaan utama antara StatelessWidget dan StatefulWidget adalah bahwa StatelessWidget tidak dapat berubah setelah di-build, sehingga cocok untuk elemen UI yang statis atau tidak akan diperbarui, sedangkan StatefulWidget memiliki data yang bisa berubah saat aplikasi berjalan, memungkinkan UI untuk beradaptasi dan merespons interaksi atau perubahan data.

2.
  a. MaterialApp = menyediakan struktur dan pengaturan dasar untuk aplikasi berbasis Material Design
  b. ThemeData = mengatur tampilan dan style keseluruhan aplikasi
  c. Scaffold = membuat struktur atau kerangka dasar untuk halaman
  d. AppBar = menampilkan header aplikasi di bagian atas layar
  e. Text = widget untuk menampilkan teks
  f. TextStyle = mengatur style dari teks
  g. Padding = memberikan space di sekitar atau di dalam widget
  h. Column = menyusun children di dalamnya secara vertikal
  i. Row = menyusun children di dalamnya secara horizontal
  j. InfoCard = widget yang dibuat sendiri untuk menampilkan informasi berupa `title` dan `content`
  k. Card = menampilkan elemen UI dengan efek shadow dan sudut yang round
  l. SizedBox = menyediakan space kosong dengan ukuran tertentu
  m. Center = memusatkan widget di dalamnya
  n. Gridview.count = widget grid yang menampilkan widget dalam bentuk grid dengan jumlah kolom yang ditentukan
  o. List.generate = membuat daftar widget ItemCard sesuai dengan panjang daftar items
  p. ItemCard = widget custom yang menampilkan icon dan teks
  q. Material = Wrapping widget lain dengan material, ngasih latar belakang dan efek shadow
  r. InkWell = Widget interaktif yang mendeteksi klik atau ketukan
  s. Container = membuat layout, memberikan padding, margin, atau warna latar belakang
  t. Icon = menampilkan icon
  u. SnackBar = menampilkan pesan sementara di bagian bawah layar
  v. ScaffoldMessenger = mengatur tampilan SnackBar

3.
   Fungsi setState()  digunakan dalam widget stateful untuk memperbarui tampilan atau UI aplikasi saat ada perubahan data. Ketika setState() dipanggil, Flutter akan menjalankan ulang metode build() pada widget tersebut untuk menampilkan data terbaru, sehingga tampilan aplikasi bisa disesuaikan secara dinamis berdasarkan data yang berubah. Yang terdampak oleh fungsi tersebut adalah widget yang memanggil setState(), subtree dari widget build(), variable yang ada di dalam setSTate()

4.
   const digunakan untuk nilai yang bersifat konstan dan harus sudah diketahui saat kompilasi. Objek yang dibuat dengan const tidak dapat diubah dan dioptimalkan oleh Dart untuk efisiensi memori. final digunakan untuk nilai yang hanya diinisialisasi sekali, tetapi bisa ditentukan saat runtime. Setelah nilai final ditetapkan, nilainya tidak bisa diubah lagi

5.
  a. Pertama saya membuat new flutter project (Empty app)
  b. Lalu saya mencoba menjalankan emulator terlebih dahulu
  c. Lalu saya membuat fungsi main di main.dart dan memanggil widget MyApp, tak lupa dengan import flutter
  d. Lalu saya membuat stateless widget di file main.dart dengan nama MyApp yang mereturn MaterialApp, lalu saya set title dan theme nya. Dan juga saya set home nya menjadi MyHomePage()
  e. Lalu saya membuat file baru bernama menu.dart, di file ini saya membuat stateless widget dengan nama MyHomePage yang me-return Scaffold
  f. Lalu saya set final variable seperti nama, npm, dan items
  g. di scaffold, saya membuat appbar dan column yang di-wrap dengan padding
  h. Di column, ada widget seperti row, center, dll
  i. Setelah membuat ItemHomepage yang berisi name dan icon, saya menggunakan model ini untuk mendefinisikan daftar item yang akan ditampilkan di dalam GridView.
  j. Di file menu.dart, saya membuat widget ItemCard yang menampilkan setiap item dari items dalam bentuk kartu. Setiap kartu akan menampilkan ikon dan teks yang sesuai dengan item.
Saya menggunakan Material sebagai latar belakang ItemCard dan mengatur warnanya agar berbeda-beda sesuai urutan item menggunakan list colors. Saya juga menambahkan efek ripple dengan InkWell agar kartu memiliki interaksi ketika ditekan.
  k. Di dalam GridView.count, saya menggunakan List.generate untuk membuat instance ItemCard berdasarkan data items yang telah saya definisikan.
Saya mengatur crossAxisCount di GridView.count menjadi 3 agar menampilkan 3 kolom, serta menambahkan jarak antar kartu menggunakan crossAxisSpacing dan mainAxisSpacing.
  l. Di dalam ItemCard, saya menambahkan logika untuk menampilkan SnackBar ketika item ditekan. Saya menggunakan ScaffoldMessenger.of(context).showSnackBar untuk menampilkan pesan bahwa tombol telah ditekan.
  m. Saya menjalankan aplikasi di emulator atau perangkat fisik untuk melihat hasilnya. Saya memastikan setiap item pada GridView muncul dengan warna yang berbeda dan bisa ditekan untuk memunculkan pesan SnackBar.
  n. Saya memastikan padding dan margin diatur dengan benar agar tampilan aplikasi terlihat rapi di berbagai ukuran layar.
Saya melakukan pengecekan bahwa aplikasi berjalan lancar tanpa error, dan setiap komponen tampil sesuai desain yang saya inginkan.
