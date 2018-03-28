# firts-task
Learn Markdown

## Apa itu Markdown?

Bagi yang sering bermain di Github dan web serupa, pasti sering melihat markdown. Biasanya markdown digunakan untuk menuliskan dokumentasi.

Pada dasarnya markdown sama seperti HTML. Namun, lebih sederhana dan mudah dibaca.

Saat ini markdown sudah digunakan untuk:

Dokumentasi;
- SSG (Static Site Generator);
- CMS seperti Ghost, Wordpress, Tumblr, dll.;
- Penulisan Buku;
- Format teks pada chat: Telegram, WA, Facebook;
- dll.

Markdown adalah (lightweight markup language) bahasa markup yang lebih ringan dari HTML untuk formatting teks.

Markdown bisa dikonversi ke dalam HTML menggunakan beberapa aplikasi. Biasanya menggunakan markdown editor itu sendiri.

Markdown dibuat pada tahun 2004 oleh John Gruber. Tujuannya untuk mempermudah penulisan dokumen web—mudah ditulis dan mudah dibaca—Karena menulis langsung HTML terasa melelahkan dan susah dibaca.

Contoh:
```
    Aku *sedang* belajar **menulis** dengan [markdown](https://en.wikipedia.org/wiki/Markdown).
```

Teks ini akan dikonversi ke HTML menjadi seperti ini:

