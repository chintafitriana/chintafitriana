### Praktikum Pemrograman Berorientasi Framework Minggu 1👋

Hi,👋
Nama: Chinta Sejatining Fitriana,
NPM: 220102079,
Kelas: TI 2D

10 Poin ringkasan dari dokumentasi codeigniter4 versi saya 😁

1. **Welcome to codeigniter,** <br>
CodeIgniter adalah kerangka kerja (framework) aplikasi web yang ditulis dalam bahasa pemrograman PHP.
Ini adalah salah satu kerangka kerja PHP yang populer dan digunakan secara luas oleh para pengembang untuk mempercepat pengembangan aplikasi web. <br>
Codeigniter ramai digunakan oleh para pengembang software saat ini karena beberapa keuntungan yang didapatkan, diantaranya yaitu: <br>
  - Konfigurasi mudah <br>
  - Kinerja yang cepat <br>
  - Ramah untuk pemula <br>
  - Keamanan yang terintegrasi <br>
  - Komunitas yang banyak <br>
  
2. **Instalasi** <br>
Terdapat 2 cara instalasi framework codeigniter 4, diantaranya yaitu: <br>
a) Manual <br>
Unduh file CodeIgniter 4 dari situs web resmi www.codeigniter.com, lalu ekstrak file tersebut. <br>

   b) Composer <br>
  Gunakan Composer dengan perintah untuk membuat proyek CodeIgniter baru. <br>
```
_composer create-project codeigniter4/appstarter nama_fileproject_
```
 <br> 
Serta jangan lupa untuk mengubah root pada laragon/xampp yang anda gunakan agar dapat running di web server nantinya. <br> 
Lalu ketikkan sintaks berikut untuk running aplikasi web anda melalui localhost yang disediakan. <br>
Untuk running localhost dapat menggunakan sintaks berikut: <br>

Sehingga muncul localhost berikut, yang dapat anda klik dengan menekan tombol _Ctrl + arahkan ke link, lalu klik_:



3. **Setting Development Mode** <br>
Dalam CodeIgniter 4, Anda dapat mengatur mode pengembangan (development mode) dengan mengubah nilai konstanta CI_ENVIRONMENT pada file .env di folder proyek.
Fungsi file .env merupakan file konfigurasi yang digunakan untuk menyimpan variabel lingkungan (environment variables) yang digunakan oleh aplikasi.
Berikut contoh gambarnya, sintaks asli bawaan dari ci4 saat pertama kali instal adalah terdapat tanda # pada awalan, hapus tanda # agar memulai mode development. <br>
```
# ENVIRONMENT
#--------------------------------------------------------------------

CI_ENVIRONMENT = development

#--------------------------------------------------------------------
# APP
#--------------------------------------------------------------------
```
Fungsi mengubah dari production ke development adalah untuk memudahkan debugging pada saat error, berikut contoh tampilan dari debugging. <br>
![image](https://github.com/chintafitriana/chintafitriana/assets/118662112/928704ed-c032-4d5a-b81c-3bd0e82e0a4f)

4. **Struktur Folder** <br>
Codeigniter4 dikenal dengan konsep MVC nya (Models, View, Controller) Struktur folder pada codeigniter4 meliputi:<br>
a) app <br>
- Controllers: Berisi file-controller yang mengatur logika aplikasi dan berinteraksi dengan Model dan View. <br>
- Models: Berisi file-model yang mengelola logika bisnis dan akses data.<br>
- Views: Berisi file-view yang menampilkan tampilan halaman web.<br>
- Config: Berisi file konfigurasi untuk aplikasi, seperti pengaturan database, rute, dan lainnya.<br>
- Helpers: Berisi file-helper yang berisi fungsi-fungsi bantu yang dapat digunakan di seluruh aplikasi.<br>
- Libraries: Berisi file-libraries yang menyediakan fungsionalitas tambahan untuk aplikasi.<br>
- Migrations: Berisi file migrasi database untuk mengelola perubahan skema database.<br>
- Seeds: Berisi file-seeder yang digunakan untuk mengisi data awal ke dalam database.<br>
b) public: Berisi file publik seperti CSS, JavaScript, gambar, dan file statis lainnya yang dapat diakses secara langsung oleh browser.<br>
c) system: Berisi file inti CodeIgniter yang memproses permintaan dan mengatur aliran aplikasi.<br>
d) writable: Direktori yang digunakan untuk menyimpan file yang dapat ditulis oleh aplikasi, seperti file log, file sesi, dan file cache.<br>
e) tests: Berisi file pengujian aplikasi menggunakan PHPUnit.<br>
f) vendor: Direktori yang berisi dependensi pihak ketiga yang diinstal melalui Composer.<br>

