# Writing-Weeks-2

## **Scope & Function**

- ### **Scope** 
  
  - <div align="justify"> Scope adalah jangkauan kode program dimana perintah program masih bisa mengakses sebuah variabel.
  - <div align="justify"> Blocks adalah code yang berada didalam curly braces {}. Blocks biasanya digunakan pada conditional, function dan looping. 
  - Scope terbagi menjadi dua, yakni : 
    1. Global scope (lingkup global) adalah sebuah variabel yang bisa diakses dari mana saja, baik di dalam maupun di luar dari suatu fungsi atau blok (grup) kode. Untuk menjadi global scope, suatu variabel harus dideklarasikan di luar blocks.
        ``` 
            Let hewan = "Kucing"; 
            function jenisHewan(){
                return hewan; // Kucing
            }

            console.log(hewan); // Kucing
        ```

    2. Local scope (lingkup lokal) adalah sebuah variabel hanya bisa diakses di dalam sebuah fungsi atau blok kode. Semua variabel yang dideklarasikan di dalam sebuah fungsi/blok hanya bisa diakses di dalam fungsi/blok tersebut saja. Tidak bisa diakses diluar blocks.  
        ```
            function Jenishewan(){}
                let hewan = "Kucing";
                return hewan; // Kucing
            }

            console.log(jenisHewan()) //kucing
            console.log(hewan); // Uncaught ReferenceError: hewan is not defined because local scope
        ```

