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
  j. InfoCard = widget yang dibuat sendiri untuk menampilkan informasi berupa title dan content
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


Tugas 8
1.  
Kegunaan const di Flutter dan Keuntungannya  
   a. const di Flutter digunakan untuk mendeklarasikan nilai yang bersifat konstan dan tidak akan berubah selama aplikasi berjalan. Dengan menggunakan const, Flutter dapat mengoptimalkan memori karena objek yang diinisialisasi dengan const hanya dibuat sekali dan dapat digunakan berulang kali tanpa membuat objek baru.
   b. Keuntungan menggunakan const adalah meningkatkan efisiensi aplikasi, baik dalam hal performa maupun memori, terutama pada elemen statis yang digunakan secara berulang. Ini membuat aplikasi lebih cepat dan ringan karena Flutter tidak perlu merebuild widget yang menggunakan const.
   c. Sebaiknya const digunakan pada widget atau nilai yang tidak memerlukan perubahan saat aplikasi berjalan, seperti teks statis, ikon, atau dekorasi tetap. const tidak diperlukan pada widget yang membutuhkan data atau properti dinamis yang berubah-ubah berdasarkan input pengguna atau variabel lain.

2. 
Perbandingan Column dan Row pada Flutter  
   a. Column adalah widget yang menyusun children-nya secara vertikal, dari atas ke bawah. Widget ini cocok untuk membuat layout yang menumpuk elemen satu per satu dalam urutan vertikal, misalnya pada form atau daftar teks dan tombol.
   b. Row adalah widget yang menyusun children-nya secara horizontal, dari kiri ke kanan. Row lebih cocok untuk tata letak yang ingin menampilkan beberapa elemen secara berdampingan, misalnya ikon dan teks di sebelahnya.
   c. Contoh implementasi:
     dart
     Column(
       children: [
         Text("Nama Produk"),
         Text("Deskripsi Produk"),
         ElevatedButton(onPressed: () {}, child: Text("Beli Sekarang"))
       ],
     );
     
     Row(
       children: [
         Icon(Icons.star),
         Text("Rating: 5.0"),
         ElevatedButton(onPressed: () {}, child: Text("Lihat Review"))
       ],
     );
     

3. 
Elemen Input yang Digunakan di Halaman Form  
   a. Pada halaman form yang dibuat, elemen input yang digunakan mencakup TextFormField untuk input seperti nama, deskripsi, dan harga. Selain itu, terdapat ElevatedButton untuk mengirim data form.
   b. Beberapa elemen input lain di Flutter yang tidak digunakan pada tugas ini adalah Slider, Switch, dan Radio. Slider cocok untuk input berbentuk rentang nilai, Switch untuk pilihan biner seperti on/off, dan Radio untuk pilihan tunggal dari beberapa opsi.

4. 
Pengaturan Tema (Theme) dalam Aplikasi Flutter  
   a. Tema diatur menggunakan ThemeData di dalam MaterialApp, yang memungkinkan pengaturan warna utama (primarySwatch), warna aksen (accentColor), dan gaya teks secara menyeluruh untuk aplikasi. Dengan tema, tampilan aplikasi bisa konsisten di seluruh halaman.
   b. Pada proyek ini, tema diimplementasikan dengan mengatur primarySwatch untuk warna utama dan accentColor untuk warna tambahan, sehingga tampilan aplikasi selaras dengan desain yang diinginkan.

5. 
Menangani Navigasi dalam Aplikasi dengan Banyak Halaman  
   a. Untuk menangani navigasi di aplikasi ini, saya menggunakan Navigator.push, Navigator.pushReplacement, dan Navigator.pop. Navigator.push digunakan untuk membuka halaman baru dan menambahkannya ke dalam stack, sehingga memungkinkan pengguna kembali ke halaman sebelumnya dengan tombol "back".
   b. Navigator.pushReplacement digunakan untuk mengganti halaman saat ini dengan halaman baru, seperti saat berpindah dari layar login ke halaman utama, agar halaman sebelumnya dihapus dari stack.
   c. Navigator.pop digunakan untuk menutup halaman saat ini dan kembali ke halaman sebelumnya, biasanya saat pengguna selesai mengisi form atau melihat detail.  
   
   Dengan kombinasi metode ini, aplikasi memiliki alur navigasi yang fleksibel dan intuitif, sehingga pengguna dapat dengan mudah berpindah antar halaman sesuai dengan kebutuhan aplikasi.



Tugas 9
1. Mengapa perlu membuat model untuk pengambilan atau pengiriman data JSON?  
   Model digunakan untuk mempermudah pengelolaan data yang diterima atau dikirim dalam format JSON jadi kita bisa mengonversi data JSON menjadi objek Dart yang lebih terstruktur dan mudah digunakan dalam aplikasi. Tanpa model, kita tetap bisa mengelola data JSON, tetapi prosesnya menjadi lebih rumit dan rawan error. Model membantu menjaga konsistensi dan memudahkan debugging serta pemeliharaan kode.

2. Fungsi dari library http yang digunakan pada tugas ini  
   Library http berfungsi sebagai alat untuk berkomunikasi dengan server melalui protokol HTTP. Pada tugas ini, library tersebut digunakan untuk melakukan permintaan (request) seperti GET atau POST ke backend (Django) dan menerima respons dari server. Contohnya, library ini memungkinkan Flutter mengambil daftar produk atau mengirim data login ke server.