5. **Routing** <br>
Routing adalah proses menghubungkan URL yang diterima oleh aplikasi web dengan tindakan atau fungsi tertentu yang harus dilakukan oleh aplikasi tersebut.
Dalam kerangka kerja web CodeIgniter, routing digunakan untuk menentukan bagaimana URL yang dikirim oleh pengguna akan diarahkan ke fungsi atau metode yang sesuai dalam aplikasi.
Pada codeigniter, terdapat 3 istilah mengenai route diantaranya yaitu: <br>
a) Routes adalah kumpulan definisi routing. <br>
b) Router adalah script yang menentukan routing. <br>
c) Routing adalah proses menemtukan rute atau url yang dituju. <br>
Routing bisa di edit pada direktori **_app > Config > Routes.php_**<br>
Contoh penulisan sintaks route:
```
//untuk dashboard bawaan ci4
$routes->get('/', 'Home::index');
//untuk masuk ke page test
$routes->get('/test', 'Test::test');
```

6. **Model** <br>
Model bertanggung jawab untuk berinteraksi dengan database atau sumber daya data lainnya. Ini dapat mencakup operasi seperti pengambilan, penambahan, pembaruan, dan penghapusan data.
Model juga dapat berisi metode khusus untuk memperoleh dan memanipulasi data sesuai kebutuhan aplikasi. Untuk membuat model pada codeigniter4 ini dapat dibuat pada direktori _**app > Model**_
lalu buat model sesuai yang anda inginkan. Pada contoh kali ini saya membuat model _**TestModel.php.**_ <br>
![image](https://github.com/chintafitriana/chintafitriana/assets/118662112/9ff13e8d-2dc3-459e-8ef4-0c5100e9c3fe) <br>
Sintaks TestModel.php: 
```
<?php

namespace App\Models;

use CodeIgniter\Model;

class TestModel extends Model
{
    // ...
}
```
   
7. **Views** <br>
View adalah bagian dari aplikasi yang menangani tampilan atau antarmuka pengguna. Tampilan berfungsi untuk menampilkan informasi kepada pengguna dan menerima input dari mereka.
Dalam CodeIgniter, tampilan biasanya berupa file-template yang berisi markup HTML atau bahasa template lainnya yang memungkinkan penggunaan variabel dan logika sederhana
untuk membangun tampilan yang dinamis. Untuk membuat views pada codeigniter4 ini dapat dibuat pada direktori _**app > Views**_ lalu buat views sesuai yang anda inginkan.
Pada contoh kali ini saya membuat model Test.php. Berikut contoh output dari test.php. <br>
![image](https://github.com/chintafitriana/chintafitriana/assets/118662112/b5604adb-3c82-46cf-a62b-4faece4eae52)

9. **Controller**<br>
Controller bertindak sebagai penghubung antara Model dan View. Controller mengelola logika aplikasi, menerima input dari pengguna melalui permintaan HTTP, dan memberikan respons yang sesuai.
Controller digunakan untuk memproses permintaan, berinteraksi dengan Model untuk mengambil atau memanipulasi data, dan memilih tampilan yang akan ditampilkan kepada pengguna.
Untuk membuat controller pada codeigniter4 ini dapat dibuat pada direktori _**app > Controllers**_ lalu buat controller sesuai yang anda inginkan. Pada contoh kali ini saya membuat controller _**Test.php.**_ <br>
Sintaks controller:
```
<?php

namespace App\Controllers;

use CodeIgniter\HTTP\RequestInterface;
use CodeIgniter\HTTP\ResponseInterface;
use Psr\Log\LoggerInterface;

class Test extends BaseController
{
    public function test()
    {
        return view('test'); // Menggunakan "return" daripada "echo"
    }
}
```
Fungsi dari _**return view('test');**_ adalah untuk menampilkan halaman test.php yang ada pada direktori **app / view** 
yang berisi tulisan _Ini contoh hasil routing_ dari sintaks test.php berikut: <br>
```
<div class="container">
    <div class="row">
        <div class="col-md-12">
            <p>Ini contoh hasil routing</p>
        </div>
    </div>
</div>
```

9. **Database Migration** <br>
Migrasi database adalah perpindahan database dari suatu tempat ke tempat yang lain. Cara ini efektif apabila ingin berganti server.
Misalnya PT 1 dengan PT 2 akan melakukan perpindahan lokasi penyimpanan data pada server yang digunakan, maka cara ini akan membantu anda dalam melakukannya.
Berikut langkah-langkah migrasi database: <br>
- 
- 
Selain menggunakan cara **_Migrasi Database_**, anda dapat melakukannya secara manual pada database anda dengan cara export database pada server lama anda
lalu import database pada server baru anda. Cara ini tergolong cukup ribet karena apabila ada banyak database tidak akan maksimmal dalam melakukannya dan tidak efisien karena terlalu lama.

11. **Membuat CRUD (Model)**