- ### **Function**
  - <div align="justify"> Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. 
  - Function dapat berdiri sendiri atau disimpan di dalam variabel. 
    ```
        // Fungsi yang berdiri sendiri
        function namaFungsi(){
        // Kode yang akan dijalankan
        }

        // Fungsi yang disimpan di dalam variabel
        let namaVariabelFungsi = function(){
        // Kode yang akan dijalankan
        }    
    ```
   - Cara memanggil function cukup dengan menambahkan tanda kurung () setelah nama fungsi tersebut. 
        ```  
            namaFungsi();

            namaVariabelFungsi(); 
        ```
    - Parameter & Argumen
      <div align="justify"> **Parameter** adalah syarat input yang harus dimasukkan ke dalam suatu fungsi dan dideklarasikan bersama dengan deklarasi fungsi. Sementara **argument** adalah nilai yang dimasukan ke dalam suatu fungsi, sesuai dengan persyaratan parameter, di mana argument dituliskan bersamaan dengan pemanggilan fungsi.

        ```
            function luasPersegiPanjang(panjang, lebar){
            return panjang * lebar;
            }

            console.log(operasiPerkalian(10, 2)) 
        ```
        - panjang & lebar adalah parameter
        - 10 & 2 adalah argument
  
    - Default Parameter
        <div align="justify"> Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function. Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen. 

        ```
        function JenisHewan(hewan="Kucing"){
            return "Hewan ini adalah" + hewan;
        }

        console.log(JenisHewan('Kelinci')); // output : "Hewan ini adalah Kelinci"
        console.log(JenisHewan()); // output : "Hewan ini adalah Kelinci"
    - Arrow Function
        <div align="justify">Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version).

        ```
            // Arrow function
                const namaFungsi = (parameter1, ..., parameterX) => {
                // kode yang ingin dijalankan dalam fungsi
                };

            // atau bila fungsi tersebut tidak memiliki parameter sama sekali
                const namaFungsiTanpaParameter = () => {
                // kode yang ingin dijalankan dalam fungsi
                };
        ```
        <div align="justify"> Implicit Return Value adalah suatu kondisi di mana sebuah fungsi langsung mengembalikan nilai tanpa ada deklarasi variabel atau operasi lainnya di dalamnya.

        ```
            const namaFungsi = () => nilaiReturn;
        ```

    - Function Hoisting 
        <div align="justify"> Compiler JavaScript yang memindahkan definisi fungsi ke atas dengan cara yang sama seperti deklarasi variabel. Akan tetapi function hoisting ini tidak berlaku jika functionnya dideklarasikan ke dalam variabel. 
        
         ```
            console.log(operasiPerkalian(10, 2)) 
            function luasPersegiPanjang(panjang, lebar){
            return panjang * lebar;
            }
        ```
    
- ### **Error dan Debbuging**
  - Error objek dilempar ketika kesalahan runtime terjadi. Objek error juga dapat digunakan sebagai objek dasar untuk pengecualian yang ditentukan pengguna. Kesalahan runtime menghasilkan error objek baru yang dibuat dan dibuang.
  - Tipe - tipe pada error antara lain : 
    - Logical Error adalah Error jenis ini adalah sebuah error atau kesalahan yang paling sulit dideteksi dalam dunia pemrograman.
    - Syntax Error adalah sebuah kesalahan yang paling sering terjadi di dunia pemrograman.
    - Runtime error juga termasuk kedalam sebuah error atau kesalahan yang sering terjadi saat sedang menjalankan sebuah program yang dibuat programmer. Biasanya Runtime error dalam dunia pemrograman ini disebabkan oleh kesalahan dalam proses input, kesalahan perhitungan, dan kesalahan dalam proses output.
    - Compilation error ini merupakan sebuah error atau kesalahan yang terdiri dari berbagai macam error dalam dunia pemrograman. Compilation error biasanya terjadi saat proses tingkat tinggi dikonversi ke dalam bentuk yang dapat dibaca oleh mesin. 
    - Interfacing error yang bisa terjadi karena adanya ketidaksesuaian program pada sebuah software. Biasanya pada kasus-kasus tertentu, interfacing error ini terjadi karena penggunaan protokol web yang salah.
   -  Debugging pada javascript yang paling umum adalah dengan console.log() variabel yang ingin diperiksa. Terdapat 2 cara dalam debugging, yakni : 
        - Menggunakan alat pengembang chrome, buka halaman dengan kode JS dan pilih file untuk didebug, klik baris yang ingin didebug dan refresh kembali dengan F5.
        - call stack, jalur yang telah diambil program untuk mencapai titik saat menetapkan titik putus atau mengalami kesalahan. 
                

## Data type 
- #### Apa itu tipe data ? 
  <div align="justify"> Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming. 
- #### Tipe data di javascript dikelompokkan ke dalam dua kategori primitif dan non-primitif 
  a. Tipe data primitif, hanya dapat menyimpan satu nilai pada satu waktu dan tidak dapat diubah menggunakan cara yang sama seperti tipe data non-primitif. Tipe data Primitif akan dianggap sama jika nilainya sama.  Di JavaScript ada tujuh tipe data primitif 

    - String 
        - <div align="justify">  String adalah deretan karakter yang diapit oleh sepasang tanda kutip baik single quotes maupun double quotes. String dapat dibuat menggunakan petik tunggal atau ganda dan diakhiri dengan petik yang sama, kita bisa memasukkan karakter diantara petik.
        - Method String dapat membantu kita dalam memanipulasi data string, kita tidak perlu membuat fungsi untuk memanipulasi string secara manual. Jadi, method String adalah fungsi atau method yang ada di dalam objek String. Beberapa properti dan method dalam string : 
            1. toUpperCase() mengembalikan string yang dikonversi ke huruf besar.
            2. toLowerCase() mengembalikan string yang dikonversi ke huruf kecil.
            3. Split() memecah string menjadi beberapa bagian sesuai separator yang ditentukan, string yang telah dibagi akan dimasukkan ke dalam array.
            4. substring() mengambil bagian dari string sesuai dengan indeks awal dan akhir yang ditentukan.
            5. length mengembalikan tipe data angka panjang string.
            6. includes() melakukan pencarian (peka huruf besar/kecil) apakah string berisi atau mengandung karakter yang ditentukan.
            7. slice() melakukan pemotongan atau mengekstrak bagian tertentu pada string mulai dari indeks awal hingga akhir sesuai dengan yang ditentukan.
            8. dll

    - Number
        - <div align="justify"> Number adalah tipe data yang mengandung semua angka termasuk angka desimal. Method Number dapat membantu kita dalam memanipulasi data angka, kita tidak perlu membuat fungsi untuk memanipulasi angka secara manual. Beberapa method dan properti Number yang tersedia di JavaScript:
  
            1. toExponential() mengonversi angka ke notasi eksponensial dan mengembalikannya sebagai string.
            2. toFixed() memformat angka ke notasi fixed-point.
            3. toString() mengonversi angka menjadi string.
            4. Number.MAX_VALUE mengembalikan nilai numerika maksimum yang dapat direpresentasikan JavaScript.
            5. Number.MIN_VALUE mengembalikan nilai numerika positif terkecil yang dapat direpresentasikan JavaScript (bukan angka paling negatif), tapi angka yang paling mendekati 0.
            6. Number.isInteger() mengecek apakah suatu nilai bilangan bulat atau bukan.
            7. Number.isNaN() mengecek aapakah suatu nilai adalah NaN atau bukan.
            8. dll. 

    - BigInt
         <div align="justify"> BigInt digunakan untuk menyimpan bilangan bulat tanpa batasasan seperti Number. Kita bisa melakukan operasi matematika dengan aman tanpa khawatir hasilnya salah.Untuk membuat nilai dengan tipe data BigInt sama seperti Number, namun kita perlu mengakhiri nilai dengan huruf 'n' . 
  
   - Boolean
        <div align="justify"> Boolean adalah tipe data yang hanya memiliki dua nilai, true dan false

    - Undefined 
       <div align="justify">tipe data ini merepresentasikan varibel/data yang tidak memiliki nilai. Tipe data undefined biasanya didapat dari hasil kesalahan program (error), kelalaian programmer, dan tidak direncanakan.
	 
  b. Tipe data non-primitif dapat menyimpan lebih dari satu nilai pada satu waktu dan dapat diubah. Tipe data non-primitif akan dianggap berbeda meskipun nilainya sama dan dalam urutan yang sama. Tipe data non-primitif terdiri dari object dan array. Object adalah tipe data yang kompleks yang memungkinkan kita menyimpan kumpulan nilai dengan tipe data yang berbeda. Objek berisi properti yang didefinisikan sebagai pasangan kunci dan nilai (key dan value).Di JavaScript kita bisa membuat objek dengan beberapa cara, bisa menggunakan new Object(), Object.create(), atau menggunakan notasi literal. Sedangkan array Array adalah jenis objek yang dapat digunakan untuk menyimpan beberapa nilai, tanpa properti seperti objek.Array memiliki indeks yang dimulai dari nol dengan kata lain elemen atau nilai pertama di dalam array memiliki indeks 0, elemen berikutnya memiliki indeks 1 dan seterusnya. kita bisa menggunakan indeks untuk memanipulasi nilainya. Sama seperti objek, array juga dapat dibuat menggunakan new Array() atau array literal [ ].
- #### Math
    - <div align="justify"> Objek Math adalah objek yang berisi fungsi-fungsi matematika dan beberapa konstanta untuk melakukan perhitungan matematika seperti sin, cos, tan, eksponen, akar kuadrat, dll.
    - Properti objek math, diantaranya : 
        - Math.E    : Bilangan Euler
        - Math.LN2  : Log 2 
        - Math.LN10 : Log 10
        - Math.LOG2E:Log E di Basis 2
        - Math.LOG10E : Log E di Basis 10
        - Math.PI   : Pi
        - Math.SQRT1_2 : Akar Kuadrat dari 0.5
        - Math.SQRT2   :  Akar Kuadrat dari 2
    - Method objek math, diantaranya : 
        - Math.abs(x) digunakan untuk mengubah angka x yang bernilai negatif menjadi positif.
        - Math.pow(x, y) digunakan untuk menghitung hasil dari x pangkat y.
        - Math.sqrt(x) digunakan untuk menghitung akar kuadrat dari x.
        - Math.cbrt(x) digunakan untuk menghitung akar pangkat 3 dari x.
        - Math.max(x, y, z, ..., n) digunakan untuk mencari angka terbesar di antara parameter x, y, z, ..., n.
        - Math.min(x, y, z, ..., n) digunakan untuk mencari angka terkecil di antara parameter x, y, z, ..., n.

## **DOM (Document Object Model)**

- #### Apa itu DOM ??
    <div align="Justify"> DOM adalah jembatan antara javascript dan HTML, dimana Javascript mampu memanipulasi HTML. Definisi lain, DOM adalah sebuah objek untuk memodelkan dokumen HTML.DOM berbentuk struktur tree.
    <div align="justify"> Objek DOM di javascript bernama document. Objek ini berisi segala hal yang kita butuhkan untuk memanipulasi HTML.Objek ini berisi kumpulan fungsi dan atribut berupa objek dari elemen HTML yang bisa digambarkan dalam bentuk tree.
- ####  cara mengakses elemen yang spesifik, terdapat beberapa fungsi yang bisa digunakan:

    - getElementById(), fungsi untuk memilih elemen berdasarkan atribut id.
        ```
            let title = document.getElementById("title")
        ```
    - getElementByClassName(), fungsi untuk memilih elemen berdasarkan atribut class.
        ```
            let list = document.getElementsByClassName("list")
        ```
    - getElementByTagName(), fungsi untuk memilih elemen berdasarkan nama tag.
        ```
            let itemBytag = document.getElementsByTagName("li")
        ```
    - querySelector(), fungsi untuk memilih elemen berdasarkan query.
        ```
            let listQuery = document.querySelector(".list")
        ```
    - querySelectorAll(), fungsi untuk memilih elemen berdasarkan query.
        ```
            let itemQuery = document.querySelectorAll(".item")
        ```
    - closest, untuk mengambil parents terdekat, atau induk elemen cocok dengan pemilih. Jika tidak ada parents yang ditemukan, metode mengembalikan null. 
        ```
            let itemQuery = document.querySelector(".item")
            console.log(itemQuery); 
            console.log(itemQuery.closest(".list"));
        ```
    - Parent elements, mengembalikan elemen induk dari elemen yang ditentukan, properti ini akan mengembalikan null jika simpul induk bukan simpul elemen.
        ```
            let itemQuery = document.querySelector(".item")
            console.log(itemQuery); 
            console.log(itemQuery.parentElement); 
        ```
    -  next elemen sibling, untuk mengembalikan node berikutnya dari node yang ditentukan sebagai objek Node atau null jika node yang ditentukan adalah yang terakhir dalam daftar.
        ```
           document.getElementById("item1").nextSibling.innerHTML;
        ```
    -  previous elemen sibling, mengembalikan konten HTML dari sibling sebelumnya dari item daftar.
        ```
             document.*getElementById("item2").previousSibling.innerHTML;
        ```

- #### DOM manipulation 
   - Element.innerHTML,  dapat kita gunakan untuk mengubah konten HTML di dalam sebuah element.
        ```
            app.innerHTML = "<h1>Hello World</h1>"
        ```
    - Element.inner text , untuk menentukan dan mengembalikan nilai konten dari suatu element dalam bentuk text atau string. 
        ```
            app.innerText = "<h1>apa kabar ??</h1>"
        ````
    - Element .createElement(), digunakan untuk membuat elemen. 
        ```
            let p = document.createElement("p")
            p.innerText = "ini adalah paragraf"
        ```
    - Element.append, digunakan untuk menambahkan element ke dalam parents baik berupa object node maupun DOM String.
        ```
            app.append(p)
        ```
    - .appendChild, digunakan untuk menambahkan element ke dalam parents baik berupa object node tetapi tidak bisa menggunakan DOM String.
        ```
            let p2 = document.createElement("p")
            p2.innerText = "paragraf ke-2"
            app.appendChild(p2)
        ```
    - Remove(), digunakan untuk menghapus elemen (atau node) dari dokumen
        ```
            let end = document.getElementById("end")
            end.remove()
        ```
    - link. attribute, digunakan untuk melihat dan mengecek attribute apa yang digunakan pada file html. 
   
        ```
            let link = document.getElementsByClassName("link")[0]
            // karena classname, maka menghasilkan html collection sehingga ditambahkan index array ke-0

            console.log(link.attributes) // // untuk cek attribute
        ```
    - SetAttribute, digunakan untuk menambahkan attribute
        ```
            link.setAttribute("id", "google") // menambahkan attribute
        ```
    - link.style, digunakan untuk memberikan styling pada file html dengan DOM. 
        ```
            link.style.color = "black"
            link.style.border = "1px solid black"
            link.style.padding = "5px 20px"
            link.style.backgroundColor = "aqua"
        ```
    - link.style.removeProperty(), digunakan untuk menghapus style properti. 
        ```
            link.style.removeProperty("border")
        ```
    - Mendapatkan style dari element
        ```
            let tess = document.getElementById("tess")
            let tessStyle = getComputedStyle(tess)
            console.log(tessStyle.height)
        ```
    - List of class, Menambahkan class, Menghapus class
        ```
            let container = document.getElementsByClassName("container")[0]
            console.log(container.classList); // [] list of class
            container.classList.add("home") // menambahkan class
            container.classList.remove("container") // menghapus class
        ```


