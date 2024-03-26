# <h1 align="center">Laporan Praktikum Modul Tipe Data</h1>
<p align="center">Arvinanto Bahtiar</p>

## Dasar Teori

Linked list adalah strukur data linier berbentuk rantai simpul di mana setiap simpul menyimpan 2 item, yaitu nilai data dan pointer ke simpul elemen berikutnya. Berbeda dengan array, elemen linked list tidak ditempatkan dalam alamat memori yang berdekatan melainkan elemen ditautkan menggunakan pointer. Ukuran elemen dari linked list dapat bertambah secara dinamis dan mudah untuk menyisipkan dan menghapus elemen karena tidak seperti array, kita hanya perlu mengubah pointer elemen sebelumnya dan elemen berikutnya untuk menyisipkan atau menghapus elemen.

Kelebihan menggunakan Linked list adalah himpunan dinamis sehingga dapat bertambah dan menyusut saat runtime dengan mengalokasikan dan membatalkan alokasi memori. Jadi kita tidak perlu memberikan ukuran awal dari linked list. Dalam linked list, pemanfaatan memori yang efisien dapat dicapai karena ukuran linked list bertambah atau berkurang pada runtime sehingga tidak ada pemborosan memori dan tidak perlu mengalokasikan memori sebelumnya. Struktur data linier seperti stack dan queue seringkali mudah diimplementasikan menggunakan linked list. Operasi penyisipan dan penghapusan cukup mudah dalam linked list. Kita tidak perlu menggeser elemen setelah operasi penyisipan atau penghapusan elemen, hanya alamat yang ada di pointer berikutnya saja yang perlu diperbarui.

Adapun kekurangan Linked list memerlukan lebih banyak memori dibandingkan dengan array. Karena dalam linked list, pointer juga perlu menyimpan alamat elemen berikutnya dan membutuhkan memori tambahan untuk dirinya sendiri. Dalam traversal, linked list lebih banyak memakan waktu dibandingkan dengan array. Akses langsung ke elemen tidak bisa dilakukan pada linked list seperti array yang dapat akses elemen berdasarkan indeks. Untuk mengakses sebuah simpul pada posisi n dari linked list, kita harus melintasi semua simpul sebelumnya. Dalam single linked list, reverse traversing tidak dimungkinkan, tetapi dalam kasus double-linked list, ini dapat dimungkinkan karena berisi pointer ke node yang terhubung sebelumnya dengan setiap node. Untuk melakukannya, diperlukan memori tambahan untuk pointer sebelumnya sehingga ada pemborosan memori. Akses acak tidak bisa dilakukan dalam linked list karena alokasi memorinya yang dinamis.

### Single Linked List

Single Linked List adalah sebuah field pointer-nya hanya satu buah saja dan satu arah serta pada akhir node yang nodenya saling terhubung satu sama lain. Jadi Setiap node pada linked list mempunyai field yang berisi pointer ke node berikutnya, dan juga memiliki field yang berisi data. Node terakhir akan menunjuk ke NULL yang akan digunakan sebagai kondisi berhenti pada saat pembacaan isi linked list.

Untuk membuat Single Linked List dalam Pemrograman C++ diperlukan sebuah Struct untuk menbuat sebuah Node berikut Syntax pembuatan Node pada Pemrograman C++ :

```C++
struct TNode{
    int data;
    struct TNode *next;
};
```
Pada Syntax Tersebut Pembuatan struct bernama TNode yang berisi 2 field, yaitu field data bertipe integer dan field next yang bertipe pointer dari Tnode Setelah pembuatan struct, buat variabel head yang bertipe pointer dari SNode yang berguna sebagai kepala linked list.

Struct adalah sebuah structure dalam ANSI/C digunakan untuk membuat tipe data yang terdiri dari beberapa anggota (member) dengan tipe tertentu. berbeda dengan array hanya berupa kumpulan variabel yang bertipe data sama. struct bisa memiliki variabel-variabel yang bertipe data sama atau berbeda, bahkan bisa menyimpan variabel yang bertipe data array atau struct itu sendiri. Variabel-variabel yang menjadi anggota struct disebut dengan elemen struct.

Untuk melakukan inisialisasi Node baru pada pemrograman C++ gunakan keyword new yang berarti mempersiapkan sebuah node baru berserta alokasi memorinya, kemudian node tersebut diisi data dan pointer nextnya ditunjuk ke NULL. Berikut contohnya :

```C++
TNode *baru
baru = ne TNode;
baru->data = databaru;
baru->next = NULL;
```

Pada Single Linked List biasanya menggunakan Head. Head yang dimaksud ini adalah Kepala dari Single Linked List. Jadi dalam pemrograman diperlukan sebuah variabel pointer head untuk mebuat head Single Linked List. Head akan selalu menunjukkan Node Pertama seperti gambar berikut :

