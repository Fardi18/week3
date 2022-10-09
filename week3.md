# JavaScript Intermediate

- ## Array dan Array Multidimentional

  - ### Array

  Array adalah sebuah tipe data list order yang termasuk ke dalam tipe data non-primitif yang dapat menampung berbagai tipe data lainnya. Array dapat menyimpan data dengan tipe data string, number, boolean dan lain-lain.

  ```javascript
  let namaArray = ["item1", "item2", "item3"];
  console.log(namaArray);
  ```

  Contoh Array:

  ```javascript
  let person = ["Fardi", 20, "Tangerang"];
  console.log(person);
  ```

  - Mengakses Array <br>
    Untuk mengakses data pada array, kita bisa menggunakan yang namanya index. Index di dalam array dimulai dari 0. Misal kita ingin mengakses data 20 pada array person, maka cara mengaksesnya adalah sebagai berikut:
    ```javascript
    let person = ["Fardi", 20, "Tangerang"];
    console.log(person[1]); //output: 20
    ```
  - Update Array <br>
    Untuk dapat update data array kita bisa menggunakan index data y akan diubah tersebut.
    ```javascript
    let person = ["Fardi", 20, "Tangerang"];
    person[2] = "Banten";
    console.log(person);
    //outputnya : ['Fardi', 20, 'Banten']
    ```
  - Const di dalam Array <br>

    1. ika menggunakan let, kita dapat mengubah array dengan array badan konten nilai yang ada di dalam array dengan nilai lain
    2. Const tidak bisa melakukan update data. Namun pada Array kidapat melakukan update konten nilai di dalam array (mutable).
    3. Yang tidak bisa adalah mengubah array dengan array yang baru jimenggunakan const

  - Array Property <br>
    Properties adalah fitur yang sudah disediakan oleh Javascript untmemudahkan developer.
    Array memiliki 5 property yang sering digunakan yaitu constructolength, index, input, dan prototype.

  - Array Method <br>
    Array memiliki method atau biasa disebut built-in methods. Artinnya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan. Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.

    ```javascript
    // .push()
    // untuk menambah item pada index terkahir
    let buah = ["Mangga", "Apel", "Anggur"];
    buah.push("Jambu");
    console.log(buah);

    // .pop()
    // untuk menghapus item pada index terkahir
    let benda = ['meja', 'buku', 'kursi']
    benda.pop()
    console.log(bend
    // .shift()
    // untuk menghapus item array index pertama
    let nama = ['fardi', 'ilham', 'ilyas', 'ferdi']
    nama.shift()
    console.log(nama)

    // .unshift()
    // untuk menambah item array pada index pertama
    let biodata = ['ganteng', 20, 'legok']
    biodata.unshift("fardi")
    console.log(biodata)

    // .splice()
    // untuk menghapus item array di tengah (berdasarkan index)
    let timBola = ['madrid', 'barca', 'city', 'liverpool']
    // timBola.splice(2) : menghapus data mulai dari index ke 2 sam seterusnya
    timBola.splice(2, 1)
    // menghapus data index ke 2 (hanya 1 data saja)
    // timBola.splice(2, 1) : 2 adalah index tujuan dan 1 adalah jumldata yang ingin dihapus
    console.log(timBola)

    // .slice()
    // untuk membuat (copy) array baru dari array yang sudah ada
    let bola = ['bekel', 'bola basket', 'bola voli', 'bola sepak']
    let bolaSlice = bola.slice(2, 4) // mengambil data dengan index kesampai ke 4
    console.log(bola)
    console.log(bolaSlice)
    ```

  - Looping pada Array <br>
    Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach().

    - .forEach()
      Digunakan untuk melakukan looping pada setiap elemen array
      ```javascript
      let penyanyiSoloPria = ["Tulus", "Bruno Mars", "Justin Bieber"];
      penyanyiSoloPria.forEach((element) => {
        console.log(penyanyiSoloPria);
      });
      //Output : 'Tulus', 'Bruno Mars', 'Justin Bieber'
      ```
    - .map()
      Digunakan untuk perulangan dengan membuat array baru
      ```javascript
      let angka = [1, 2, 3, 4, 5];
      let angkaBaru = angka.map((num) => {
        return num + 2;
      });
      console.log(angka);
      //Output : [3, 4, 5, 6, 7]
      ```
      - Perbedaan antara .forEach() dan map() adalah .forEach() tidak akan membuat array baru dan .map() sebaliknya.
      - Jadi, gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.
      - Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

  - ### Array Multidimensional

    Multidimensional array bisa juga disebut sebagai array di dalam array.
    Contoh:

    ```javascript
    let person = [
      ["Nama", "Fardi"],
      ["Umur", 20],
    ];
    ```

    - Akses data multidimensional array <br>
      Misal ingin mengkases data 20, maka caranya adalah
      ```javascript
      let person = [
        ["Nama", "Fardi"],
        ["Umur", 20],
      ];
      console.log(person[1][1]);
      ```
      Sama seperti array satu dimensi, multidimensional array juga dapat menggunakan Property dan Method built-in Array.

