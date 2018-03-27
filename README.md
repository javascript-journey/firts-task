# firts-task


## 1. Git Flow yang benar
Git flow yang benar atau cara pemakain git yang benar adalah sebuah ekstensi git untuk menyediakan operasi repositori tingkat tinggi untuk model percabangan atau branching model. Untuk lebih jelas nya cek [disini](http://nvie.com/posts/a-successful-git-branching-model/) ya.

### Setup
Sebelum kamu memulai atau membuat Git flow, pastikan komputer kamu sudah terinstal git ya.
Git flow dapat bekerja pada OSX, LINUX dan Windows.

Instalasi pada OSX *Homebrew*
> $ brew install git-flow-avh

Instalasi pada OSX *Macports*
> $ port install git-flow-avh

Instalasi pada Linux
> $ apt-get install git-flow

Instalasi pada Windows(Cygwin)
> $ wget -q -O - --no-check-certificate https://raw.github.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh install stable | bash

Kamu membutuhkan wget dan util-linus untuk menginstal git-flow.

Untuk detail instruksi pemasangan git flow kamu bisa cek [disini](https://github.com/petervanderdoes/gitflow-avh/wiki/Installation)

### Inisialisasi
Git flow membutuhkan inisialisasi untuk menyesuaikan dengan proyek kamu.
Untuk memulai menggunakan git-flow dengan menginisialisasi dalam repositori git yang sudah ada :
> git flow init

Setelah menjalankan perintah di atas, kamu diharuskan menjawab beberapa pertanyaan mengenai konvensi nama untuk branch kamu. Sangat disarankan untuk menggunakan nilai bawaan.

### Fitur
* Mengembangkan fitur baru untuk rilis selanjutnya
* Khususnya hanya dalam repositori yang sudah ada sebelumnya

##### Mulai Sebuah fitur baru
Pengembangan fitur baru dimulai dari branch 'develop'.
Mulai pengembangan sebuah fitur baru dengan
> git flow feature start FITURSAYA

Perintah ini membuat sebuah branch fitur baru berdasarkan 'develop' dan beralih ke branch tersebut.

##### Menyelesaikan sebuah fitur
Untuk menyelesaikan sebuah fitur yang telah kamu buat, kamu bisa lakukan cara berikut :

* Merge FITURSAYA kedalam 'develop'
* Menghapus branch fitur
* Beralih kembali ke branch 'develop'

> git flow feature finish FITURSAYA

##### Mempublikasikan sebuah fitur
Jika kamu mengembangkan sebuah software dengan kolaborasi, maka kamu harus mempublikasikan fitur yang telah kamu buat ke dalam server remote agar bisa digunakan oleh pengguna lain. Caranya :
> git flow feature publish FITURSAYA

##### Mendapatkan sebuah fitur yang telah terpublikasi
Kalo tadi kamu mempublikasi kan fitur yang telah kamu selesaikan supaya teman mu bisa menggunakan nya. Terus bagaimana caranya supaya kamu juga bisa menggunakan fitur yang telah dibuat teman mu ?. Caranya :
> git flow feature pull origin FITURSAYA

Kamu juga bisa mengecek atau melacak sebuah fitur berdasarkan asalnya dengan menggunakan :
> git flow feature track FITURSAYA


### Membuat Sebuah Rilis

#### Mulai sebuah rilis
Untuk memulai sebuah rilis, gunakan perintah *git flow release* . Perintah ini akan membuat sebuah *branch* rilis yang dibuat dari *branch* 'develop'
> git flow release start RELEASE [BASE]

Kamu bisa menambahkan opsi sebuah [BASE] commit sha-1 hash untuk memulai rilis dari. *Commit* harus berada dalam *branch* 'develop'.

Akan lebih bijak untuk mempublikasi *branch* rilis setelah membuatnya. Caranya sama dengan mempublikasi fitur, dengan perintah:
> git flow release publish RELEASE

Kamu bisa melacak sebuah rilis remot dengan perintah :
> git flow release track RELEASE)

### Menyelesaikan Sebuah rilis
Menyelesaikan sebuah rilis adalah sebuah langkah besar dalam git branching. Beberapa hal yang terjadi ketika menyelesaikan sebuah rilis :

* Merge branch rilis kembali ke 'master'
* Menandai (tags) rilis dengan namanya sendiri
* Merge rilis kembali ke dalam 'develop'
* Menghapus branch rilis

> git flow release finish RELEASE

Dan jangan lupa untuk melakukan push pada penanda (tags) anda dengan *git push --tags*

### Hotfixes

* Hotfixes muncul dari kebutuhan untuk melakukan tindakan sesegera mungkin atas keadaan yang tidak diinginan pada versi production
* Mungkin percabangan dari penanda (tag) yang sesuai dalam *branch* master yang ditandai sebagai versi production

#### git flow hotfix start
Seperti perintah git flow yang lain, sebuah hotfix dimulai dengan
> git flow hotfix start VERSION [BASENAME]

Argumen versi dengan ini menandai nama sebuah rilis hotfix baru. Dengan opsi anda dapat menspesifikasikan sebuah penamaan dasar untuk memulai.

#### Menyelesaikan sebuah hotfix
Dengan menyelesaikan sebuah *hotfix* ini berarti akan di-*merge* kembali ke dalam develop dan master. Sebagai tambahan merge ke master ditandai dengan *versi hotfix*.


#### Catatan

* Tidak semua perintah yang tersedia dapat mencakup semua, hanya yang paling penting saja
* Kamu masih bisa menggunakan git dan semua perintahnya secara normal seperti yang anda ketahui, git flow adalah hanya sebuah koleksi alat




## 2. Markdown
Markdown adalah satu bahasa yang diciptakan untuk mempermudah pembuatan dan pembacaan kode HTML. Markdown diciptakan dalam bahasa Perl. 

Format tulisan markdown sendiri adalah plain-text yang artinya kamu bisa membuat markdown dari text-editor biasa seperti notepad, sublime, emacs, vi, vi, dll. Lisensi markdown sendiri adalah opensource BSD.


#### Cara Membuat Dokumen Markdown
1. Pastikan Laptop atau Komputer sudah terinstall *perl*, kalo kamu belum install silakan kamu download [disini](http://strawberryperl.com/).
2. Kalo sudah terinstall , silakan kamu download libary markdown [disini](https://daringfireball.net/projects/downloads/Markdown_1.0.1.zip).
3. Buat file Markdown.
4. Compile file markdown dengan perintah perl Markdown.pl --html4tags file_mardown_kamu.md. Perintah tersebut akan menghasilkan output file html yang dapat kamu buka lewat browser.

Ribet ya?, tenang, kita punya cara yang lebih mudah dari cara diatas.

Caranya adalah dengan menggunkan Sublime Text 3. Dengan menggunakan Sublime Text 3 kamu bisa menggunakan Markdown dengan mudah, ikuti tutorial dbawah ini ya .
1. Buka Sublime Text 3. Jika belum download silahkan download dan install ST3 terlebih dahulu [disini](http://www.sublimetext.com/3).
2. Buka package manager dengan menggunakan perintah ```ctrl+shift+p```. Jika kamu belum memiliki package manager, install terlebih dahulu [disini](https://packagecontrol.io/installation).
3. Pilih menu Install Package.
4. Pilih plugin MarkdownEditing.
5. Buka lagi package manager.
6. Pilih Markdown Preview.
7. Untuk melihat hasil markdown dalam bentuk file html, kamu membuka konsol perintah dengan ```ctrl+shift+p``` kemudian kamu dapat memilih perintah Markdown Preview: Preview In Browser.
8. Browser akan terbuka untuk memperlihatkan hasil konversi markdown ke html.


#### Penggunaan Syntax 

##### Header

Untuk membuat sebuah header di markdown kamu hanya perlu menuliskan ```#``` kemudian diikuti dengan judul atau heading yang akan kamu buat, contohnya :
````
# Heading tag <h1>
## Heading tag <h2>
### Heading tag <h3>
#### Heading tag <h4>
##### Heading tag <h5>
###### Heading tag <h6>
````

##### Paragraf
Membuat paragraph di markdown sangat mudah, kamu tinggal mengetikan saja apa yang akan kamu ketik, kemudian tekan *enter* maka otomatis akan dikonversikan menjadi sebuah paragraf.

##### Unordered List
Unordered List atau daftar tak berurut, cara membuatnya adalah dengan mengunakan ```*``` kemudian diikuti dengan nama list atau daftar  , contohnya :
```
* List 1
* List 2
```
Syntax diatas akan menghasilkan :

* List 1
* List 2

#### Ordered List
Ordered List atau daftar terurut, cara membuatnya adalah dengan mengetikan ```spasi``` + ```enter```, contohnya :
```
1. List 1
2. List 2
```
Syntax diatas akan menghasilkan :
1. List 1
2. List 2

#### Bold
Efek Bold bisa kamu buat dengan menggunakan ```**```, contohnya:
```
**Bold**
```

Syntax diatas akan menghasilkan **Bold**.

#### Italic
Efek Italic bisa kamu buat dengan menggunakan ```*```, contohnya:
```
*Italic*
```

Syntax diatas akan menghasilkan *Italic*.

#### Blockquote
Blockquote dapat dibuat dengan syntax ```>``` diikuti dengan nama Blockquote nya, contohnya:
```
> ini adalah Blockquote saya
```

Syntax diatas akan menghasilkan 
> ini adalah Blockquote saya

#### Hyperlink
Membuat Hyperlink di markdown cukup mudah, caranya:
```
[Link Kamu](http://linkkamu.com).
```
Dan hasilya seperti ini [Link Kamu](http://linkkamu.com).

#### Horizontal Rule
Horizontal Rule bisa kamu buat dengan syntax ```---``` lalu ```enter```. Dan hasilnya sepert dibawah ini.

----

#### Table 
Untuk membuat sebuah table di Markdown, caranya dengan menyusun daftar kata dan membaginya dengan tanda hubung ```-``` (untuk baris pertama), kemudian untuk memisahkan setiap kolom adalah dengan menggunakan pipa ```|```.
Coba kamu perhatikan syntax dibawah ini.
```
Kolom Pertama | Kolom Kedua
------------ | -------------
Baris pertama dari kolom pertama | Baris pertama dari kolom kedua
Baris kedua dari kolom pertama | Baris kedua dari kolom pertama
```

Hasil syntax diatas :

Kolom Pertama | Kolom Kedua
------------ | -------------
Baris pertama dari kolom pertama | Baris pertama dari kolom kedua
Baris kedua dari kolom pertama | Baris kedua dari kolom pertama


## 3. ES6 Variable
Pada ES6 kita akan mengenal tiga syntax untuk mendeklarasikan sebuah variable. Tidak seperti pada ES5 kita hanya mengenal satu cara untuk mendeklarasikan sebuah variable. Lalu apa ketiga syntax baru tersebut?, dialah ```const, let dan var```. 

Ayo kita bahas satu-persatu, oke??.

#### Conts
const, singkatan constan, adalah kata kunci JavaScript yang mendeklarasikan sebuah variabel baru dengan nilai yang tidak dapat berubah. Artinya variabel yang kamu buat tidak akan bisa kamu ubah nilainya.

Untuk lebih jelasnya coba kamu perhatikan kode dibawah ini.
```
const contoh = 'belajar variable const';
console.log(contoh);
```


Jika kita jalankan kode diatas, maka akan muncul diconsole ```belajar variable const``` dan ini berjalan normal. Lalu bagaimana jadinya jika kita merubah variable ```contoh``` diatas??, perhatikan kode dibawah ini.

```
const contoh = 'belajar variable const';
console.log(contoh);
contoh = 'Saya sedang belajar variable const';
```

Maka akan dipastikan kita akan mendapatkan error seperti ini **TypeError: Assignment to constant variable**. Lah kenapa?, alasan nya adalah karena seperti yang sudah saya sampaikan sebelumya, bahwa sifat variable const adalah tidak dapat berubah. Yaaa seperti namanya, const dari kata konstan yang artinya tidak dapat berubah.

#### let
Tidak seperti ```const```, jenis variable ```let``` dapat kita ubah nilai variable nya.
Untuk lebih jelasnya coba lihat kode dibawah ini.
```
let contoh = 'belajar variable let';
contoh = 'kita ubah variable let';
console.log(contoh);
// output : kita ubah variable let
```

Pada kode diatas, kita berhasil merubah variable ```contoh``` menjadi ```kita ubah variable let```, yang sebelumnya ```belajar variable let```.

Tapi, ada yang perlu kita perhatikan. Syntax ```let``` bersifat **block scope**, artinya variable ```let``` hanya dapat diubah didalam suatu cakupan **scope**. Bingung?, Biar kode yang menjelaskan.
```
for (let i = 0; i < 10; i++) {
  console.log(i)
}
console.log(i) // this i is undefined
```

Pada saat kita menjalankan kode diatas kita akan mendapatkan error **ReferenceError: i is not defined**, padahal variable ```i``` sudah kita deklarasikan didalam perulangan  ```for```. Inilah yang saya maksud bahwa variabel ```let``` hanya dapat diubah didalam suatu cakupan **scope**. **Scope** disini maksudnya adalah tanda **{....}** ya.

#### var
Syntax ```var``` sama seperti variable let, yaitu sama-sama bisa kita ubah nilai variablenya. Bedanya adalah syntax ```var``` bersifat **function scope**.
Sekarang coba kita gunakan kode dibawah ini sebagai contohnya ya.
```
for (var i = 0; i < 10; i++) {
  console.log(i);
}
console.log(i) // this i = 10

```

Pada baris terakhir kode diatas akan menghasilkan keluaran berupa angka ```10```. Padahal kita mendekalarasikan variable ```i``` hanya pada perulangan ```for```. Dan inilah yang dimaksud dengan **function scope**, yang artinya variabel yang kita deklarasikan di dalam sebuah fungsi akan dapat kita gunakan asalkan masih dalam skope fungsi tersebut.


## 4. Template Literal
Pada Javascript non-ES6 ketika kita ingin menyisipkan atau menggabungkan konten atau variable ke dalam sebuah string , kita akan menggunakan tanda **+** sebagai penghubung.
Di ES6 kita dipermudah untuk menyisipkan atau menggabungkan konten atau variable ke dalam sebuah string, caranya adalah dengan menggunakan tanda **`(tombol ini biasanya terletak di bagian atas keyboard Anda, di sebelah kiri tombol 1)**(), kemudian setelah itu bungkus variable kita dengan cara **${namaVariable}**. Contohnya:
```
let namaSaya = 'Riko';
let kotaSaya = 'Bandar Lampung';
console.log(`Nama saya ${namaSaya}. Saya tinggal di ${kotaSaya}`);
// Output : Nama saya Riko. Saya tinggal di Bandar Lampung.
```

## 5. Named Argument
Arguments adalah nilai yang ditampung dari seluruh argument yang dikirimkan kepada sebuah fungsi. Pada Javascript ES5 penulisan argument adalah ```argument``` , namun pada Javascript ES6 penulisannya disingkat ```args```.

Terkadan ketika kita ngoding, kita sering salah melemparkan argumen ke sebuah fungsi. Misalnya:
```
// fungsi menerima 2 argumen
fungsi penjumlahan(a,b){
    return a+b;
}
// tapi kita malah mengrimkan 3 argumen
penjumlahan(1,2,3);
```

Pada syntax diatas kita tidak diperbolehkan mengirimkan argumen melebihi jumlah data yang telah ditentukan. 
Lalu bagaimana jika kita ingin mengirimkan argumen yang bersifat dinamis?, naa disinilah kita bisa menggunakan ```args```.
Contohnya:
```
function list (...args){
 return console.log(...args); // Laravel CI Yii
}
list("Laravel","CI","Yii");
```

```
function penjumlahan (a,...args){
    // kita bisa membaca argument dengan metode array
    return a+args[0]+args[1]; // 9
}
// 2 adalah argument yang terdaftar pada a, 
// sedangkan 3,4 terdaftar ke 'args'
sum(2,3,4);
```






















