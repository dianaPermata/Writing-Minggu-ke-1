# Writing-Weeks-1-Backend Bootcamp

## **Web Server & Restful API**

- ### **Webserver**
    <div align = "justify"> adalah perangkat lunak (software) dalam server yang berfungsi untuk menerima permintaan (request) berupa halaman web melalui protokol HTTP dan atau HTTPS dari klien yang lebih dikenal dengan nama browser, kemudian mengirimkan kembali (respon) hasil permintaan tersebut dalam bentuk halaman-halaman web yang pada umumnya berbentuk dokumen HTML.

  - Web server terdiri dari 2 komponen penting:
    - Hardware
        <div align="justify"> Di sisi software, web server adalah komputer yang menyimpan software web server dan file komponen situs web, (misalnya: dokumen HTML, gambar, CSS stylesheet, dan file JavaScript). Web server terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web.
    - Software
        <div align="justify"> Di sisi software, web server mencakup beberapa bagian yang mengontrol bagaimana pengguna web mengakses file yang dihosting. Minimal adalah server HTTP. Server HTTP adalah perangkat lunak yang memahami URL (alamat web) dan HTTP (protokol yang digunakan browser untuk melihat halaman web). Server HTTP dapat diakses melalui nama domain situs web yang disimpannya, dan mengirimkan konten situs web yang dihosting ini ke perangkat pengguna akhir. 
  - Static site adalah Diagram yang menunjukkan arsitektur web server dasar untuk static site (static side adalah site yang mengembalikan konten hard-coded yang sama dari server setiap kali sumber daya tertentu diminta). Saat pengguna ingin menavigasi ke halaman, browser mengirimkan permintaan "GET" HTTP yang menentukan URL-nya.
  - Client side adalah sistem yang berjalan di web browser pengguna.
  - dynamic site/server side adalah site di mana beberapa konten respons dihasilkan secara dinamis, hanya bila diperlukan. Di dynamic web, halaman HTML biasanya dibuat dengan memasukkan data dari database ke dalam placeholder di template HTML (ini adalah cara yang jauh lebih efisien untuk menyimpan konten dalam jumlah besar daripada menggunakan static web).
  - Software architecture
    - Monolithic adalah arsitektur dimana keseluruhan kode akan dikompilasi menjadi satu aplikasi (biasanya menjadi satu binary atau artifact) dimana aplikasi tersebut menjalankan seluruh proses yang dibutuhkan. 
    - Front-end dan back-end adalah 
    - Nicroservice adalah arsitektur yang membagi aplikasi menjadi layanan yang lebih kecil dan saling terhubung. 
- ### **REST** 
    <div align="justify"> REST adalah singkatan dari REpresentational State Transfer. REST merupakan gaya arsitektur untuk menyediakan standar antara sistem komputer di web, sehingga memudahkan sistem untuk berkomunikasi satu sama lain. Sistem yang sesuai dengan REST, sering disebut sistem RESTful, dicirikan oleh sifatnya yang stateless dan dapat memisahkan masalah klien dan server. Stateless artinya server tidak perlu mengetahui apa pun tentang status klien dan sebaliknya. Sehingga, baik server maupun klien dapat memahami pesan apa pun yang diterima, bahkan tanpa melihat pesan sebelumnya.Dalam gaya arsitektur REST, implementasi klien dan implementasi server dapat dilakukan secara independen tanpa saling mengetahui satu sama lain. 

  - HTTP method terdiri dari : 
      - GET, Mengambil dokumen dari server.
      - POST, Mengirimkan data ke server untuk diproses.
      - PUT, Menyimpan data yang ada di bagian Body ke server.
      - DELETE, Menghapus data dari server. 
   - Respons dari server berisi status code untuk memperingatkan klien tentang informasi keberhasilan operasi. Sebagai developer, tidak perlu mengetahui setiap status code (ada banyak status code), tetapi harus mengetahui kode yang paling umum dan cara penggunaannya. HTTP status code terdiri dari : 
      - Status code 2** : success
      - Status code 3** : redirect
      - Status code 4** : client error
      - Status code 5** : server error


## **Node JS**
- Definisi resmi dari situsnya menyatakan bahwa "Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js' package ecosystem, npm, is the largest ecosystem of open source libraries in the world." Node.js itu secara sederhananya, merupakan platform JavaScript yang dapat berjalan di backend atau server-side, di komputer kita secara langsung.
- Arsitektur yang digunakan Node JS, diantaranya : 
  - Single thread 
    <div align="justify"> Thread dalam ilmu komputer adalah eksekusi menjalankan beberapa tugas atau program secara bersamaan. Javascript menggunakan konsep single thread, yang berarti hanya memiliki satu tumpukan panggilan yang digunakan untuk menjalankan program. 
  - Even loop
    <div align="justify"> Event loop akan memfasilitasi kondisi ini, event loop akan memeriksa terus menerus, ketika antrian kosong di call stack maka akan menambah antrian baru dari event queue sampai semua perintah selesai di eksekusi.
  - Server side programming 
     <div align="justify"> Dengan menggunakan NodeJS kita dapat menjalankan javascript di server side menggunakan terminal command line menggunakan perintah “node”. 
