)# <h1 align="center">Laporan Praktikum Modul Array</h1>
<p align="center">Lailatur Rahmah</p>

## Dasar Teori
Dalam beberapa literatur, array sering disebut (diterjemahkan) sebagai larik. Array
adalah kumpulan dari nilai-nilai data bertipe sama dalam urutan tertentu yang
menggunakan sebuah nama yang sama. Nilai-nilai data di suatu array disebut dengan
elemen-elemen array. Letak urutan dari elemen-elemen array ditunjukkan oleh suatu
subscript atau indeks.
Array bisa berupa array berdimensi satu, dua, tiga atau lebih. Array berdimensi
satu (one-dimensional array) mewakili bentuk suatu vektor. Array berdimensi dua (twodimensional array) mewakili bentuk dari suatu matriks atau table. Array berdimensi tiga
(three-dimensional array) mewakili bentuk suatu ruang. 

Array adalah suatu struktur yang terdiri dari sejumlah elemen yang memiliki tipe data yang sama. Elemen-elemen array tersusun secara sekuensial dalam memori komputer. Semua elemem array bertipe sama. Array cocok untuk organisasi kumpulan data homogen yang ukuran atau jumlah elemen maksimumnya telah diketahui dari awal. Homogen adalah bahwa setiap elemen dari sebuah array tertentu haruslah mempunyai tipe data yang sama. 

#### ARRAY BERDIMENSI SATU
Array satu dimensi tidak lain adalah kumpulan elemen-elemen identik tersusun dalam satu baris. Elemen-elemen tersebut dapat berbeda. Petunjuk indeks hanya satu.

tipe_data nama_var[ukuran];

Keterangan:
tipe_data : untuk menyatakan tipe dari elemen array, misalnya int, char, float.

nama_var : nama variabel array

ukuran : untuk menyatakan jumlah maksimal elemen array

Contoh pendeklarasian array : 
```C++
float nilai_tes[5];
```
Mengakses Elemen Array Berdimensi Satu

Pada C, data array akan disimpan dalam memori yang berurutan. Elemen pertama
mempunyai indeks bernilai 0. Jika variabel nilai_tes dideklarasikan sebagai array dengan
5 elemen, maka elemen pertama memiliki indeks sama dengan 0, dan elemen terakhir
memiliki indeks 4. 

Inisialisasi Array Berdimensi Satu 

Sebuah array dapat diinisialisasi sekaligus pada saat dideklarasikan. Untuk
mendeklarasikan array, nilai-nilai yang diinisialisasikan dituliskan di antara kurung
kurawal ({}) yang dipisahkan dengan koma. 

```C++
int jum_hari[12] =
{31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};  
```
#### ARRAY BERDIMENSI DUA

Array berdimensi satu dapat disimpan pada sebuah array berdimensi dua.
Pendeklarasian array berdimensi dua adalah sebagai berikut : 

```C++
int data_lulus[4][3];   
```
Nilai 4 untuk menyatakan banyaknya baris dan 3 menyatakan banyaknya kolom. Gambar
10.1 memberikan ilustrasi untuk memudahkan pemahaman tentang array berdimensi dua. 

Mengakses Elemen Array Berdimensi Dua
Array seperti data_lulus dapat diakses dalam bentuk data_lulus[indeks pertama, indeks
kedua] : 

(1) data_lulus[0][1] = 540;
merupakan instruksi untuk memberikan nilai 540 ke array data_lulus untuk indeks
pertama = 0 dan indeks kedua bernilai 1.

(2) printf(“%d”,data_lulus[2][0]);
merupakan perintah untuk menampilkan elemen yang memiliki indeks pertama = 2 dan
indeks kedua = 0.
Perhatikan contoh potongan program di bawah ini. 

