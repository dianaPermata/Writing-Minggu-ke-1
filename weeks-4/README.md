# Writing-Weeks-4

## **Asyncronous**

- ### Async-await 
  <div align="justify">Selain menggunakan callback dan promise, kita juga bisa menggunakan async/await untuk menggunakan asynchronous pada JavaScript. Async/await baru ada ketika update ES8  JavaScript dan dibangun menggunakan promise. Jadi sebenarnya async/await dan promise itu sama saja, namun hanya berbeda dari syntax dan cara penggunaannya. Ada 2 kata kunci yang memiliki pengertian sebagai berikut:

    - async, mengubah function synchronous menjadi asynchronous.
    - await, menunda eksekusi hingga proses asynchronous selesai.
   <div align= "justify">Sebuah async function bisa tidak berisi await sama sekali atau lebih dari satu await. Keyword await hanya bisa digunakan didalam async function, jika digunakan di luar async function maka akan terjadi error

    <div align="justify">Contoh asnyc-await 

            async function asyncNonton() {
                try {
                let result = await nonton("jalan")
                console.log(result);
             } catch (error) {
                console.log(error)
               }
             }

            asyncNonton()

- ### Fetch 
  <div align="justify"> Dalam JavaScript kita bisa mengirimkan network request dan juga bisa mengambil informasi data terbaru dari server jika dibutuhkan. Contoh network request yang biasa kita lakukan:

    - Mengirimkan data dari sebuah form.
    - Mengambil data untuk ditampilkan dalam list/table.
    - Mendapatkan notifikasi.
  <div align="justify">Dalam melakukan network request, JavaScript memiliki metode bernamafetch().Proses melakukan fetch() adalah salah satu proses asynchronous di JavaScript sehingga kita perlu menggunakan salah satu diantara promise atau async/await.
  <div align = "justify"> Berikut ini contoh request data dengan fetch() menggunakan promise:

        fetch("https://digimon-api.vercel.app/api/digimon")
        .then(result => result.json())
        .then(result => {
        console.log(result)
        })

    
## **Git dan Github Lanjutan**

  - ### Apa itu git dan github ???
     - Git
        <div align="justify"> adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file. biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.

     - Github
        <div align="justify"> adalah sebuah layanan cloud yang bisa membantu para pengguna untuk menyimpan,mengelola dan mengembangkan. Didalam github kita bisa mengupload file,membuat file yang mana filenya bisa kita kelola dengan version control system punya github.
  - ### Cara Kolaborasi di github 
    - Team leader membuat repo untuk project yg akan di buat di organization.
    - Repo dibuat public, dan ceklis README.
    - Buat branch bernama dev.
    - Invite anggota tim dan jadikan owner.
    - Masing-masing anggota lakukan git clone pada repo yg sudah dibuat.
    - Bagi tugas pada masing-masing anggota kelompok.
    - Pindah ke branch dev git switch dev untuk melakukan development. 
    - Sebelum ngoding, lakukan git pull pada branch dev untuk update kode terbaru.
    - Anggota membuat branch dari dev git branch [nama-branch].
    - Pindah ke dalam branch yg sudah dibuat git switch [nama-branch].
    - Lakukan pengerjaan di dlm branch tersebut.
    - Jika fitur sudah selesai, sebelum di push lakukan langkah no 3, 4, dan 6.
    - Lalu git merge dev untuk menghindari conflict di github.
    - Jika ada conflict, selesaikan semuanya.
    - Jika sudah aman, commit lalu git push origin [nama-branch].
    - Lakukan pull request untuk merge ke branch dev.
    - Tunggu pull request di acc oleh team lead.
    - Jika sudah, ulangi proses dari no 2.
    - Setiap ada pull request, leader akan mengeceknya.
    - Jika pull request belum sesuai, bisa dikasih komen atau beri kabar anggota yg melakukan pull request tersebut.
    - Jika sudah sesuai, lakukan merge. 


## **Responsive Website**
- Responsive Web Design (RWD) bertujuan untuk membuat website kita dapat diakses dalam device apapun.
- Ada beberapa teknik dalam menjadikan website responsive : 
  - Menambahkan viewport pada file html. 
  - Menggunakan Max-width element
  - Menggunakan media query. Pada media query menggunakan dua cara yakni min-width dan max-width. Media query ini, membuat beberapa styles yang tergantung pada jenis device. contoh syntax :
  
        @media only screen and (orientation: landscape) {
          body {
            background-color: lightblue;
          }
        }

- Breakpoint adalah perubahan yang terjadi pada tampilan saat berganti device atau ukuran width. 

## **Boostrap**

- Boostrap adalah Bootstrap adalah framework HTML, CSS, dan JavaScript yang berfungsi untuk mendesain website responsive dengan cepat dan mudah. 
- Beberapa layout pada boostrap
  - Breakpoint
    <div align="justify">breakpoint sebagai acuan untuk menyesuaikan tampilan dalam berbagai ukuran viewport. Misalkan pada ukuran desktop, content dipaparkan secara horizontal ke kanan, sedangkan pada ukuran mobile phone, content dipaparkan secara vertical ke bawah.Dalam bootstrap terdapat beberapa breakpoint, yaitu:

    - sm
    - md
    - lg
    - xl
    - xxl  
  - Container adalah elemen paling dasar dalam layout bootstrap. Terdapat 3 macam container dalam bootstrap, yaitu:
 
    - Default container : class container memiliki sifat yang responsive dan fixed-width, yang berarti lebarnya akan berubah pada setiap breakpoint.
    - Fluid Container : Class container-fluid memiliki lebar yang sama dengan viewport.
    - Responsive container, diurutkan dari breakpoint terkecil, terdiri dari:

      - .container-sm
      - .container-md
      - .container-lg
      - .container-xl
      - .container-xxl
  - Grid 
    <div align="justify"> Grid biasanya digunakan bersama dengan container. 
    - Class row berfungsi untuk mengubah sifat dari div di dalamnya yang semula akan ditampilkan secara block, akan dapat ditampilkan secara inline. Maka dari itu div di dalamnya dapat dipaparkan secara horizontal.
    - Class col berfungsi untuk mengubah div tersebut menjadi responsif terhadap lebar viewport. Di dalam contoh terdapat tiga div dengan class col di dalam class row, maka dari itu lebar setiap col adalah lebar row dibagi tiga (jumlah div dengan class col) secara merata.
    - Grid system membagi lebar halaman menjadi 12 bagian. Sehingga apabila menggunakan class col-8, maka lebarnya akan menjadi 8/12 atau 2/3 dari lebar halaman.
- Beberapa komponen pada boostrap. 
  - Tables
  - Accordion
  - Alerts
  - Badge
  - Breadcrumb
  - Buttons
  - Button group
  - Card
  - Carousel
  - Close button
  - Collapse
  - Dropdowns
  - List group
  - Modal
  - Navbar
  - Navs & tabs
  - Dsbnya. 
  
- Beberapa content pada boostrap
  - Reboot
  - Typography
  - Images
  - Tables
  - Figures 