- NodeJS punya beberapa Module Built-in yang bisa langsung kita pakai sesuai kebutuhan aplikasi NodeJS kita, diantaranya : 
  - Console merupakan module bawaan dari javascript yang ada di node JS untuk digunakan sebagai debug atau menampilkan code secara interface.
  - Process adalah modules yang digunakan untuk menampilkan dan mengontrol prosess Node JS yang sedang dijalankan.
  - OS module merupakan module yang digunakan untuk menyediakan informasi terkait sistem operasi komputer yang digunakan user.
  - Module Util merupakan alat bantu / utilities untuk mendukung kebutuhan internal API di Node JS.
  - Events
  - Errors merupakan modules yang dapat digunakan untuk mendefinisikan error di Node JS sehingga lebih informatif. Kita juga dapat menghandle error menggunakan try catch.
  - Buffer merupakan modules yang digunakan untuk mengakses, mengelola dan mengubah tipe data raw atau tipe data bytes.
  - Fs atau “file system” merupakan module yang dapat membantu berinteraksi dengan file yang ada diluar code. FS paling sering digunakan untuk membaca file dengan ekstensi .txt, .csv, dan .json.
  - Timers merupakan modules yang digunakan untuk melakukan scheduling atau mengatur waktu pemanggilan fungsi yang dapat diatur di waktu tertentu.
- Kita bisa mengimport module built-in tersebut, ataupun Package module yang yang kita buat sendiri nantinya dengan menggunakan require. 
- NPM atau (Node Package Manager) adalah package dan dependency manager utama pada NodeJS. NPM sudah otomatis terinstal ke komputer kita setelah kita menginstall Node JS. Untuk menjadikan projek Node kita bisa mengakses berbagai module yang ada di NPM, kita perlu menginisialisasi file package.json, sebuah file config yang akan menyimpan metadata project kita. Selain itu, kita juga bisa menggunakan External Open Source dan meng-installnya menggunakan NPM, sesuai dengan kebutuhan aplikasi kita. 
- Node.js memiliki built-in modul yang disebut HTTP, built-in modul ini memungkinkan Node JS mentransfer data melalui Hyper Text Transfer Protocol (HTTP). Modul HTTP dapat membuat server HTTP yang mendengarkan port server dan memberikan respons kembali ke klien.
- Menambahkan HTTP header yaitu 
  - Dengan menggunakan method res.writeHead() untuk menambahkan header HTTP.
  - Argumen pertama dari method res.writeHead() adalah status code, 200 berarti semuanya OK. 
  - Argumen kedua adalah objek yang berisi header respons. Respons yang dikembalikan dari HTTP web server bisa dalam berbagai format.
  - Respons yang dikembalikan dari HTTP web server bisa dalam berbagai format.
- Cara membaca query string yaitu ketika server di jalankan, kemudian kita akses dari browser ke url : http://localhost:8080/skilvul maka akan tampil tulisan skilvul.


## **Express JS**
- Express adalah salah satu package NodeJS yang memungkinkan kita untuk membuat HTTP REST API ataupun aplikasi web dengan mudah. 
- Dengan Express, kita dapat membuat berbagai hal dengan lebih cepat daripada harus membuatnya secara manual:
  - Parsing Request Body from HTTP
    <div align="justify">Req.body berfungsi untuk menangkap nilai/data yang dikirimkan user dari interface / dari postman. Untuk menggunakan req.body kita harus memanggil library body-parser. Body-parser adalah library untuk menangani application/x-www-form-urlencoded (data JSON yang dikirim melalui form-html/interface).
  - Parsing Cookies
    <div align="justify">Kita dapat menggunakan middleware cookie-parser untuk mengatur cookie.
- Fitur yang ada di express ialah routing dan rendering.     
- Routing mengacu pada bagaimana endpoint sebuah website/aplikasi (URIs) merespons permintaan client. Kita menentukan rute menggunakan metode Express yang sesuai dengan metode HTTP. Misal app.get(), app.post(), app.all(), dan juga ap.use().
  - Router method, metode rute diturunkan dari salah satu metode HTTP, dan dilampirkan ke turunan express class. Ada metode perutean khusus, app.all(), yang digunakan untuk memuat fungsi middleware di jalur untuk semua metode permintaan HTTP. Misalnya, handler berikut dijalankan untuk permintaan ke rute “/secret” apakah menggunakan GET, POST, PUT, DELETE, atau metode permintaan HTTP lainnya yang didukung dalam modul http.
  - Router path, alur rute, dalam kombinasi dengan metode permintaan, menentukan titik akhir di mana permintaan dapat dibuat. Jalur rute dapat berupa string, pola string, atau ekspresi reguler. Karakter ?, +, *, dan () adalah himpunan bagian dari pasangan ekspresi regulernya. Tanda hubung (-) dan titik (.) ditafsirkan secara harfiah oleh jalur berbasis string.
  - Router parameter, diberi nama segmen URL yang digunakan untuk menangkap nilai yang ditentukan pada posisinya di URL. Nilai yang ditangkap diisi di objek req.params, dengan nama parameter rute yang ditentukan di jalur sebagai kuncinya masing-masing.
  - Router handler, Kita bisa menyediakan beberapa callback function seperti halnya middleware untuk menghandle request. Dengan memberikan callback next(), untuk melanjutkan ke callback yang selanjutnya.
  - Chaining route, Dengan menggunakan app.route() dengan catatan memiliki path yang sama “/example”, kita bisa menggunakannya dengan method yang berbeda-beda.