```C++
/* Memberikan data ke array */

    data_lulus[0][0] = 80;
    data_lulus[0][1] = 540;
    data_lulus[0][2] = 1032;

    INT HURUF_A[8][8] = {
            { 0, 1, 1, 1, 1, 1, 0, 0 } ,
            { 0, 1, 0, 0, 0, 1, 0, 0 } ,
            { 0, 1, 0, 0, 0, 1, 0, 0 } ,
            { 1, 1, 1, 1, 1, 1, 1, 0 } ,
            { 1, 1, 0, 0, 0, 0, 1, 0 } ,
            { 1, 1, 0, 0, 0, 0, 1, 0 } ,
            { 1, 1, 0, 0, 0, 0, 1, 0 } ,
            { 0, 0, 0, 0, 0, 0, 0, 0 }
}; 
```
#### ARRAY MULTIDIMENSI

C++ memungkinkan untuk membuat array yang dimensinya lebih dari dua. Bentuk umum pendeklarasian array berdimensi banyak : 

tipe nama_var[ukuran 1][ukuran2]…[ukuranN]; 

```C++
int data_huruf[2][8][8];  
```
Contoh inisialisasi array berdimensi tiga : 

```C++
int data_huruf [2][8][8] =
    { { { 0, 1, 1, 1, 1, 1, 0, 0 } ,
        { 0, 1, 0, 0, 0, 1, 0, 0 } ,
        { 0, 1, 0, 0, 0, 1, 0, 0 } ,
        { 1, 1, 1, 1, 1, 1, 1, 0 } ,
        { 1, 1, 0, 0, 0, 0, 1, 0 } ,
        { 1, 1, 0, 0, 0, 0, 1, 0 } ,
        { 1, 1, 0, 0, 0, 0, 1, 0 } ,
        { 0, 0, 0, 0, 0, 0, 0, 0 }
     },
     { 
        {1, 1, 1, 1, 1, 1, 0, 0 } ,
        {1, 0, 0, 0, 0, 1, 0, 0 } ,
        {1, 0, 0, 0, 0, 1, 0, 0 } ,
        {1, 1, 1, 1, 1, 1, 1, 0 } ,
        {1, 1, 0, 0, 0, 0, 1, 0 } ,
        {1, 1, 0, 0, 0, 0, 1, 0 } ,
        {1, 1, 1, 1, 1, 1, 1, 0 } ,
        {0, 0, 0, 0, 0, 0, 0, 0 }
      } };  
```

## Guided 

### 1. Program Input Array Tiga Dimensi

```C++
#include <iostream>

using namespace std;
// program input array 3 dimensi
int main()
{
    // deklarasi array
    int arr[2][3][3];
    // input elemen
    for (int x = 0; x < 2; x++)
    {
        for (int y = 0; y < 3; y++)
        {
            for (int z = 0; z < 3; z++)
            {
                cout << "Input Array[" << x << "][" << y << "][" << z << "]: ";
                cin >> arr[x][y][z];
            }
        }
        cout << endl;
    }
    // output array
    for (int x = 0; x < 2; x++)
    {
        for (int y = 0; y < 3; y++)
        {
            for (int z = 0; z < 3; z++)
            {
                cout << "Array[" << x << "][" << y << "][" << z << "]: " << arr[x][y][z] << endl;
            }
        }
    }
    cout << endl;
    // tampilan array
    for (int x = 0; x < 2; x++)
    {
        for (int y = 0; y < 3; y++)
        {
            for (int z = 0; z < 3; z++)
            {
                cout << arr[x][y][z] << ends;
            }
            cout << endl;
        }
        cout << endl;
    }
    return 0;
}
```
#### Output:
![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/3dc06397-2d41-40f4-9969-309666657cbb)
![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/6d53de4d-bec6-4c8c-acad-c086dde07876)

### 2. Program Mencari Nilai Maksimal pada Array 

```C++
#include <iostream> 
using namespace std; 

int main() { 
    int maks, a, i = 1, lokasi; 
    cout << "Masukkan panjang array: "; 
    cin >> a; 
    int array[a]; 
    
    cout << "Masukkan " << a << " angka\n"; 
    for (i = 0; i < a; i++) { 
        cout << "Array ke-" << (i) << ": "; 
        cin >> array[i]; 
    } 
    
    maks = array[0]; 
    for (i = 0; i < a; i++) { 
        if (array[i] > maks) { 
            maks = array[i]; 
            lokasi = i; 
        } 
    } 
    
    cout << "Nilai maksimum adalah " << maks << " berada di Array ke " << lokasi << endl; 

    return 0; 
}
```
#### Output:
![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/27bd3b60-7bed-483f-b9d0-124d30214a91)

