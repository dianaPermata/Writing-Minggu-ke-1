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
