# Writing-Weeks-3

## **Array & Multidemensional**

- ### Array
   <div align="justify"> Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.
    - Array didefinisikan menggunakan square brackets
    - Cara mengakses/memanggil array dengan memanggil index ke berapa, karena array pada javascript dihitung dari index data ke-0
    - Array datanya juga dapat diupdate, contohnya :

      
        let hewan = ["kucing", "kelinci", "jerapah", "harimau"];

        hewan[1] = "singa";

      console.log(hewan); // output ["kucing", "singa", "jerapah", "harimau"];

    - Const in array 
        - Jika menggunakan let, kita dapat mengubah array  dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
        - Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
        - Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.
  
    - Array Properties 
        <div align="jusstify"> Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.
        - Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype. Yang saya contohkan adalah properti length, dimana properti length akan mengembalikan nilai dari jumlah panjang data suatu array. 
  
        ```    
        let hewan = ["kucing", "kelinci", "jerapah", "harimau"];

        console.log(hewan.length); // output : 4
            

    - Array method 
        <div align="justify"> Array memiliki method atau biasa disebut built-in methods. Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan.
         Contoh Array Built-in Methods. 

        - .push() adalah method untuk menambahkan item  array pada urutan yang paling akhir.
        - .shift() adalah method untuk menghapus item Array pada index pertama
        - .unshift() adalah method untuk menambahkan item Array pada index pertama
        - .sort() adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric
  
    - Looping Array
      <div align="justify"> Array memiliki built in methods untuk melakukan looping yaitu .map() melakukan perulangan/looping dengan membuat array baru  dan .forEach() melakukan looping pada setiap elemen array. 

    - Multidemensional array  
         <div align="justify"> Multidimensional Array bisa dianalogikan dengan array of array (ada array didalam array).
        - Cara akses index multidimensional array 
         
           
                let arrMulti = [
                    ["nama", "alpha"],
                    ["umur", 17],
                    ["kelas", "JS"],
                ]

                console.log(arrMulti[2][1]) // JS
            

        - Multidimensional array juga dapat menggunakan Property dan Method built-in Array.


- ### Object
    - Apa itu object ??
        <div align="justify"> object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.
    - Object dapat diassign kedalam sebuah variabel. 
    - Object juga dapat menyimpan properti dengan tipe data apapun seperti array. 
    - Cara mengakses object
    - Kita juga bisa menggunakan bracket notation saat memanggil properti dari sebuah object.
    - Kita dapat melakukan update pada variabel dengan tipe data Object.
        - Do's
            - Object dapat mengupdate value dari key yang sudah tersedia.
            - Object dapat menambahkan key dan value baru.
        - Dont's
             <div align="justify">Jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru.
    - Delete object property
        <div align="justify"> dapat menghapus properti dari object menggunakan delete operator.
    - Method adalah value yang dimasukkan pada properti berupa function. 
    - Nested Object
        <div align="justify"> Objek bersarang adalah objek yang berada di dalam objek lain.
    - Looping object
        <div align="justify"> Jika ingin menampilkan seluruh object properti. Kita bisa menggunakan looping.Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.
    - Array of object
        <div align="justify"> Object sama seperti Array yang bisa menyimpan banyak data. Array of object ini membantu menggunakan data lebih dari satu.


- ### Modules
   - Modules  adalah reusable code(data yang digunakan berulang kali) yang dapat di export dari suatu file javascript dan diimport ke file javascript yang lain.
   - Untuk bisa menghubungkan file antar JavaScript kita bisa menggunakan export dan import sehingga memungkinkan untuk saling menggunakan kode antar module.
   - Export digunakan untuk meng-export variabel pada file JavaScript. Variabel yang di_export_ dapat berisi data seperti string, object, array, hingga function. Hal ini dilakukan agar file JavaScript tersebut dapat dijadikan sebuah module, sehingga variabel yang telah di-export dapat digunakan pada file JavaScript lain dengan menggunakan import.
   - Import diibaratkan sebagai pasangan dari export. Jadi import digunakan untuk menggunakan variabel yang sudah di-export dari module lainnya.
   - Export as digunakan untuk mengganti nama darifunction, variabel, dan data. 
   -  import as digunakan untuk mengubah langsung nama data yang kita import. 
   - Export default digunakan jika hanya 1 data yang ingin kita export. Biasanya digunkan jika hanya ada 1 data atau export single class component.


- ### Recursive 
   - Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive biasanya digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.
        ```
            function recursive() {
                // ....
                recursive();
                // .....
            }
        ```

   - Ciri - ciri rekursif
       - Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
       - Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

- ### Asynchronous
    - Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous. Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung.
    - Cara membuat asynchronous secara simulasi artinya tidak murni asynchronous dengan beberapa cara:
        - Callback  function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.
        - Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API. Dalam pengambilan data, promise memiliki 3 kemungkinan state yaitu Pending(sedang dalam proses, Fulfilled (berhasil), Rejected (gagal).
        - Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.
    - Proses asynchronous identik dengan delay, dimana hasil dari proses tersebut membutuhkan selang waktu tertentu untuk menghasilkan output. Kita akan menemukan proses asynchronous pada proses Ajax, komunikasi HTTP, Operasi file, timer, dsb.
    - setTimeout digunakan untuk simulasi asynchronous. Karena sebenarnya kita tidak bisa membuat proses asynchronous murni.
    - HTTP Request fetch() adalah native web API untuk melakukan HTTP calls dari external network. fetch() memiliki parameter utama yaitu URL/endpoint API, dan parameter kedua yaitu options, options ini berisi method, headers dan body. Tergantung keinginan kita.
    
    
- ### Web Storage 
    - Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB).
    - Web storage dapat menampung sebesar 10MB untuk satu domain.Tipe Web StorageWeb API menyediakan dua tipe Web Storage untuk kita gunakan, yakni sessionStorage dan localStorage.
    - Local Storage adalah data yang disimpan tidak memiliki waktu expired window.
        - Untuk menyimpan data pada local storage, kita menggunakan method setItem() yang membutuhkan 2 parameter. Parameter pertama adalah key yang ingin kita simpan dan parameter kedua adalah data (value) dari key yang akan disimpan.
        - Untuk mengambil data yang telah tersimpan pada local storage, kita dapat menggunakan method getItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang kita inginkan.
        - Untuk menghapus data yang telah tersimpan pada local storage, kita dapat menggunakan method removeItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang ingin kita hapus.
         
    -  Session Storage adalah data yang disimpan akan hilang jika browes ditutup Pada dasarnya untuk menggunakan localStorage dan sessionStorage sama, terlebih dahulu kita harus mengatur key dan value nya.
        -  Sama seperti local storage, cara mendapatkan data dari session storage juga menggunakan getItem().
        -  untuk menghapus data dari session storage ada 2, yaitu: menghapus session storage satu persatu berdasarkan key dengan removeItem() dan menghapus seluruh session storage sekaligus dengan clear().
  
