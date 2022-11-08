# Writing-Weeks-2-Backend Bootcamp

## **Design Database With MYSQL**

- **Database** adalah tempat untuk menyimpan data yang terstruktur, dimana di dalamya terdapat informasi yang bersifat tersruktur. 
- Database dapat berbasis SQL (merupakan singkatan dari Structured Query Language. SQL adalah bahasa yang digunakan untuk mengatur/mengelola data dalam database relasional) dan NON-SQL(merupakan database yang tidak membutuhkan skema dan tidak memiliki relasi untuk setiap tabelnya).  
- Database dapat diakses dengan DBMS (Database Management System, yang merupakan  software yang digunakan untuk mengelola, menyimpan, dan mengambil database). 
- Di dalam database terdapat 
  - Table  adalah kumpulan value yang dibangun oleh row dan column, dimana didalamnya terdapat atrribut dari sebuah data.
  - Field (column) adalah kolom dari sebuah tabel, dimana masing - masing field memiliki tipe data masing - masing. 
  - Record adalah kumpulan nilai yang saling terkait. Record merupakan isi/ data dari sebuah table. 
- Jenis Perintah dasar SQL, diantaranya : 
  -  **DDL (Data Definition Languange)** adalah perintah yang digunakan untuk membuat database baru, mengubah dataset dan menghapus data. DDL ini, terdapat beberapa jenis perintah, yaitu 
     -  Create adalah perintah untuk membuat table, kolom dan databse baru. 
     -  Alter adalah perintah yang Alter digunakan untuk mengubah struktur dari tabel yang ada, seperti untuk menambahkan atau menghapus kolom/field. 
     - Drop adalah perintah yang digunakan untuk menghapus baik itu berupa database, table maupun kolom hingga index.
  -  **DML (Data Manipulation Language )** adalah , perintah yang digunakan untuk memanipulasi data. 
     -  Select  adalah perintah yang digunakan untuk memanipulasi data dengan tujuan menampilkan maupun mengambil sebuah data pada tabel.
     -  Insert adalah perintah yang digunakan untuk memasukkan sebuah record baru atau data baru ke dalam sebuah tabel database. 
     -  Update adalah perintah yang digunakan untuk pembaruan data di dalam sebuah tabel. 
     -  Delete adalah perintah yang digunakan untuk menghapus sebuah record yang ada di dalam sebuah table. 
  -  **DCL (Data Control Language)**
     - Grant digunakan untuk memberikan hak akses pada user.
     -  Revoke digunakan untuk mencabut hak akses yang telah diberikan pada user.
  - SQL table join  
      -  JOIN merupakan salah satu fungsi yang ada di SQL yang digunakan untuk penggabungan table melalui kolom atau key tertentu dimana memiliki nilai terkait untuk mendapatkan satu set data dengan informasi lengkap. SQL join terbagi menjadi 3, diantaranya : 
         - Inner join adalah Penggabungan antara dua tabel atau lebih ini hanya dapat dilakukan jika tabel-tabel tersebut memiliki key kolom yang sama.
         - Left join adalah menampilkan semua data sebelah kiri dari tabel yang di joinkan dan menampilkan data sebelah kanan yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis. 
         - Right join adalah menampilkan semua data sebelah kanan dari tabel yang di joinkan dan menampilkan data sebelah kiri yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis.    
- Database relationship adalah relasi atau hubungan antara beberapa tabel. Relasi antar tabel dihubungkan oleh Primary key dan foreign key. Ada beberapa tipe database relationships diantaranya : 
    - One-To-One adalah hanya satu dari masing- masing entity yang saling berhubungan atau berelasi.  
    - One To Manny adalah dimana satu attribute dari satu entity bisa berhubungan dengan dua atau lebih attribute dari entity yang lain.
    - Many To Many adalah suatu relasi dimana satu attribute dari satu entity dapat memiliki hubungan dengan dua atau lebih attribute dari entity yang lain, begitupun dengan sebaliknya.


## **Authentication & Authorization**

- **Authentication** merupakan proses untuk memastikan suatu pengenalan atau memastikan suatu pengakuan. Biasanya terjadi saat proses login. Sedangkan Sedangkan authorization adalah proses selanjutnya setelah authentication berhasil. Sistem akan memberikan akses sesuai kebijakan yang sudah ditentukan sebelumnya.
- Authorization adalah proses penentuan apakah user tersebut diijinkan / ditolak untuk melakukan satu atau beberapa action atau akses terhadap resources tertentu dalam system. User login terhadap system dengan menggunakan user-ID dan password, kemudian system mengenalinya dan user mendapatkan akses atau ditolak terhadap suatu resource system tertentu
- Perbedaan Authentication, Authorization, dan Encryption
  - Autentikasi = Data seseorang akan dicek ke - validannya dengan mencocokkan data tersebut ke sebuah basis data.
  - Authorization = Seseorang / kelompok yang telah melalui ke proses autentikasi akan diarahkan (bisa juga diberikan) sesuai dengan hak akses atau apa saja yang berhak diakses oleh seseorang tersebut.
  - Enkripsi adalah cara mengacak data sehingga informasi tersebut hanya bisa dibaca oleh orang-orang yang memiliki aksesnya saja.
  

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

      Kita bisa mengembalikan ke posisi awal dengan menggunakan undo-all,Dan juga mengembalikan ke posisi sesuai spesifikasi dengan menambahkan --to “nama file”


