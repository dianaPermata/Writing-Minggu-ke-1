# Writing-Minggu-ke-1
## **Unix Command Line Interface**

- #### **Command line interface** 
   <div align="justify">merupakan shell berbasis teks yang digunakan untuk menjalankan program, mengelola file komputer, dan berinteraksi dengan komputer. 
- #### **Shell** 
  <div align="justify">adalah  program yang menerima perintah, kemudian meneruskan perintah tersebut ke system untuk dieksekusi. 
- #### Aplikasi yang digunakan untuk mengakses CLI adalah **Terminal emulator**. 

- #### **File system structure** 
  <div align="justify"> adalah struktur yang mengatur bagaimana data disimpan di dalam sebuah system. Dalam menyusun file dan direktori pada sistem operasi Windows dan user menggunakan struktur yang bentuknya mirip tree atau disebut dengan file system tree. 
 ![Picture1](https://user-images.githubusercontent.com/113364526/191979262-6a8b991d-2e25-4503-b6cb-374249390a3d.png)

- #### **Command untuk navigasi** :
   - Pwd (print working directory) : untuk melihat current working directory (keberadaan saat ini).
   - Ls (list) : untuk melihat isi file yang ada disebuah direktori.
   - Cd (Change Directory) : untuk berpindah direktori lain

- #### **Manipulasi file dan directory** : 
   - Touch : untuk membuat sebuah file.
   - Mkdir : untuk membuat sebuah direktori.
   - Head : untuk melihat beberapa line awal dari sebuah file text.
   - Tail : untuk melihat beberapa line awal dari sebuah file text. 
   - Cat : untuk melihat isi sebuah file.
   - Cp : mencopy file atau cp-R directory.
   - Mv : untuk memindahkan file atau mv-R directory. Selain itu juga dapat digunakan untuk rename.
   - Rm : untuk menghapus file yang terdiri dari beberapa command yakni : Rm-R (hapus file) & Rm-d (hapus direktori).

   
## **Git & Github**
- #### Apa itu git dan github ???
   - Git
     <div align="justify"> adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file. biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.
   - Github
     <div align="justify"> adalah sebuah layanan cloud yang bisa membantu para pengguna untuk menyimpan,mengelola dan mengembangkan. Didalam github kita bisa mengupload file,membuat file yang mana filenya bisa kita kelola dengan version control system punya github.
      
- #### Pentingnya menggunakan git & github
  <div align="justify"> Dengan menggunakan Git dann Github, kita bisa berkolaborasi mengerjakan proyek yang sama dengan orang lain tanpa harus repot  copy paste folder aplikasi yang terupdate. Selain itu juga, kita tidak perlu menunggu rekan dalam satu tim menyelesaikan program dahulu untuk berkolaborasi. Kita juga bisa membuat file di dalam proyek yang sama atau membuat code di file yang sama dan menyatukannya saat sudah selesai.
   
 - #### Contoh Alur kerja dari git & github 
   - Membuat repository baru dengan menggunakan git init. jika folder sudah ada sebelumnya menggunakan.....
   - Memeriksa kondisi file dengan menggunakan git status. 
   - Setelah cek status dengan ‘git status’, selanjutnya kita ubah status ‘untrackted file’ dan ‘unmodified’ menjadi modified. Tapi gimana kalau untracked file nya dalam jumlah besar. menampilkan daftar commits yang ada di branch beserta detail-nya.
   - Lakukan ‘git commit’ untuk save perubahan pada version control.Dan kita bisa menambahkan pesan untuk membeikan checkout pada setiap perbuahan. contohnya "git commit -m "pesan checkout".
   - Setelah itu mempublish file ke github dengan melakukan git remote untuk menghubungkan repository lokal ke remote server. 
   - selanjutnya, lakukan git push origin  untuk mempublish file ke github. 
   
- #### Cara cloning github ke local : 
   -
   -
   -

   
## **HTML**
- #### HTML(Hypertext Markup Language) 
   <div align="justify">adalah bahasa komputer yang digunakan untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet. HTML berperan dalam menampilkan konten pada browser dengan menggunakan tag html.
   
- #### Tools utama yang harus dipersiapkan untuk membuat HTML :
   -  Browser
   -  Code editor
   
- #### Dasar - dasar HTML 
   
    - Kita bisa menuliskan HTML tanpa structure dan kita bisa tetap menjalankan nya tetapi untuk menjalankannya dengan baik kita perlu HTML Structure. HTML structure atau yang disebut dengan kerangka HTML seperti di bawah ini : 
Dalam kerangka HTML terdapat ```<!DOCTYPE>``` syntax mendefinisikan versi dari HTML yang digunakan dan harus dideklarasi sebelum tag ```<html>``` dan 3 tag utama, yaitu ```<html>,<head>, dan <body>``` : 
       - ```<html></html>``` adalah root element dari halaman HTML. Semua HTML tag lainnya harus dibungkus dengan tag ini.
       - ```<head></head>``` berisi ```<meta>, <title>```, konten css/js internal maupun link ke file css/js eksternal. 
       - ```<body></body>```berisi konten website yang ingin ditampilkan pada browser.
   
    - **HTML Element** merupakan sebuah komponen dalam halaman web, bisa berupa paragraf, judul, atau gambar. struktur dari HTML elemen seperti di bawah ini : 
       ```
          <!DOCTYPE html>
          <html lang="en">
          <head>
               <meta charset="UTF-8">
               <meta http-equiv="X-UA-Compatible" content="IE=edge">
               <meta name="viewport" content="width=device-width, initial- scale=1.0">
               <title>Document</title>
           </head>
           <body>
           
           </body>
           </html>
         Pada source code di atas HTML elemen terdiri dari : 
           - Opening tag (tag pembuka)
           - Closing tag (tag penutup)
           - Attribute 
           - Konten
   
   - Selain HTML elemen, juga terdapat empty HTML element dimana memiliki Self-closing Tag, yang hanya memiliki Opening Tag (tag pembuka) dengan garis miring sebelum kurung tutup. Contohnya adalah ``` <br /> atau <img />. ```
   
   - Salah satu contoh tag HTML
      - Tag untuk membuat tulisan tebal dan miring
        ``` html
        <b>Hello world</b> & <i>Hello World<i>
        ```
      - Tag untuk menuliskan link
        ``` html
        <a href="https://www.google.co.id/">Google</a>
        ```
      - Tag untuk membuat daftar/list
          - Ordered list 
             ```html
             <ol>
                <li>Hello World</li>
                <li>Hello World</li>
                <li>Hello World</li>
              </ol>
             ```
           - Unordered list
             ```html
             <ul>
                <li>Hello World</li>
                <li>Hello World</li>
                <li>Hello World</li>
              </ul>
             ```
       - Tag untuk menampilkan gambar/image. 
           ```html
           <img src="https://www.google.co.id/url?sa=i&url=https%3A%2F%2Fid.wikipedia.org%2Fwiki%2FKucing_persia&psig=AOvVaw0WbxrJ_HmSXMIEbrTkLlWy&ust=1664119855387000&source=images&cd=vfe&ved=0CAwQjRxqFwoTCLid59uor_oCFQAAAAAdAAAAABAD" alt="Si Kucing"></img>
           ```
   
  - Dalam HTML terdapat beberapa elemen semantik yang dapat digunakan untuk mendefinisikan berbagai bagian halaman web, salah satunya yaitu : 
      - ``` <section>``` : untuk mempresentasikan bagian - bagian dokumen atau aplikasi seperti mengelompokkan konten/dokumen menjadi beberapa bagian seksi berdasarkan tema dan tata letak masing - masing. 
      - ```<header>``` : element yang merepresentasikan konten pengantar, pembukaan atau navigasi yang terdiri dari deretan link. Dalam penggunaannya, ```<header>``` element berisi element heading (h1 - h6) tapi tidak diperlukan, daftar isi (table of contents), logo, form pencarian dll. 
      - ```<article>``` : digunakan untuk memberi mark up sebuah independent content, artinya element itu dapat berdiri sendiri sebagai sebuah konten utuh yang tidak terikat dengan konten lain (element lain).
      - ```<nav>``` : untuk mempresentasikan link navigasi. 
    
  - Setelah kita selesai membuat suatu website pastinya kita ingin website yang dibuat digunakan oleh banyak orang. Dengan begitu, proses untuk menyebarkan website dijangkau oleh orang - orang yaitu dengan mendeploy website ke server dengan menggunakan salah satu layanan yaitu netlify. 

   
## **CSS**
  
   
   
## **Algoritma**
- **Algoritma** adalah urutan logis untuk memecahkan masalah secara logis dan sistematis. Dengan kata lain, dalam kehidupan sehari - hari kita sudah menerapkan algoritma untuk memecahkan suatu masalah. 

- **Manfaat algoritma** : 
1. Membantu menyederhanakan suatu program yang rumit dan juga besar.
2. Mempermudah pembuatan program yang dapat menyelesaikan masalah tertentu.
3. Membantu menyelesaikan suatu masalah dengan logika dan juga sistematis.
   
- **Contoh algoritma sederhana** :
    Perhitungan Luas Persegi Panjang
1. Masukkan panjang 
2. Masukkan lebar
3. Luas persegi panjang adalah panjang * lebar
4. Tampilkan luas persegi panjang 
   
- **Penerapan algoritma luas persegi panjang ke dalam bahasa pemrograman C++**

```
#include <iostream>
  using namespace std;
  int main (){
  int p, l;
  cout<<"Masukkan panjang = ";
  cin>>p;
  cout<<"Masukkan lebar= ";
  cin>>l;
  cout<<"Luas Persegi panjang = "; cout<<(p*l)
  }
  ```

- **Penerapan algoritma urutan bilangan genap sampai 10 ke dalam bahasa pemrograman javascript**

 ```
let i= 1;

for ( i=1; i<10; i++) {
    if(i%2==0){
    console.log(i);
    }
}
 ```
 