3. Fungsi dari CookieRequest dan alasan penggunaannya di seluruh komponen  
   CookieRequest adalah class untuk menangani autentikasi berbasis cookie. Setelah user berhasil login, server Django mengirimkan cookie autentikasi sebagai respons. CookieRequest menyimpan cookie ini sehingga setiap permintaan berikutnya dari Flutter dapat menyertakan cookie tersebut untuk menjaga sesi user tetap aktif. Instance CookieRequest perlu dibagikan ke semua komponen di aplikasi agar setiap halaman dapat mengakses status autentikasi tanpa memerlukan login ulang.

4. Mekanisme pengiriman data dari input hingga ditampilkan di Flutter  
   - Input Data: User memasukkan data melalui UI di Flutter, misalnya detail produk.  
   - Pengiriman Data ke Server: Data dikirimkan ke backend Django menggunakan http.post atau CookieRequest.post dalam format JSON.  
   - Proses di Backend: Django memproses data tersebut, misalnya menyimpannya ke database atau memvalidasi data.  
   - Respon dari Server: Django mengirimkan respon (biasanya dalam format JSON) kembali ke Flutter, berisi hasil operasi (misalnya, data yang disimpan atau pesan sukses).  
   - Menampilkan Data: Flutter mem-parsing respon JSON menjadi objek yang terstruktur (berbasis model) dan menampilkannya di UI aplikasi.

5. Mekanisme autentikasi (login, register, logout)  
   - Register:  
     User memasukkan data akun di Flutter, seperti username dan password. Data ini dikirim ke Django melalui http.post. Django memvalidasi data tersebut (misalnya, memastikan password memenuhi kriteria) dan menyimpan akun baru di database. Jika validasi berhasil, Django mengirimkan respons ke Flutter bahwa proses pendaftaran sukses.  
   - Login:  
     User memasukkan username dan password di Flutter, yang kemudian dikirimkan ke Django melalui http.post. Django mencocokkan data dengan database. Jika berhasil, Django mengirimkan cookie autentikasi kepada Flutter sebagai tanda user berhasil login. Cookie ini disimpan di CookieRequest untuk digunakan pada permintaan berikutnya.  
   - Logout:  
     User memilih logout di aplikasi. Flutter mengirimkan permintaan logout ke Django. Django menghapus sesi autentikasi user dan mengirimkan respon sukses ke Flutter. Setelah logout, cookie autentikasi dihapus, sehingga user perlu login ulang untuk mengakses fitur tertentu.

6. 
 a. Setup Autentikasi pada Django untuk Flutter
 a.a. Membuat Django App
- Saya membuat app baru bernama authentication di Django dengan perintah python manage.py startapp authentication
  
- Kemudian, saya menambahkan authentication ke INSTALLED_APPS di settings.py untuk mendaftarkan app ini agar Django mengenalinya.

 a.b. Instalasi django-cors-headers
- Saya menginstal library django-cors-headers dengan perintah pip install django-cors-headers
- Library ini penting agar Django dapat menerima request dari Flutter
 a.c. Konfigurasi CORS di settings.py
- Saya menambahkan:
  CORS_ALLOW_ALL_ORIGINS = True
  CORS_ALLOW_CREDENTIALS = True
  CSRF_COOKIE_SECURE = True
  SESSION_COOKIE_SECURE = True
  CSRF_COOKIE_SAMESITE = 'None'
  SESSION_COOKIE_SAMESITE = 'None'
 a.d. Konfigurasi ALLOWED_HOSTS
- Menambahkan 10.0.2.2 ke ALLOWED_HOSTS agar emulator Android bisa mengakses server Django.
 b. Implementasi Endpoint Login
 b.a. Fungsi Login
- Saya membuat view login di authentication/views.py:
  - Fungsi ini mengecek username dan password menggunakan authenticate dari Django.
  - Jika valid, user akan login, dan Django mengembalikan JSON respons yang berisi status login dan username.
 b.b. URL Routing
- Saya menambahkan endpoint login ke authentication/urls.py:
  from authentication.views import login
  urlpatterns = [path('login/', login, name='login')]
 b.c. Testing Login
- Saya mencoba mengakses endpoint ini melalui Postman dengan mengirim username dan password, memastikan respons JSON sesuai.
 c. Integrasi dengan Flutter
 c.a. Setup Provider dan CookieRequest
- Di main.dart, saya wrap MaterialApp dengan Provider
 c.b. Halaman Login
- Saya membuat halaman login.dart:
 d. Setup Register pada Django
 d.a. Fungsi Register
- Membuat fungsi register di Django:
  - Fungsi ini menerima data POST berupa username, password1, dan password2.
  - Mengecek kesesuaian password dan apakah username sudah ada.
  - Jika valid, membuat user baru menggunakan User.objects.create_user().

 d.b. URL Routing
- Menambahkan endpoint register di authentication/urls.py:
 e. Integrasi Halaman Register di Flutter
- Membuat halaman register.dart:
  - Mirip dengan login, tetapi mengirimkan username, password1, dan password2 ke endpoint register/.
  - Jika sukses, aplikasi menavigasi ke halaman login.
 f. Fetch Data dari Django ke Flutter
 f.a. Fungsi Fetch di Flutter
- Di Flutter, saya membuat fungsi fetch data JSON dari endpoint Django
 f.b. Tampilan List
- Membuat widget ListView.builder di Flutter untuk menampilkan data produk dalam daftar.
 g. Logout
 g.a. Endpoint Logout di Django
- Membuat fungsi logout:
 g.b. Implementasi Logout di Flutter
- Menambahkan opsi logout di menu, menghapus cookie, dan menavigasi kembali ke halaman login.