<br><br><br>

- ## Object

  Object adalah segala sesuatu baik benda mati atau hidup. Semuanya bisa kita sebut dengan object. Jika dimasukkan ke dalam bahasa pemrograman, object adalah tipe data yang memiliki property dan method dimana property adalah ciri dari objectnya dan method adalah apa saja yang bisa dilakukan oleh sang object tersebut.
  Membuat suatu object :

  ```javascript
  let object = {
    key1: value1,
    key2: balue2,
  };
  ```

  Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

  - Mengakses data pada object <br>

    1. Menggunakan dot

    ```javascript
    let person = {
      nama: "Fardi",
      umur: 20,
    };
    //cara akses data pada object dengan dot (.)
    console.log(person.nama);
    //output : 'Fardi'
    ```

    2. Menggunakan Bracket Notation

    ```javascript
    let person = {
      nama: "Fardi",
      umur: 20,
    };
    //cara akses data pada object dengan bracket notation
    console.log(person["nama"]);
    //out
    ```

  - Update data object

    ```javascript
    let person = {
      nama: "Fardi",
      umur: 20,
    };
    //update data object
    person.umur = 17;
    console.log(person.umur);
    //Output : 17
    ```

  - Delete data object

    ```javascript
    let person = {
      nama: "Fardi",
      umur: 20,
    };
    //hapus data object menggunana delete operator
    delete person.umur;
    ```

  - Method <br>
    Jika value yang kita masukkan pada property berupa function. Maka itu disebut method.

  - Nested Object <br>
    Contoh :
    ```javascript
    let barcelona = {
      namaClub: "Barcelona",
      pelatih: "Xavi",
      pemain: {
        pedri: {
          nama: "Pedri Gonzalves",
          nomorPunggung: 8,
          posisi: "Gelandang",
        },
      },
    };
    console.log("Pemain gelandang", barcelona.namaClub, barcelona.pemain.pedri.nama);
    //Output : Pemain gelandang Barcelona Pedri Gonzalves
    ```
  - Looping Object <br>
    Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping. Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.
    ```javascript
    let barcelona = {
      namaClub: "Barcelona",
      pelatih: "Xavi",
      pemain: {
        pedri: {
          nama: "Pedri Gonzalves",
          nomorPunggung: 8,
          posisi: "Gelandang",
        },
      },
    };
    for (let data in barcelona) {
      console.log(barcelona[data]);
    }
    for (let pemain in barcelona.pemain.pedri) {
      console.log(barcelona.pemain.pedri[pemain]);
    }
    ```
  - Array of Object <br>
    Object sama seperti Array yang bisa menyimpan banyak data. Kita dapat menggunakan array of object untuk data yang lebih dari satu.
    ```javascript
    let pemainBarcelona = [
      {
        nama: "Lewandowski",
        posisi: "Penyerang",
        nomorPunggung: 9,
      },
      {
        nama: 'Ter Stegen',
        posisi: 'Kiper'
        nomorPunggung: 1
      }
    ];
    ```