Aku *sedang* belajar **menulis** dengan [markdown](https://en.wikipedia.org/wiki/Markdown).


## Editor untuk menulis Markdown
#### Markdown Editor di Mac OSX
- Mou - Free
- iA Writer - $19.99
- Desk - $29.99
- ByWord - $11.99
- Day One - $9.99
- SublimeText - $70

#### Markdown Editor di Windows
- WriteMonkey - Free
- MarkdownPad - Free + $14.99 Pro version
- Texts - $14.50
- SublimeText - $70

#### Markdown Editor di Linux
- [Remarkable](https://remarkableapp.github.io/) - Free
- Haroopad - Free
- ReText - Free
- UberWriter
- Mark My Words

## File Markdown
File markdown dapat kita simpan dengan ekstensi `.markdown` atau `.md`.

## Format dasar Markdown
#### Heading
Contoh:
```
    # Heading 1
    ## Heading 2
    ### Heading 3
```
Hasil:
```html
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
    <h3>Heading 3</h3>
```
Heading ini sampai level 6 seperti pada HTML. Jumlah tanda pagar di depannya menandakan levelnya.

#### Format Teks
Contoh:
```
    **Tebal**
    *miring*
    ~~strikeline~~
```

#### Membuat Link
Contoh:
```
    [link ke petanikode](https://www.petanikode.com/)
```

#### Menyisipkan Gambar
Contoh:
```
    ![Gambar teks editor VS Code](https://www.petanikode.com/img/markdown/markdown-vscode.png)
```
Hasil:
![Gambar teks editor VS Code](https://www.petanikode.com/img/markdown/markdown-vscode.png)

#### Membuat List
Contoh:
```
    * Milk
    * Bread
        * Wholegrain
    * Butter


    1. Tidy the kitchen
    2. Prepare ingredients
    3. Cook delicious things
```
Hasil:
* Milk
* Bread
    * Wholegrain
* Butter


1. Tidy the kitchen
2. Prepare ingredients
3. Cook delicious things

#### Menyisipkan Quote
Contoh:
```
    > To be or not to be, that is the question.
```
Hasil:
> To be or not to be, that is the question.


##### Referensi
[https://www.petanikode.com/markdown-pemula/](https://www.petanikode.com/markdown-pemula/)

---





# ES6 Variable

Di dalam JavaScript kita tidak perlu mendeklarasikan jenis tipe data. Seluruh variabel di dalam JavaScript dapat berisi nilai apapun (tipe data apapun), dan dapat diubah menjadi tipe lain sepanjang program. Untuk mendeklrasikan sebuah variabel ada 3 cara yaitu menggunakan const, let, dan var.

**let dan var** : fungsi dari let dan var sebenarnya sama untuk mendeklarasikan variabel yang nilainya dapat diubah. Namun perbedaanya adalah var mempunyai cakupan dalam sebuah fungsi (function scope) dan let mempunyai cakupan dalam sebuah block (block scope). Bingung apa maksudnya? oke saya akan memberikan sebuah contoh melalui code.

**var (function scope)**
```js
    function looping() {
        for (var i = 0; i < 5; i++) {
            console.log(i); // 0 1 2 3 4 5
        }
        function inLooping() {
            console.log(i); // 5
        }
        inLooping();
    }
    looping();
```
Jika code diatas dijalankan maka akan mengeluarkan output yang sesuai pada comment code baris 2 dan 4.

> Variabel yang dideklarasikan menggunakan var hanya dapat dipanggil dalam cakupan sebuah fungsi dimana variabel tersebut dideklarasikan. Child function juga dapat memanggil variabel yang dideklarasikan menggunakan var pada root functionnya

**let (block scope)**

Contoh:
```js
    for (let i = 0; i < 5; i++) {
        console.log(i); // 0 1 2 3 4
    }
    if (true) {
        let i = "100";
        console.log("i = ",i); // i = 100
    }
```
Nah jika kalian menjalankan code diatas akan mengeluarkan output seperti comment pada baris 2 dan 6. Ini dikarenakan variabel yang dideklarasikan menggunakan let dipanggil dalam block scope masing-masing.

> dari contoh code diatas adalah variabel yang dideklarasikan menggunakan let hanya dapat dipanggil dalam sebuah block scope yang sama. Sebuah block scope dapat ditandai dengan sebuah kurung kurawal { ….. some code here ….. }

**const (variabel konstanta)**

Sifat const sama seperti let, namun perbedaanya variabel yang dideklarasikan menggunakan const tidak dapat diubah nilainya atau *immutable variables*.

Contoh:
```js
    const phi = 3.14;
    phi = 3.147;

    console.log(phi)
```
Jika code diatas dijalankan maka akan mengeluarkan output error *TypeError: Assignment to constant variable*. Ini menandakan sebuah variabel yang dideklarasikan menggunakan const nilainya tidak dapat diubah atau *di-reassign*.

##### Referensi
[https://medium.com/@renopp/kenalan-dengan-es6-javascript-introduction-variable-arrow-function-part1-6bd5c148473b](https://medium.com/@renopp/kenalan-dengan-es6-javascript-introduction-variable-arrow-function-part1-6bd5c148473b)

---





# Javascript ES6 – Template literal

Penulisan string sangat penting dalam javascript. Terdapat beberapa perubahan yang terjadi saat kita akan melakukan printing terhadap suatu variabel atau hanya literal biasa. Jika biasannya kita menggunakan “+” untuk memisahkan literal dan suatu variabel maka pada ES6 diperkenalkan suatu metode baru yang bernama template string. Penggunaan template string ini sangat membantu kita untuk mengkombinasikan literal dengan variabel.

### Akses variabel
Pada non-es6 format untuk menuliskan “hello world” yang tersimpan dalam suatu variabel maka syntax yang kita gunakan adalah sebagai berikut ini.

```js
    var nama = 'dengananda ferdian priyambada';
    console.log(nama);
```

Dengan menggunakan ES6 kita diperkenalkan dengan istilah template string. Template ini dapat menampilkan literal dan variabel (kombinasi) tanpa menggunakan pemisah “+” (tanda/simbol plus). Data non literal dapat diapit dengan menggunakan “`” dan kemudian setelah itu letakan dollar ($) dan masukan nama variabel diantara dua bracket ({nama variabel}). Simbol ini terletak dipojok kiri keyboard anda disamping kiri keypad angka 1. Sesuatu yang berada di dalam apitan atau diantara tanda tersebut(${sesuatu}) akan diasosiasikan dengan :

- Variabel yang berada dalam class / file javascript
- Operasi aritmatika
- String method

Template string sangat berguna dan memudahkan kita dalam menulis program. Karena kita tidak perlu menggunakan tanda “+” (plus/tambah) saat hendak menggabungkan literal dan juga non literal misalkan variabel. Karena menggunakan + akan sangat merepotkan , lebih banyak karakter yang harus ditulis dan diperhatikan. Lihatlah perbedaannya dibawah ini.

ditulis tanpa menggunakna template string.

```js
    var nama = 'dengananda ferdian priyambada';
    var alamat  = 'jl xxxx 250 surabaya';
    console.log("nama saya adalah " + nama + "
    Saya tinggal di " + alamat);
```

ditulis dengan menggunakan template string

```js
    var nama = 'dengananda ferdian priyambada';
    var alamat  = 'jl xxxx 250 surabaya';
    console.log(`nama saya adalah ${nama} 
    Saya tinggal di alamat ${alamat}`);
```

sehingga, sebisa mungkin untuk menggunakan template string untuk memudahkan pekerjaan dan kode menjadi sangat CLEAN dan enak untuk dilihat.

##### Referensi
[https://degananda.com/javascript-es6-template-literal/](https://degananda.com/javascript-es6-template-literal/)

---





# Git Flow

![alur git](https://abas.github.io/asset/git-design-pattern.svg)

### Inisialisasi - `git init`

Contoh:
```
  $ git init
```

Berfungsi untuk menginisialisasi directory sebagai **local** repository, maksudnya kita akan membuat folder yang diinit sebagai local repository atau singkat nya **`folder yang akan di upload`**.

### Tracked File - `git add {nama.file}/{nama.directory}`
Contoh:
```
  $ git add README.md
```

berfungsi untuk mengtrack **new/modified** file, jadi ketika ada file baru atau file yang termodifikasi maka untuk mengupload ke [github](https://github.com/) repository kita perlu meng-track file tersebut baru bisa kita upload.

### Commit Message - `git commit -m '{message}'`
Contoh:
```
  $ git commit -m 'ini adalah pesan perubahan'
```

ketika kita push perubahan pada [github](https://gtihub.com/) tentu kita perlu menyertakan atau memberitahu apasih yang kita rubah disitu? jadi **git commit** itu berfungsi memberi pesan commit atau pesan perubahan yang terjadi pada [github](https://gtihub.com/) repository.

### Push Update - `git push {nama.remote} {nama.branch}`
Contoh:
```
  $ git push origin master
```

untuk melakukan perubahan pada [github](https://github.com/) repository kita gunakan command `git push` diatas terdapat origin yang berarti nama remote yang kita gunakan, remote disini yaitu alamat repository [github](https://github.com/) yang akan kita update, sementara master adalah nama branch(cabang) yang kita gunakan.

![git flow](https://abas.github.io/asset/git-fork-push-pull.svg)

##### Referensi
[https://abas.github.io/2017/12/12/Git-Flow/](https://abas.github.io/2017/12/12/Git-Flow/)

---





# Memahami Konsep …args pada Fungsi JavaScript untuk Pemula

### Apa itu ..args pada Javascript

Setelah dicari-cari dari berbagai literatur akhirnya saya menemukan jawabannya. Arguments adalah nilai yang ditampung dari seluruh argumen yang dikirimkan kepada sebuah fungsi. Pada Javascript ES5 penulisan argument adalah ‘arguments’ sedangkan pada javascript ES6 penulisan disingkat menjadi ‘args’.

Contoh kode:
```js
  var a = function (){
    console.log("fungsi a");
  };
  var b = function (){
    console.log("fungsi b");
  };
  var c = function (){
    console.log("fungsi c");
  };
  function tampung (...args){
    console.log(args)
  }
  tampung(a(),b(),c());
  // fungsi a
  // fungsi b
  // fungsi c
```

#### Kesimpulan:


1. Fungsi ‘…args’ adalah nilai yang ditampung dari argument yang dikirim ke sebuah fungsi meski argumen tersebut tidak didaftarkan.
2. Fungsi ‘…args’ adalah solusi jika kita ingin membuat fungsi yang inputan datanya bersifat dinamis.
3. Dengan menambahkan fungsi ‘…args’ kita bisa mencegah error.
4. Meskipun ‘…args’ bisa dibaca dengan metode array, namun ‘…args’ sebanarnya bukanlah array. [penting!]

##### Referensi
[https://medium.com/musliadi/memahami-konsep-args-pada-fungsi-javascript-untuk-pemula-cc500b76cc12](https://medium.com/musliadi/memahami-konsep-args-pada-fungsi-javascript-untuk-pemula-cc500b76cc12)
# 1. GIT FLOW
![Gitflow Image](https://s3-ap-northeast-1.amazonaws.com/mash-jp/production/posts/33601/77e43d06d94a73c9a220c6a077b523f8575a3794.33653.desktop.png?1487731115)

### Apa Itu Gitflow ?
Git-Flow adalah sebuah ekstensi git untuk menyediakan operasi repositori tingkat tinggi untuk model percabangan *(Branching Model)*.

### Tips Dasar
* Git flow menyediakan bantuan command line yang sangat baik. Baca perlahan untuk melihat apa yang terjadi
* Git-flow adalah solusi berbasis merge. Ini tidak me-rebase fitur branch.

### Setup
* Sebagai syaratnya, kita diharuskan memasang/menginstal git. Git flow sendiri dapat bekerja pada OSX, Linux dan Windows.
* Untuk detail instruksi pemasangan **Git Flow** kita bisa kunjungi [Git Flow Wiki](https://github.com/petervanderdoes/gitflow-avh/wiki/Installation).

```java
$ brew install git-flow-avh
// Instalasi untuk OSX
```
```java
$ apt-get install git-flow
// Instalasi untuk Linux
```
```java
$ wget -q -O - --no-check-certificate https://raw.github.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh install stable | bash
// Instalasi untuk Windows
```

### Referensi
* [Rujukan GitFlow](https://danielkummer.github.io/git-flow-cheatsheet/index.id_ID.html)



# 2. MARKDOWN
![Markdown Image](https://static.cdn-cdpl.com/wp-images/2014/05/codimio_markdown-image(700x350-crop).jpg)
### Apa Itu Markdown ?
**Markdown** adalah *(lightweight markup language)* bahasa markup yang lebih ringan dari **HTML** untuk formatting teks.

**Markdown** bisa dikonversi ke dalam **HTML** menggunakan beberapa aplikasi. Biasanya menggunakan markdown editor itu sendiri atau aplikasi lain yang tersedia di masing masing System Operasi. Namun sekarang sudah banyak Text Editor yang menyediakan Plugin untuk *Preview Markdown*. *Sebagai contoh disini saya menggunakan* **Sublime Text 3**.

**Markdown** dibuat pada tahun 2004 oleh **John Gruber**. Tujuannya untuk mempermudah penulisan dokumen Web (mudah ditulis dan mudah dibaca). Karena menulis langsung menggunakan **HTML** terasa melelahkan dan susah dibaca.

### File Markdown
File markdown dapat kita simpan dengan ekstensi `.markdown` atau `.md`.

Contoh : `belajar.md` atau `belajar.markdown`.

### Format Dasar Markdown
Untuk format format dasar perintah **Markdown**, silakan teman teman pelajari salah satu artikel dari [Petani Kode](https://www.petanikode.com/) yang satu ini [Format Dasar Markdown](https://www.petanikode.com/markdown-pemula/).

### Referensi
* [Format Dasar Markdown](https://www.petanikode.com/markdown-pemula/)


# 3. ES6 Variabel
![Es6 Image](https://cdn-images-1.medium.com/max/1280/1*lNPsaF_3m5QMU4jNVBn25Q.jpeg)
### Apa itu ES6 ?
**ES6** adalah sebuah singkatan dari  *ECMAScript versi 6*. ES6 rilis pada tahun 2015, sehingga ES6 sering juga disebut ES 2015. 

Lalu apa itu **ECMAScript** ? ECMAScript adalah standarisasi scripting language (*Javascript*) yang dibuat oleh [European Computer Manufactur Associaton (ECMA)](https://en.wikipedia.org/wiki/Ecma_International). Untuk menjalankan sebuah program yang ditulis menggunakan ES6, kita dapat menggunakan NodeJS. Dengan perintah seperti ini :

**`node namaFileJS`**

### Variabel
Di dalam JavaScript kita tidak perlu mendeklarasikan jenis tipe data, seluruh variabel di dalam JavaScript dapat berisi nilai apapun (tipe data apapun). Untuk mendeklarasikan sebuah variabel ada 3 cara, yaitu menggunakan *const*, *let*, dan *var*.

##### let dan var
Fungsi dari **let** dan **var** sebenarnya sama, yaitu *mendeklarasikan variabel yang nilainya dapat diubah*.
Perbedaanya adalah **var** mempunyai cakupan dalam sebuah fungsi *(function scope)* dan **let** mempunyai cakupan dalam sebuah block *(block scope)*.
* **var (function scope)**

```java
for (var i = 1; i <= 3; i++) {
    console.log(i) // 1 2 3
}
console.log(i) // 4
//var-1.js
```

```java
function looping() {
    for (var i = 1; i <= 3; i++) {
        console.log(i); // 1 2 3
    }
}
looping();
console.log(i); // ReferenceError: i is not defined
//var-2.js
```

> Jika kita jalankan kode pada **`var-1.js`** maka output nya akan sesuai dengan yg tertera di komentar pada baris ke 2 dan 4.
> Bagaimana jika **`var-2.js`** kita jalankan ? Maka hasilnya juga akan sama dengan yg ada dikomentar pada baris ke 3. Karena variabel i dideklarasikan menggunakan **var** didalam function looping(). Sedangkan pada baris ke 7, kita memanggil variabel i diluar function looping(). Ini menunjukan jika **var** hanya berjalan pada cakupan function *(function scope)*. 

* **let (block scope)**

```java
for (let i = 1; i <= 3; i++) {
  console.log(i); // 1 2 3
}
console.log(i); // ReferenceError: i is not defined
// let-1.js
```

```java
for (let i = 1; i <= 3; i++) {
  console.log(i); // 1 2 3
}
if (true) {
    let i = "10";
    console.log("i = ",i); // i = 10
}
// let-2.js
```

>Jika **`let-1.js`** dijalankan maka akan mengeluarkan output *ReferenceError: i is not defined*. Kenapa? karena batas sebuah block adalah sebuah kurung kurawal **{ some code here }**.
>Nah jika kita menjalankan **`let-2.js`** akan mengeluarkan output seperti comment pada baris 2 dan 6. Ini dikarenakan variabel yang dideklarasikan menggunakan **let** dipanggil dalam *block scope* masing-masing.

##### conts
Sifat **const** sama seperti let, namun perbedaanya variabel yang dideklarasikan menggunakan **const** tidak dapat diubah nilainya atau *immutable variables*.

* **const (variabel konstanta)**
```java
const phi = 3.14;
phi = 3.147;

console.log(phi // TypeError: Assignment to constant variable.
// const-1.js
```

>Pesan error pada komentar di baris ke 4, menandakan sebuah variabel yang dideklarasikan menggunakan **const** nilainya tidak dapat diubah atau di-reassign.

### Referensi
* [Kenalan Dengan ES6 JavaScript](https://medium.com/@renopp/kenalan-dengan-es6-javascript-introduction-variable-arrow-function-part1-6bd5c148473b)


# 4. TEMPLATE LITERAL
![Template Literal Image](https://assets.hongkiat.com/uploads/thumbs/640x410/ecmascript-6-template-literals-twitter.jpg)

Jika biasannya kita menggunakan “+” untuk memisahkan literal dan suatu variabel maka pada ES6 diperkenalkan suatu metode baru yang bernama template string. Penggunaan template string ini sangat membantu kita untuk mengkombinasikan literal dengan variabel.

* **Akses Variabel**

>Pada *Non-ES6* format, jika kita Ingin menampilkan tulisan "Rindang Ramadhan" yang tersimpan di dalam variabel, maka syntax yang digunakan sebagai berikut :
```java
var nama = "Rindang Ramadhan";
console.log(nama); // Rindang Ramadhan
```

Dengan menggunakan ES6 kita diperkenalkan dengan istilah *Template String*. Template ini dapat menampilkan literal dan variabel (kombinasi) tanpa menggunakan pemisah **“+”** (tanda/simbol plus). Data non literal dapat diapit dengan menggunakan **“`”** dan kemudian setelah itu letakan dollar **($)** dan masukan nama variabel diantara dua bracket *({nama variabel})*.

```java
var nama = "Rindang Ramadhan";
console.log(`${nama}`); // Rindang Ramadhan
```
contoh diatas adalah jika kita memanggil variabel *nama* dengan menggunakan template string yang mana variabel tersebut kita apit dengan menggunakan simbol **“`”**.

Jika kita ingin mengkombinasikan literal dan variabel maka letakan literal tersebut diluar apitan simbol **“${}”**. Maka implementasinnya adalah seperti berikut ini.
```java
var nama = "Rindang Ramadhan";
console.log(`Halo Saya ${nama}`); // Halo Saya Rindang Ramadhan
```

* **Aritmatika**
>Sesuatu yang berada didalam **${}** dalam diasosiasikan dengan proses aritmatika seperti pertambahan, pengurangan, pembagian maupun perkalian. Sebagai contoh kita akan operasikan variabel didalam simbol/syntax **${}** tersebut.

```java
var angka1 = 1;
var angka2 = 2;
console.log(`Penjumlahan ${angka1} + ${angka2} adalah <1>angka1+angka2</1>`) // Penjumlahan 1 + 2 adalah 3
```

* **String Method**
>Tidak hanya itu saja, kita juga dapat menggunakan method yang terkait variabel-variabel tersebut. Misalnya kita memiliki variabel string. Kita dapat melakukan fungsi seperti indexof untuk mendapatkan index dari karakter tertentu, membesarkan huruf (menjadikan uppercase) terhadap string tersebut dan metode lain yang berhubungan dengan variabel tersebut.

```java
var nama = "Rindang Ramadhan";
console.log(`Nama saya ${nama.toLocaleUpperCase()}`); // Nama saya RINDANG RAMADHAN 
```

* **Multiline**
>Dengan template literal ini kita dapat menuliskan literal secara multiline. Perhatikan contoh dibawah ini.
```java
console.log(`
    Rindang Ramadhan
    Santri Programmer
    PT. Andaglos Global Teknologi
    `);
// Rindang Ramadhan
// Santri Programmer
// PT. Andaglos Global Teknologi
```

### Referensi
* [Javascript ES6 - Template Literal](https://degananda.com/javascript-es6-template-literal/)


# 5. NAMED ARGUMENTS
![Named Arguments Image](https://cdn-images-1.medium.com/max/800/1*3Pa_j7j3pDeqnIfsQb1HUA.png)

### Apa itu ..args pada Javascript ?
**Arguments** adalah nilai yang ditampung dari seluruh argumen yang dikirimkan kepada sebuah fungsi. Pada Javascript ES5 penulisan argument adalah **‘arguments’** sedangkan pada javascript ES6 penulisan disingkat menjadi **‘args’**.

```java
function sum (a,b){ //menerima 2 argumen
   return a+b; 
}
// kita malah mengirim 3 argumen
sum(2,3,4); // error
```
>Pada contoh fungsi diatas kita tidak diperkenankan mengirim argumen melebihi jumlah data yang kita daftarkan, dalam bahasa lain fungsi diatas bersifat statis. Padahal dalam kasus lain kita ingin argumen yang kita kirimkan ke fungsi dapat bersifat dinamis. Disini lah **`args`** berperan..

```java
function list (...args){
   return console.log(...args); // Fahrizal Rama Riko
}
list("Fahrizal","Rama","Riko");
// arg1
```

```java
function list (...args){
   return console.log(args); // ['Fahrizal', 'Rama', 'Riko'] tanpa "..."
}
list("Fahrizal","Rama","Riko");
// arg2
```

```java
function sum (a,...args){
// kita bisa membaca argument dengan metode array
  console.log(a+args[0]+args[1]); // 9
}
// 2 adalah argument yang deftar pada a, 
// sedangkan 3,4 terdaftar ke 'args'
sum(2,3,4);
// arg3
```

#### Kesimpulan
* Fungsi **‘…args’** adalah nilai yang ditampung dari argument yang dikirim ke sebuah fungsi meski argumen tersebut tidak didaftarkan.
* Fungsi **‘…args’** adalah solusi jika kita ingin membuat fungsi yang inputan datanya bersifat dinamis.
* Dengan menambahkan fungsi **‘…args’** kita bisa mencegah error.
* Meskipun **‘…args’** bisa dibaca dengan metode array, namun ‘…args’ sebanarnya bukanlah array. [penting!]


### Referensi
* [Musliadi - Medium](https://medium.com/musliadi/memahami-konsep-args-pada-fungsi-javascript-untuk-pemula-cc500b76cc12)