![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/dc977ed1-2239-4099-a449-ef2da2e38ebb)

Dengan menggunakan struktur seperti ini, linked list dibentuk dengan cara menunjuk pointer next suatu elemen ke elemen yang
mengikutinya. Pointer next pada elemen terakhir merupakan NULL, yang menunjukkan akhir dari suatu list. Elemen pada awal suatu list disebut head dan elemen terakhir dari suatu list disebut tail.

### Double Linked List

Pada dasarnya, penggunaan Double Linked List hampir sama dengan penggunaan Single Linked List yang telah kita pelajari pada materi sebelumnya. Hanya saja Double Linked List menerapkan sebuah pointer baru, yaitu prev, yang digunakan untuk menggeser mundur selain tetap mempertahankan pointer next. Double linked list terdiri dari elemen-elemen individu, dimana masing-masing
dihubungkan dengan dua pointer. Masing-masing elemen terdiri dari tiga bagian, yaitu sebuah data dan sebuah pointer yang berisi alamat data berikutnya disebut dengan next dan pointer yang berisi alamat data sebelumnya disebut before. Dengan menggunakan struktur two-member seperti ini, linked list dibentuk dengan cara menunjuk pointer next suatu elemen ke elemen yang mengikutinya. Pointer before pada elemen terakhir merupakan NULL, yang menunjukkan awal dari suatu list. Pointer next pada elemen terakhir merupakan NULL, yang menunjukkan akhir dari suatu list. 

![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/18c52c0c-3b92-4a5e-a07f-c4d4538ca646)

Double linked list dibentuk dengan menyusun sejumlah elemen sehingga pointer next menunjuk ke elemen yang mengikutinya dan pointer back menunjuk ke elemen yang mendahuluinya. Info adalah data yang digunakan dalam simpul, back adalah pointer yang menunjuk pada simpul sebelumnya, dan next adalah pointer yang menunjuk pada simpul sesudahnya.

![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/256c9586-83d2-43b5-8974-7a28d68b1549)


## Guided 

### 1. Latihan Single Linked List

```C++
#include <iostream>
using namespace std;

int main() {
    cout << "ini adalah file code guided praktikan" << endl;
    return 0;
}
```
Program ini merupakan implementasi dari single linked list non-circular dalam bahasa C++. Program ini memungkinkan pengguna untuk menambahkan node baru di depan atau belakang linked list, menghapus node pertama atau terakhir, menambahkan node pada posisi tengah tertentu, menghapus node pada posisi tengah tertentu, serta mengubah nilai data dari node pertama, terakhir, atau pada posisi tengah tertentu. Setiap node dalam linked list menyimpan nilai data integer, dan fungsi-fungsi yang disediakan dalam program memungkinkan manipulasi linked list sesuai kebutuhan pengguna. Program tersebut juga menyediakan fungsi untuk menghitung jumlah node dalam linked list, membersihkan seluruh linked list, serta menampilkan nilai data dari semua node dalam linked list. Program diuji melalui serangkaian operasi untuk memastikan fungsionalitasnya sesuai dengan yang diharapkan.

### 2. Latihan Double Linked List

```C++
#include <iostream>
using namespace std;

int main() {
    cout << "ini adalah file code guided praktikan" << endl;
    return 0;
}
```
Program ini adalah implementasi dari Double Linked List dalam bahasa C++. Dalam program ini, terdapat dua kelas utama kelas Node yang merepresentasikan node dalam linked list, dan kelas DoublyLinkedList yang merepresentasikan linked list itu sendiri. Setiap node memiliki tiga anggota: data yang menyimpan nilai data, prev yang merupakan pointer ke node sebelumnya, dan next yang merupakan pointer ke node berikutnya. Kelas DoublyLinkedList memiliki anggota head dan tail yang merupakan pointer ke node pertama dan terakhir dalam linked list. Fungsi push digunakan untuk menambahkan data baru di depan linked list, fungsi pop digunakan untuk menghapus data dari depan linked list, fungsi update digunakan untuk mengubah nilai data tertentu dalam linked list, fungsi deleteAll digunakan untuk menghapus seluruh data dalam linked list, dan fungsi display digunakan untuk menampilkan seluruh data dalam linked list. Program ini memberikan pilihan kepada pengguna untuk menambahkan, menghapus, mengubah, menghapus semua, menampilkan data, atau keluar dari program melalui menu yang disediakan.

## Unguided 

### 1. Soal mengenai Single Linked List

Buatlah program menu Single Linked List Non-Circular untuk
menyimpan Nama dan usia mahasiswa, dengan menggunakan inputan
dari user. Lakukan operasi berikut:

a. Masukkan data sesuai urutan berikut. (Gunakan insert depan,
belakang atau tengah). Data pertama yang dimasukkan adalah
nama dan usia anda.

[Nama_anda] [Usia_anda]
    John        19
    Jane        20
    Michael     18
    Yusuke      19
    Akechi      20
    Hoshino     18
    Karin       18

b. Hapus data Akechi
c. Tambahkan data berikut diantara John dan Jane : Futaba 18
d. Tambahkan data berikut diawal : Igor 20
e. Ubah data Michael menjadi : Reyn 18
f. Tampilkan seluruh data

```C++
#include <iostream>
using namespace std;

int main() {
    cout << "ini adalah file code unguided praktikan" << endl;
    return 0;
}
```
#### Output:

![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/3c5b87c6-b8aa-45be-9804-9600c4cb0986)

![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/21fbd3b8-ef6e-4a5c-b84e-08c5fa7fa914)

![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/75081d7b-5c00-4b07-b83a-b6311ab4133e)

Program diatas akan meminta pengguna untuk memasukkan data mereka sendiri, yang akan menjadi data pertama dalam linked list (nama dan usia). Kemudian, program akan secara otomatis menambahkan data mahasiswa lain yang telah ditentukan ke dalam linked list. Pengguna dapat memilih berbagai operasi seperti menampilkan data, menghapus data, menambahkan data di tengah atau di awal, mengubah data, atau keluar dari program melalui menu yang disediakan. Misalnya, jika pengguna memilih untuk menambahkan data di tengah, program akan meminta nama, usia, dan posisi tempat penambahan data. Kemudian, program akan menambahkan data tersebut ke dalam linked list pada posisi yang ditentukan. Setiap operasi akan diproses sesuai dengan pilihan pengguna, dan data akan ditampilkan dengan format nama dan usia. Program akan terus berjalan hingga pengguna memilih untuk keluar.


### 2. Soal mengenai Double Linked List

Modifikasi Guided Double Linked List dilakukan dengan penambahan
operasi untuk menambah data, menghapus, dan update di tengah / di
urutan tertentu yang diminta. Selain itu, buatlah agar tampilannya
menampilkan Nama produk dan harga.

[Nama Produk]    [Harga]

Originote        60.000

Somethinc        150.000

Skintific        100.000

Wardah           50.000

Hanasui          30.000

Case:
1. Tambahkan produk Azarine dengan harga 65000 diantara
Somethinc dan Skintific
2. Hapus produk wardah
3. Update produk Hanasui menjadi Cleora dengan harga 55.000
4. Tampilkan menu seperti dibawah ini
Toko Skincare Purwokerto
1. Tambah Data
2. Hapus Data
3. Update Data
4. Tambah Data Urutan Tertentu
5. Hapus Data Urutan Tertentu
6. Hapus Seluruh Data
7. Tampilkan Data
8. Exit

Pada menu 7, tampilan akhirnya akan menjadi seperti dibawah
ini :

[Nama Produk]    [Harga]
Originote        60.000
Somethinc        150.000
Azarine          65.000
Skintific        100.000
Cleora           55.000

```C++
#include <iostream>
using namespace std;

int main() {
    cout << "ini adalah file code unguided praktikan" << endl;
    return 0;
}
```
#### Output:
![240302_00h00m06s_screenshot](https://github.com/suxeno/Struktur-Data-Assignment/assets/111122086/6d1727a8-fb77-4ecf-81ff-5de9386686b7)

Program di atas adalah implementasi dari aplikasi manajemen data produk skincare menggunakan Double Linked List dalam bahasa C++. Setiap node memiliki atribut nama_produk untuk menyimpan nama produk dan harga untuk menyimpan harga produk. Selain itu, setiap node memiliki pointer prev yang menunjukkan ke node sebelumnya dalam linked list, dan next yang menunjukkan ke node berikutnya. Kelas Linked List merepresentasikan linked list produk skincare. Setiap linked list memiliki satu pointer head yang menunjukkan ke node pertama dalam linked list. Program utama memungkinkan pengguna untuk melakukan berbagai operasi. Menu operasi mencakup menambah data, menghapus data, mengubah data, menambah data pada posisi tertentu, menghapus data pada posisi tertentu, menghapus seluruh data, menampilkan data, dan keluar dari program.

## Kesimpulan
Ringkasan dan interpretasi pandangan kalia dari hasil praktikum dan pembelajaran yang didapat[1].

## Referensi
[1] I. Holm, Narrator, and J. Fullerton-Smith, Producer, How to Build a Human [DVD]. London: BBC; 2002.