- #### DOM events
   - Apa itu DOM events ??
        <div align="justify"> DOM events adalah kejadian/kegiatan interaksi yang terjadi pada suatu webste. 
   - Cara memberikan event pada html
  
        1. HTML attribute (elemen ini diletakkan pada file html)
            ```
                 <h1 onclick="alert"('Selamat datang')>Hallo</h1>
            ```
        2. event property (elemen ini diletakkan pada file javascript)
            ```
                paragraf.onclick = function(){
                    alert("ini adalah paragraf")
                }
            ```
        3. addeventlistener() (elemen ini diletakkan pada file javascript)
            ```
                let button = document.getElementById("btn")
                button.addEventListener("click", function(){
                    alert("ini adalah paragraf")
                  })
            ```

   - Beberapa jenis events 
  
        1. Click, event yang terjadi ketika user melakukan klik atau tab.
        2. Submit, event yang biasanya terjadi pada form saat kita melakukan submision atau mengirim data pada form.
        3. Focus, akan diaktifkan ketika sebuah elemen telah menerima fokus
        4. Blur, event terjadi karena elemen kehilangan fokus.
        5. Hover, event yang terjadi karena mouse, dimana saat pointer berada di atas element
        6. Change, biasanya terjadi pada elemen input seperti input text, radio, checkbox, select-option, dll. Event change akan terjadi saat nilai pada elemen tersebut berubah.
        7. Scroll, event terjadi ketika user melakukan scroll.
        8. dll.
    - contoh salah satu penggunaan DOM events
        ```
        let button = document.getElementById("btn")
        button.addEventListener("click", function(){
            alert("ini adalah paragraf")
        })
        ```
		
