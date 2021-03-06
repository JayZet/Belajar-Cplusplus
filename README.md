# Apa itu C++
C++ adalah sebuah bahasa pemrograman yang dikembangkan dari bahasa C oleh Bjarne Stroustrup pada tahun 1980 an di Bell Labs. Salah satu kelebihan bahasa C++ dibandingkan bahasa C adalah dukungan terhadap konsep PBO (Pemrograman Berorientasi Objek)



# Table Konten : 
* [Sintak Dasar](#sintak-dasar)
* [Komentarin Sourcenya yuk biar tidak bingung](#komentar)
    * [Komentar sebaris](#komentar-sebaris)
    * [komentar lebih dari 1 baris](#komentar-lebih-dari-sebaris)
* [Tipe Data](#tipe-data)
* [Deklarasi Variabel](#deklarasi-variabel)
    * [Deklarasi Konstanta](#deklarasi-konstanta)

## Sintak Dasar
Untuk menulis kode program dengan C++ ada sintak dasarnya, dimana sintak tersebut sangatlah penting agar program dapat berjalan, karena jika tidak ada maka program tidak dapat berjalan sama sekali, atau bahkan error. Sintak dasarnya seperti ini :

    #include<iostream>
    using namespace std;

    int main(){

    }

Penjelasan kode :

    #include<iostream> 
    
 C++ melampirkan beberapa header dengan cara #include<file_header_yang_ingin_ditampilkan>,
oh iya #include itu termasuk preprocessor dan #include ini berguna untuk memanggil atau menambahkan file header.
setiap File header memiliki fungsi dan kegunaan tertentu salah satunya adalah iostream. 
iostream adalah library standar untuk melakukan operasi input maupun output dalam program 
yang kita tulis, salah satu sintak untuk melakukan input dan output adalah cin 
dan cout dimana cin adalah sintak untuk melakukan input dari keyboard dan
cout adalah sintak untuk mencetak kode program agar dapat tampil dilayar.
berikut ini adalah contoh sederhana dari input dan output program paling sederhana : 

<img src="https://github.com/NurcahyaAri/Belajar-Cplusplus/blob/master/images/basic%20input%20output%20.gif" alt="alt text" width="510px" height="267px" alt="input output sederhana" title="input output sederhana">

    using namespace std;

 untuk menggunakan standar library dari C++ maka kita harus menuliskan kode tersebut, karena jika tidak 
 dituliskan maka program yang kita buat akan error.

    int main(){

    }
 
terakhir adalah int main(), int main() sendiri adalah fungsi utama dalam program c++. setiap kode program yang ditulis akan dipanggil disini, jadi ketika program kalian jalankan maka semua baris yang ada di fungsi main inilah yang nantinya akan diproses, tetapi jika kalian menulis kode diluar main() dan tidak dipanggil didalam fungsi ini maka kode tersebut tidak akan diproses sama sekali


## Komentar
Ketika kita sudah menulis sebuah kode program terkadang kita juga bingung apa yang sudah kita tulis, atau kita malah lupa bagaimana proses program tersebut berjalan, dan juga kita sering kali lupa dan bertanya tanya "mengapa kita buat programnya seperti ini ya? gunanya sebenernya apa ini?" nah dengan adanya komentar ini kita dapat mengomentari kegunaan dari baris program yang sudah kita buat agar kita tidak bingung, selain itu komentar juga biasa digunakan untuk menulis lisensi program atau pengarang program tersebut. berikut ini adalah contoh komentar
<img src="https://github.com/NurcahyaAri/Belajar-Cplusplus/blob/master/images/komentar.png" alt="alt text" alt="input output sederhana" title="input output sederhana">

disitu terlihat jelas bahwa komentar tidak akan ikut tampil ketika program dijalankan. oh iya komentar ada dua jenis, yaitu : 

### komentar sebaris
ketika kita hanya ingin mengomentari hanya satu baris program maka kita dapat menggunakan komentar jenis ini cara penggunaannya seperti ini
    // text yang ingin dijadikan komentar

### komentar lebih dari sebaris
sedangkan ketika kita ingin mengomentari 2 baris atau 3 atau mungkin 10 baris kita juga bisa, untuk mengomentari lebih dari 10 baris caranya seperti ini
    /* Nama saya Ari Nurcahya
       Saya bingun mau nulis apa lagi
       Saya suka kucing, dan juga suka Dia
    */
untuk komentar lebih dari 1 baris kita mulai dengna /* kemudian ditutup dengan */

# Tipe Data
Tipe data adalah pengenal untuk suatu variabel, tipe data ini akan memberitahukan kepada compiler mengenai tipe data apa yang dipakai dan seberapa lebar compiler mengalokasikan ruang memori kepada suatu variabel.

| Tipe Data | Deskripsi | Ukuran Memori | Jangkauan |
|-----------|-----------|---------------|-----------|
| int       | Bilangan Bulat| 2 Byte    | -32768 hingga 32768|
| short int | sama dengan int namun jangkauan nya lebih pendek| 2 Byte | -32768 hingga 32768 |
| Long int | Memiliki jangkauan lebih panjang dari int | 4 Byte | -2147483648 hingga 2147483648 |
| bool | Tipe data untuk menampung nilai kebenaran (True or False) defaultnya adalah false | 1 Byte | False or True |
| float | bilangan pecahan atau koma | 4 Byte | 3,4x10^-308 hingga 1,7x10^+308 |
| double | sama dengan float, namun jangkauannya 2 kali dari float | 8 Byte | 1,7x10^-308 hingga 1,7x10^+308 |
| long double | sama dengan double, tetapi jangkaunnya lebih lebar | 10 Byte | 3,4x10^-4932 hingga 3,4x10^+4932 |
| char | Menampung tipe karakter | 1 Byte | -128 hingga 128 |
| wchar_t | sama dengan char, namun jangkauannya lebih lebar | 2 hingga 4 Byte | 1 wide karakter |
    
# Deklarasi Variabel
Variabel adalah suatu data yang nilainya dapat berubah-ubah. Variabel sangat erat kaitanya dengan tipe data, karna keberadaan suatu data perlu ditentukan tipe datanya untuk pengenalan prosesor dalam mengolah data tersebut. yuk langsung ke contoh aja ya:

```cpp
int a;
float b;
```
Nah berdasarkan cakupannya, variabel dibagi menjadi dua, global dan local variabel. Variabel global merupakan variabel yang dapat digunakan disemua kode program. Variabel ini dapat dipanggil dimanapun dari bagian suatu program. Sedangkan variabel lokal adalah variabel yang hanya berlaku pada suatu fungsi tertentu saja dan variabel tersebut tidak berdampak pada variabel diluar fungsi. Biar lebih paham, yuk langsung simak contohnya:
```cpp
#include<iostream>
using namespace std;
int a; // ini adalah variabel global

int main(){
int b = 29; // ini adalah variabel lokal
return 0;
}
```
## Deklarasi Konstanta
Konstanta merupakan variabel yang memilki nilai tetap, tidak dapat dilakukan perubahan. Ada 2 cara untuk mendeklarasikan variabel konstanta, yuk perhatikan:
1. Menggunakan const
```cpp
const float phi = 3.14;
const char karakter = 'a';
```
2. Dengan menggunakan preposesor #define
```cpp
#define maks = 10;
```
pada proses pendeklarasian dengan menggunakan preposesor, kamu gak perlu mendeklarasikan tipe data variabel konstanta tersebut.

# Bermain dengan Matematika di C++
```
5*2 = 10
x+y;
1/2*x+y;
```
Nah di atas itu adalah contoh sederhana dari perhitungan matematika. Perhitungan dalam matematika sendiri sudah pasti ada nilai(operand), operasinya(operator) dan hasilnya. Di dalan pemrograman juga kurang lebih akan seperti itu.Yuk langsung ke study kasus :D

JayZet mempunyai uang sebesar 50k, kemudian JayZet membeli nastel sebesar 10k, berapakah sisa uang JayZet? mari selesaikan dengan c++ (harga makanannya dalam inputan user)
```cpp
#include <iostream>
using namespace std;
int main(){
int my_money = 50000;
int nastel;

cout << "masukkan harga nastel: ";
cin >> nastel; //kita masukkan harga nastel 10000

my_money = my_money - nastel;

cout<<"jumlah uang kita sekarang adalah"<<my_money<<endl; //ouputnya adalah 40000
```
Study Kasus yang kedua, kita akan mencoba menghitung luas lingkaran dengan jari-jari 7cm.
Analisa variabel yang akan digunakan, r -> untuk jari-jari, hasil -> untuk menampung hasil dan rumus, dan terakhir variabel konstanta untuk phi, phi = 3.14, kemudian terakhir akan kita hitung dengan rumus phi*r*r.

```cpp
#include <iostream>
using namespace std;
int main(){
float r, hasil;
const float phi = 3.14; //bisa juga langsung float phi = 3.14; 
r = 7;
hasil = phi*r*r;
cout << "Luas lingkaran adalah: " <<hasil<<endl;
```
nah kenapa variabel r dan hasil bertipe float? karena kemungkinan dari hasilnya akan bertipe pecahan, makanya kita menggunakan tipe data float. Nilai phi kita gunakan const yang artinya nilai phi tidak mungkin diubah.

## Operator Aritmatika
| operator | Nama | Kegunaan |
-----------|------|----------|
| + | Penjumlahan | untuk melakukan operasi penjumlahan |
| - | pengurangan | untuk melakukan operasi pengurangan |
| * | Perkalian | untuk melakukan operasi perkalian |
| / | pembagian | untuk melakukan operasi pembagian |
| % | modulus | untuk melakuakn operasi modulus atau sisa bagi|