<br><br><br>

- ## Recursive

  Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.
  Syntaxnya:

  ```javascript
  function recursive() {
    // ...
    recursive();
    // ...
  }
  ```

  - Ciri-ciri Recursive <br>
    1. Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
    2. Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.
  - Contoh kasus Recursive menghitung mundur angka dari 3 sampai 1

    ```javascript
    function countDown(fromNumber) {
    console.log(fromNumber);

    let nextNumber = fromNumber - 1;

    //jika kondisi bernilai false maka recursive berhenti
    if (nextNumber > 0) {
        countDown(nextNumber);
    };
    countDown(3)
    //Output
    // 3
    // 2
    // 1
    ```

<br><br><br>

- ## Asynchronous

  JavaScript merupakan bahasa single-thread, non-blocking dan asyncrhonus. <br> <br>
  Asynchronous yang biasa dikenal juga dengan sebutan non-blocking. <br> <br> mengizinkan komputer kita untuk memproses perintah lain sambil menunggu suatu proses lain yang sedang berlangsung. <br> <br>
  Ini artinya kita bisa melakukan lebih dari 1 proses sekaligus (multi-thread). <br> <br>
  Eksekusi perintah dengan asynchronous tidak akan melakukan blocking atau menunggu perintah sebelumnya selesai. <br> <br>
  Jadi sambil menunggu kita bisa mengeksekusi perintah lain. <br> <br>
  Javascript merupakan bahasa concurrent yaitu seperti menjadikannya bisa multi-task padahal sebenarnya tidak (membentuk ilusi). <br> <br>
  Menjalankan Asyncrhonus pada javascript bisa menggunakan:

  1. `setTimeout(function, milliseconds)` digunakan untuk simulasi pemanggilan kembali proses asynchronous yang sedang/sudah selesai dijalankan. Pemanggilan hanya dilakukan 1 kali.
  2. `setInterval(function, milliseconds)` digunakan untuk simulasi pemanggilan proses asynchronous yang sedang/sudah dijalankan dalam interval waktu tertentu. Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan. <br> <br>

  Penggunaan asynchronous lebih effisien dibandingkan synchronous, tetapi terdapat problem dimana ada satu perintah yang bergantung pada output eksekusi asynchronous sebelumnya. Dengan kata lain fungsi berjalan kejar-kejaran (race condition), sehingga data yang kita inginkan menjadi kosong. <br>
  Untuk mengatasi masalah tersebut kita bisa menggunnakan:

  1. Callback
  2. Promises
  3. Async / Await
     <br><br>

  - Callback <br>
    Callback adalah sebuah function, namun bedanya dengan function pada umumnya adalah pada cara eksekusinya. Jika function pada umumnya dieksekusi secara langsung, sedangkan callback dieksekusi di dalam function lain melalui parameter. <br>
    Singkatnya, Callback adalah sebuah function yang dijadikan argumen.

    - Membuat Callback Function
      Kita dapat memanggil callback pada sebuah function dengan cara memanggilnya ke dalam parameter dan digunakan di dalam function.
      **Pertama**, kita deklarasikan dahulu function `greeting(name)` yang ingin kita panggil dalam callback function lain. Function `greeting(name)` berisi `console.log()` yang menerima sebuah parameter `name`.

      ```javascript
      function greeting(name) {
        console.log(`Halo ${name}, selamat datang di Skilvul!`);
      }
      ```

      **Kedua**, buat sebuah function `introduction(firstName, lastName, callback)` dengan menerima parameter `firstName`, `lastName` dan `callback` lalu di dalam function tersebut kita menggabungkan parameter `firstName` dan `lastName` ke dalam variabel `fullName` untuk mengirimkannya ke dalam `callback`.

      ```javascript
      function introduction(firstName, lastName, callback) {
        const fullName = `${firstName} ${lastName}`;

        callback(fullName);
      }

      introduction("Miftah", "Faris", greeting);
      //Output : Halo Miftah Faris, selamat datang di Skilvul !
      ```

      **Ketiga**, dalam pemanggilan function `introduction`, kita mengisi argumen dari parameter yang dibutuhkan yaitu Miftah, Faris, dan function `greeting` yang sudah kita buat sebelumnya lalu kita panggil `callback(fullName)` di dalam function `introduction` sehingga kita bisa mendapatkan hasil dari function `greeting`.

  - Promise <br>
    Promise adalah salah satu fitur dari ES6 (ES2015) JavaScript. Konsep promise hadir untuk memecahkan masalah yang bertele-tele dengan callback, semakin banyak kita menggunakan callback untuk proses asynchronous semakin kompleks dan sulit kode kita untuk dibaca dan dipelihara. Kita juga akan sering menghadapi callback di dalam callback dan seterusnya. Masalah seperti ini disebut dengan Callback Hell. <br>

    - Konsep Promise <br>
      Promise sesuai dengan artinya adalah janji. Seperti ketika kita berjanji, jika apa yang kita janjikan bisa kita lakukan maka kita harus melakukannya, jika janjinya ada halangan maka kita tidak bisa melakukannya atau jika janji tersebut belum pada waktunya kita juga harus menunggunya. <br>
      Beberapa istilah dalam Promise : 1. Pending = Jika kita belum melewati batas waktu dilaksanakan dan belum mengetahui janji tersebut bisa ditepati atau tidak. 2. Fullfiled = Jika janji berhasil dipenuhi sebelum batas waktu yang ditentukan. 3. Rejected = Jika janji gagal ditepati karena suatu hal dan kita melakukan rencana lain. 4. Settled = Jika semua janji sudah selesai terpenuhi kita sudah bebas melakukan hal lainnya.

      - 3 Status Promise dalam JavaScript <br>
        1. **pending**, jika data sedang diproses.
        2. **fulfilled**, jika data telah berhasil didapatkan. <br>
        3. **rejected**, jika data gagal didapatkan.
      - Membuat sebuah Promise <br>
        Menggunakan new

        ```javascript
        let newPromise = new Promise((resolve, reject) => {
          if (true) {
            // apa yang dilakukan jika promise fulfilled
            resolve("Berhasil");
          } else {
            // apa yang dilakukan jika promise rejected
            reject("Gagal");
          }
        });
        ```

        Kita bisa membuat sendiri apa yang akan dilakukan pada sebuah promise. Di dalam promise ada 2 keyword yaitu `resolve()` dan `reject()`.

        `resolve()`, jika proses berhasil atau fullfilled.
        `reject()`, jika proses gagal atau rejected.

      - Penggunaan promise fullfiled <br>
        Untuk fulfilled hanya bisa tereksekusi jika kita kondisi berhasil pada saat kita melakukan async. Kita set condition menjadi true untuk simulasi fulfilled.

        ```javascript
        const condition = true;

        let newPromise = new Promise((resolve, reject) => {
          if (condition) {
            // apa yang dilakukan jika promise 'fulfilled'
            resolve("Berhasil");
          } else {
            // apa yang dilakukan jika promise 'rejected'
            reject(new Error("Error Gagal"));
          }
        });
        ```

        Untuk bisa mengeksekusi promise yang sudah dibuat kita bisa memanggil promise tersebut menggunakan `.then():`

        ```javascript
        const condition = true;

        let newPromise = new Promise((resolve, reject) => {
          if (condition) {
            // apa yang dilakukan jika promise 'fulfilled'
            resolve("Berhasil");
          } else {
            // apa yang dilakukan jika promise 'rejected'
            reject(new Error("Error Gagal"));
          }
        });

        newPromise.then((result) => {
        console.log(result); // Output: "Berhasil"
        ```

      - Penggunaan promise rejected <br>
        Untuk rejected hanya bisa tereksekusi jika kita mengalami error pada saat kita melakukan proses asynchronous. Kita set condition menjadi false untuk simulasi rejected.:

        ```javascript
        const condition = false;

        let newPromise = new Promise((resolve, reject) => {
          if (condition) {
            // apa yang dilakukan jika promise 'fulfilled'
            resolve("Berhasil");
          } else {
            // apa yang dilakukan jika promise 'rejected'
            reject(new Error("Error Gagal"));
          }
        });
        ```

        Untuk bisa mengantisipasi jika terjadi error kita bisa menambahkan
        `.catch()` pada promise. Sehingga, kita bisa memberi tahu pengguna jika terjadi suatu error:

        ```javascript
        const condition = false;

        let newPromise = new Promise((resolve, reject) => {
          if (condition) {
            // apa yang dilakukan jika promise 'fulfilled'
            resolve("Berhasil");
          } else {
            // apa yang dilakukan jika promise 'rejected'
            reject(new Error("Error Gagal"));
          }
        });

        newPromise
          .then((result) => {
            console.log(result);
          })
          .catch((error) => {
            console.log(error.message); // Output: "Error Gagal"
          });
        ```

    <br><br><br>