## Unguided 

### 1. Buatlah program untuk menampilkan Output seperti berikut dengan data yang diinputkan oleh user! 

![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/bb267499-c690-441e-953d-155591a52394)

```C++
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> data_array;
    int num;
    
    cout << "Masukkan 10 angka dalam array:\n";
    for (int i = 0; i < 10; ++i) {
        cout << "Angka ke-" << i+1 << ": ";
        cin >> num;
        data_array.push_back(num);
    }

    cout << "Data array: ";
    for (int i = 0; i < data_array.size(); ++i) {
        cout << data_array[i];
        if (i != data_array.size() - 1)
            cout << " ";
    }
    cout << "\n";

    cout << "Nomor genap: ";
    for (int i = 0; i < data_array.size(); ++i) {
        if (data_array[i] % 2 == 0) {
            cout << data_array[i];
            if (i != data_array.size() - 1)
                cout << ", ";
        }
    }
    cout << "\n";

    cout << "Nomor ganjil: ";
    for (int i = 0; i < data_array.size(); ++i) {
        if (data_array[i] % 2 != 0) {
            cout << data_array[i];
            if (i != data_array.size() - 1)
                cout << ", ";
        }
    }
    cout << "\n";

    return 0;
}
```
#### Output:
![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/dae9ce01-ea4e-4b3d-9f49-3e399abacee6)

Program C++ di atas memungkinkan pengguna untuk memasukkan sepuluh angka ke dalam sebuah vektor, kemudian program akan menampilkan angka-angka tersebut kemudian memisahkan antara angka genap dan angka ganjil. Dengan menggunakan perulangan `for`, program mampu menampilkan data array dalam satu baris. Program memeriksa setiap angka dalam vektor untuk menentukan apakah itu genap atau ganjil, dan kemudian menampilkan angka-angka tersebut dalam kelompok yang sesuai. Program ini menunjukkan cara untuk memproses dan memisahkan data dengan mudah dan efisien.

### 2. Buatlah program Input array tiga dimensi (seperti pada guided) tetapi jumlah atau ukuran elemennya diinputkan oleh user! 

```C++
#include <iostream>

using namespace std;

int main() {
    int x_ukuran, y_ukuran, z_ukuran;

    // Meminta pengguna untuk memasukkan ukuran array
    cout << "Masukkan ukuran array (x y z): ";
    cin >> x_ukuran >> y_ukuran >> z_ukuran;

    // Deklarasi array dengan ukuran yang dimasukkan pengguna
    int arr[x_ukuran][y_ukuran][z_ukuran];

    // Input elemen array
    for (int x = 0; x < x_ukuran; ++x) {
        for (int y = 0; y < y_ukuran; ++y) {
            for (int z = 0; z < z_ukuran; ++z) {
                cout << "Input Array[" << x << "][" << y << "][" << z << "]: ";
                cin >> arr[x][y][z];
            }
        }
        cout << endl;
    }

    // Output array
    cout << "Elemen-elemen array:" << endl;
    for (int x = 0; x < x_ukuran; ++x) {
        for (int y = 0; y < y_ukuran; ++y) {
            for (int z = 0; z < z_ukuran; ++z) {
                cout << "Array[" << x << "][" << y << "][" << z << "]: " << arr[x][y][z] << endl;
            }
        }
    }
    cout << endl;
// tampilan array
    for (int x = 0; x < x_ukuran; x++)
    {
        for (int y = 0; y < y_ukuran; y++)
        {
            for (int z = 0; z < z_ukuran; z++)
            {
                cout << arr[x][y][z] << ends;
            }
            cout << endl;
        }
        cout << endl;
    }


    return 0;
}
```
#### Output:
![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/f1bcda10-c812-4567-84d6-06d3793aed2d)
![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/0d7df01e-cfa1-4a14-afc0-9cdcdad75853)