- **Express Rendering**
  <div align="justify"> Express JS dapat merender menggunakan file HTML dengan fungsi yang disediakan yaitu sendFile(), yang pada dasarnya akan mengirim file HTML ke browser yang kemudian secara otomatis dipresentasikan oleh browser. 
- **Middleware** 
  <div align="justify"> adalah perangkat lunak yang berada di antara sistem operasi dan aplikasi yang berjalan di dalamnya. Pada dasarnya, middleware berfungsi sebagai lapisan terjemahan tersembunyi yang memungkinkan komunikasi dan manajemen data untuk aplikasi yang terdistribusi. Terkadang middleware disebut sebagai plumbing, karena menghubungkan dua aplikasi secara bersamaan sehingga data dan database dapat dengan mudah dilewatkan di antara “pipa.” Menggunakan middleware memungkinkan pengguna untuk membuat permintaan seperti mengirimkan formulir di browser web, atau mengizinkan server web untuk mengembalikan halaman web dinamis berdasarkan profil pengguna.Contoh middleware yang umum mencakup middleware database, middleware server aplikasi, middleware berorientasi pesan, middleware web, dan monitor pemrosesan transaksi. Setiap program biasanya menyediakan layanan olahpesan sehingga aplikasi yang berbeda dapat berkomunikasi menggunakan kerangka kerja olahpesan seperti protokol akses objek sederhana (SOAP), layanan web, REST, dan JavaScript Object Notation (JSON)



## **Design Database**

- **Desain database** adalah organisasi data menurut model database. Perancang menentukan data apa yang harus disimpan dan bagaimana elemen data saling berhubungan.
- **Entity-relationship** terbagi mejdai dua yaitu, **Entity-Relationship Model (ERM)** merupakan abstrak dan konseptual representasi data. Kemudian, **Entity-relationship diagram (ERD)** merupakan sebuah model untuk menyusun database agar dapat menggambarkan data yang mempunyai relasi dengan database yang akan didesain.
-  Komponen entity-relationship : 
   -  **Entitas**, kumpulan objek yang dapat diidentifikasikan secara unik atau saling berbeda. Biasanya, simbol dari entitas adalah persegi panjang.
   -  **Atribut**, setiap entitas pasti mempunyai elemen yang disebut atribut yang berfungsi untuk mendeskripsikan karakteristik dari entitas tersebut.
   -  **Relasi**, hubungan antara sejumlah entitas yang berasal dari himpunan entitas yang berbeda. Jenis Relasi terdiri dari : 
      - One-To-One adalah hanya satu dari masing- masing entity yang saling berhubungan atau berelasi.  
      - One To Manny adalah dimana satu attribute dari satu entity bisa berhubungan dengan dua atau lebih attribute dari entity yang lain.
      - Many To Many adalah suatu relasi dimana satu attribute dari satu entity dapat memiliki hubungan dengan dua atau lebih attribute dari entity yang lain, begitupun dengan sebaliknya.
-  **Normalisasi database** adalah teknik untuk mengorganisir data ke dalam bentuk table, supaya data tidak redudant, mudah dicari dan tidak terjadi anomali. 
-  Proses normalisasi database terbagi menjadi 3 yakni : 
   - 1NF (First Normal Form) adalah sebuah model data dikatakan memenuhi bentuk normal pertama apabila setiap atribut yangdimilikinya memiliki satu dan hanya satu nilai. Apabila ada atribut yang memiliki nilai lebih.
   - 2NF (Second Normal Form) adalah sebuah model data dikatakan memenuhi bentuk normal kedua apabila ia memenuhi bentuknormal pertama dan setiap atribut non-identifier sebuah entitas bergantung sepenuhnya hanya pada semua identifier entitas tersebut.
   - 3NF (Third Normal Form) adalah Sebuah model data dikatakan memenuhi bentuk normal ketiga apabila ia memenuhi bentuknormal kedua dan tidak ada satupun atribut non-identifying (bukan pengidentifikasi unik) yang bergantung pada atribut non-identifying lain. Apabila ada, pisahkan salah satu atribut tersebut menjadi entitas baru, dan atribut yang bergantung padanya menjadi atribut entitas baru tersebut. 
