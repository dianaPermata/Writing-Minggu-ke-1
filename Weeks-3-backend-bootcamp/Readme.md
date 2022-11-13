# Writing-Weeks-2-Backend Bootcamp

## **Sequelize**

- **Sequelize** adalah node.js promise-based ORM (Object Relational Mapping) untuk Postgre, MySQL, MariaDB, SQLite, Microsoft SQL Server dan databse lainnya. Dengan memanfaatkan ORM, Anda dapat membuat aplikasi dengan mudah tanpa menuliskan perintah SQL (Structured Query Language).
- Cara Pengunaan sequelize
  - Sebelumnya menginstall  sequeze cli  terlebih dahulu melalui terminal untuk menggenerate sequelize. 
   
            npm i -g sequelize-cli
   
   - Selanjutnyaa install sequelize di folder project.
     
            npm i sequelize

   - Melakukan initialisasi sequelize, kemudiam secara otomatis akan membuat folder yang terdiri dari config, models, migrations, dan seeders. 

            npx sequelize-cli init
   - Database yang kita gunakan adalah MySQL, untuk menjalankan mysql, sequelize membutuhkan library tambahan yaitu mysql2. Install dengan cara berikut 

            npm i mysql2

   - Buat database Mysql lalu konfigurasi database dengan membuka file config.json dan sesuaikan dengan MySql yang digunakan. 
   - Setelah database dibuat, pindah ke terminal untuk membuat Model. Kemudian akan menghasilkan file javascript pada folder models. 

            npx sequelize-cli model:generate --name User --attributes name:string,label:string,picture:string,email:string,phone:string,website:string,summary:string

   - Untuk mengubah file model ke tabel pada database maka lakukan migrate db dengan perintah berikut.

             npx sequelize-cli db:migrate


 
   - Setelah data berhasil dibuat dan disimpan oleh database, kita dapat meng-undo dengan perintah berikut ini : 

            npx sequelize-cli: db:migrate:undo
            npx sequelize-cli: db:migrate:undo-all
            npx sequelize-cli: db:migrate:undo-all --to 'nama file' 

      Kita bisa mengembalikan ke posisi awal dengan menggunakan undo-all,Dan juga mengembalikan ke posisi sesuai spesifikasi dengan menambahkan --to “nama file”. 
  - Melakukan  generate seed
  
              npx sequelize-cli seed:generate --name demo-todo

  - Setelah generate maka kita dapat melakukan pengisian data seed didalam file seed generator. Terdapat 2 data yang diisi yaitu “up” untuk mengisi data di db, dan “down” untuk drop atau menghapus semua data seed di db. 
  - Kemudian menjalankan generate seed menggunakan sequelize.

             npx sequelize-cli db:seed:all


- Simple CRUD 
  - findAll() berfungsi untuk mencari banyak data dalam database, jika panggil tanpa parameter maka akan mengambil semua data.
  - findOne() berfungsi untuk mencari satu spesifik data dengan kriteria pada parameter.
  - create() berfungsi untuk membuat data baru pada database.
  - update() berfungsi untuk melakukan pengubahan data.
  - destroy() berfungsi untuk menghapus data.
  
  
## **MongoDB**

- MongoDB adalah salah satu jenis database NoSQL berbasis dokumen dengan menggunakan format file berupa JSON (JavaScript Object Notation).
- MongoDB sering dipakai untuk aplikasi berbasis cloud, Big Data, maupun Grid Computing. 
- Komponen database mongoDB : 
  - Database adalah wadah untuk menyimpan berbagai macam collection.
  - Collection adalah tempat kumpulan dari berbagai macam document/data.
  - Document adalah unit terkecil yang berada pada mongoDB. Document dapat dianggap sebagai data. 
-  Operasi CRUD MongoDB 
   - Untuk melihat daftar database bisa menggunakan perintah "show dbs". 
    - Untuk membuat database baru menggunakan "use nama database". 
    - Untuk menambahkan collection baru dengan menggunakan perintah "db.createCollections("artis")". 
    - Untuk Menambahkan data pada collection, dapat menggunakan "db.nama collection.insert({ nama : "thor", genre : "action" })". 
    - Untuk melihat datanya dengan menggunakan perintah "db.nama collection.find()".
    - Untuk mengupdate datanya yaitu dengan perintah "db.nama collection.update({'attribute':'data yang akan diubah'}, $set:{'attribute' :'data untuk mengubah'})".
    - Untuk menghapus sebuah data pada collection, yaitu dengan "db:nama collection.remove({'attribute':'data yang akan dihapus'})" . 