Program ini adalah sebuah program C++ yang dapat menginputkan ukuran array tiga dimensi (x, y, z), kemudian mengisi elemen-elemennya, dan menampilkannya kembali. Setelah semua elemen dimasukkan, program menampilkan elemen-elemen array dengan mencetak setiap elemen beserta indeksnya. Selain itu, program juga menampilkan elemen-elemen array tanpa struktur dimensi, yaitu dengan mencetak semua elemen dalam satu baris tanpa pemisah, memungkinkan pengguna untuk melihat data array secara kontinu. Program ini memberikan pengguna kontrol atas ukuran dan isi array tiga dimensi.

### 3. Buatlah program menu untuk mencari nilai Maksimum, Minimum dan Nilai rata – rata dari suatu array dengan input yang dimasukan oleh user! 

```C++
#include <iostream>
#include <vector>

using namespace std;

int main() {
    int n;

    cout << "Masukkan panjang array: ";
    cin >> n;

    vector<int> arr(n);
    cout << "Masukkan elemen array:\n";
    for (int i = 0; i < n; ++i) {
        cout << "Elemen ke-" << i+1 << ": ";
        cin >> arr[i];
    }

    int maksimum = arr[0];
    for (int i = 1; i < n; ++i) {
        if (arr[i] > maksimum) {
            maksimum = arr[i];
        }
    }

    int minimum = arr[0];
    for (int i = 1; i < n; ++i) {
        if (arr[i] < minimum) {
            minimum = arr[i];
        }
    }

    double total = 0;
    for (int i = 0; i < n; ++i) {
        total += arr[i];
    }
    double rata_rata = total / n;

    cout << "Nilai maksimum: " << maksimum << endl;
    cout << "Nilai minimum: " << minimum << endl;
    cout << "Nilai rata-rata: " << rata_rata << endl;

    return 0;
}
```
#### Output:
![image](https://github.com/morcellaa/Struktur-Data-Assignment/assets/162486799/52dcd5cc-e274-4f99-8e2a-93a0dc16748b)

Program akan meminta pengguna untuk memasukkan panjang array, kemudian mengisi array dengan elemen-elemen yang dimasukkan oleh pengguna. Lalu, program mencari nilai maksimum dan minimum dari elemen-elemen array tersebut, serta menghitung nilai rata-rata dari seluruh elemen array. Program ini menggunakan vektor untuk menyimpan elemen-elemen array agar bisa menginputkan array dengan panjang yang dinamis sesuai dengan input pengguna. Setelah semua perhitungan selesai, program menampilkan nilai maksimum, minimum, dan rata-rata tersebut ke layar.

## Kesimpulan
Array merupakan sebuah variabel yang dapat menyimpan lebih dari satu nilai yang memiliki tipe data sama.  Hal ini berbeda dengan variabel biasa yang hanya mampu menampung satu buah nilai. Setiap nilai yang disimpan di dalam array disebut dengan elemen array, sedangkan nilai urut yang digunakan untuk mengakses elemennya disebut dengan indeks array. Array berdimensi satu disebut juga sebagai larik dan digunakan untuk merepresentasikan data dalam satu baris, sementara array berdimensi dua digunakan untuk matriks atau tabel. Array berdimensi tiga digunakan untuk merepresentasikan ruang. 

Apabila kita akan membuat program untuk menyimpan sekumpulan data, misalnya data-data hasil penelitian yang berupa bilangan, dimana jumlah dari data tersebut puluhan, ratusan atau bahkan ribuan, apakah akan menggunakan variabel sebanyak data yang ada? Jawabannya tentu tidak, karena hal tersebut merupakan hal yang sangat tidak efisien. Penggunaan array dalam program akan membuat program lebih efisien dan mudah dipahami.

## Referensi
[1] Piero, Diego and Murni, Dewi. Menentukan Determinan Matriks Persegi Panjang Menggunakan Bahasa C++. Padang; 2021.
[2] Firliana, Rina and Kasih, Patmi. Algoritma dan Pemrograman C++. Adjie Media Nusantara, Nganjuk; 2018.