- ## Web Storage

  Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. Data ini dimanfaatkan oleh situs web tersebut untuk merekam kebiasaan pengguna agar dapat memberikan rekomendasi sesuai preferensi si pengguna tersebut. <br>

  - Cookies <br>
    Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB). <br>
    Biasanya data yang disimpan di cookies adalah access token pengguna saat login atau data pencarian saat melakukan pencarian pada situs web tertentu. Hal ini yang biasanya dilakukan oleh situs pencarian untuk melacak pencarian kita dan menampilkan iklan yang berhubungan dengan pencarian kita sebelumnnya. <br>
    Kekurangan Cookies:
    1. Memperlambat aplikasi web dengan mengirimkan data yang sama setiap kita akses website.
    2. Harus mengenskripsi terlebih dahulu saat ingin menyimpan data dalam cookies karena data tidak dienskripsi melalui internet.
    3. Penyimpanan yang sangat kecil (4kb)
    4. Memiliki kadaluarsa
  - Local Storage <br>
    LocalStorage merupakan salah satu cara yang dapat digunakan untuk menyimpan data di web browser. <br>
    Beberapa karakteristiknya adalah local storage:

    1. Tidak ada kadaluarsa
    2. Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
    3. Dapat menyimpan data hingga 5MB.
    4. Hanya dapat menyimpan data string.

    - Kita bisa menyimpan data menggunakan method `setItem()` dengan 2 parameter : `key` dan `value`

    ```javascript
    localStorage.setItem("key", value);
    ```

    - Kita bisa mengambil data menggunakan method `getItem()` dengan 1 parameter : `key`

    ```javascript
    localStorage.getItem("key");
    ```

    - Kita bisa menghapus data menggunakan method `removeItem()` dengan 1 parameter : `key`

    ```javascript
    // menghapus key tertentu
    localStorage.removeItem("key");

    // menghapus semua key
    localStorage.clear();
    ```

  - Session Storage <br>
    Berbeda dengan local storage, walaupun masuk ke dalam web storage, data yang tersimpan pada session storage akan hilang ketika session dari sebuah laman berakhir. <br>
    Beberapa karakteriktik session storage :

    1. Data yang disimpan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.
    2. Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.
    3. Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.
    4. Data yang tersimpan dalam session storage harus berbentuk string.
    5. Hanya dapat menyimpan data sebanyak 5MB.

    - Kita bisa menyimpan data menggunakan method `setItem()` dengan 2 parameter : `key` dan `value`

    ```javascript
    // menambah session storage
    sessionStorage.setItem("key", value);
    ```

    - Kita bisa mengambil data menggunakan method `getItem()` dengan 1 parameter : `key`

    ```javascript
    // mendapatkan session storage
    sessionStorage.getItem("key");
    ```

    - Kita bisa menghapus data menggunakan method `removeItem()` dengan 1 parameter : `key`

    ```javascript
    // menghapus session storage satu persatu berdasarkan key
    sessionStorage.removeItem("key");

    // menghapus seluruh session storage sekaligus
    sessionStorage.clear();
    ```