-  Dalam mendesain MongoDB kita ada 2 pendekatan yaitu Embedding dan Referencing : 
   - Embedding adalah Pendekatan yang menggabungkan data yang berhubungan ke dalam struktur atau document tunggal.
   - Referencing adalah Model data yang ternormalisasi menjelaskan hubungan yang menggunakan reference antar document. 
- Relasi dalam MongoDB
   - One-To-One adalah hanya satu dari masing- masing entity yang saling berhubungan atau berelasi.  
    - One To Manny adalah dimana satu attribute dari satu entity bisa berhubungan dengan dua atau lebih attribute dari entity yang lain.
    - Many To Many adalah suatu relasi dimana satu attribute dari satu entity dapat memiliki hubungan dengan dua atau lebih attribute dari entity yang lain, begitupun dengan sebaliknya.


## **Mongoose**

- Mongoose adalah sebuah module pada NodeJS yang di install menggunakan npm, berfungsi sebagai penghubung antara NodeJS dan database nosql MongoDB.
- Mongoose bisa digunakan untuk mengelola hubungan antara data, menyediakan validasi. Selain itu juga digunakan untuk menerjemahkan antara objek dalam kode dan representasi objek di MongoDB.
- Install mongoose dengan perintah "npm install mongoose" .
- Membuat koneksi dengan menggunakan MongoDB database dengan perintah "mongoose.connect('mongodb://localhost:27017/myapp');"
- Mendefining schema
      
            const { Schema } = mongoose;

            const blogSchema = new Schema({
                title:  String, // String is shorthand for      {type: String}
                author: String,
                body:   String,
                comments: [{ body: String, date: Date }],
                date: { type: Date, default: Date.now },
                hidden: Boolean,
                meta: {
                  votes: Number,
                  favs:  Number
                }
              });
    Untuk menggunakan model users dari schema yang telah buat untuk melakukan pengolahan data, atau operasi CRUD.

- Simple CRUD
  - Untuk menampilkan keseluruhan data (READ) kita bisa menggunakan fungsi find().
  - Saat menggunakan method POST untuk mendaftarkan user, sebelum mendaftarkan dicek dulu apakah user sudah ada atau belum dengan menggunakan findOne(), jika sudah ada akan muncul pesan error, jika belum terdaftar maka user akan didaftarkan menggunakan fungsi create(). 
  - Untuk mendapatkan data user berdasarkan id, dengan fungsi findById().
  - Untuk menghapus satu data berdasarkan ID dengan menggunakan deleteOne(). 
  - Untuk mengedit/update satu data berdasarkan ID dengan menggunakan findByIdAndUpdate().
- Populate adalah proses penggabungan 2 collection atau lebih menjadi satu objek JSON. Populate berkaitannya dengan relasi database. 

## **Docker**

- Docker adalah software yang menjalankan suatu aplikasi menggunakan container. 
- Docker men-sharing kernel dari host OS, serta meng-container-kan suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja .
- Docker berfungsi sebagai penyedia layanan virtual bagi aplikasi yg diinstall pada sebuah host. Docker akan menyediakan hal-hal yang diperlukan untuk aplikasi mulai dari akses file, koneksi internet, hingga port agar aplikasi dapat berjalan dengan baik. 
- Perbedaan VM dan container 
  <div align item="justify"> VM memakan banyak resource dan waktu utk booting karena melakukan virtualisasi pada host hardware-nya. Sedangkan container kebalikannya dari vm, container melakukan virtualisasi pada host OS-nya. 
- Perintah dasar docker 
  - Docker pull, donwload image dari docker hub.
  - Docker image, untuk melihat kumpulan images yang sudah ter download.
  - Docker run, untuk menjalankan container.
  - Docker ps, untuk melihat container yang berjalan.
  - Docker file merupakan sebuah blueprint untuk  membuat image, juga bisa membuat custom image menggunakan docker file.
  - Docker compose, untuk menjalankan lebih dari 1 container secara bersamaan dan saling terhubung.


