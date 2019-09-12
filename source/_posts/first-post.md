---
title: Contoh Array C++
date: 2019-09-02 10:52:58
tags: C++
---

### Soal:
1. Buatlah programm untuk menghitung dan mencetak nila rata-rata, nilai tertinggi, dan nilai terendah dari sekelompok bilangan bulat positif (integer). Jumlah data tidak diketahui, dimasukan melalui keyboard.

``` bash
#include<iostream>
#include<string>

using namespace std;

main() {
    int 
    nilai[100], 
    batas__nilai, 
    index__nilai;

    float 
    jumlah__nilai, 
    rata__nilai, 
    max__nilai,
    min__nilai; 

    cout<< "\n Masukan jumlah data yang ingin dihitung : ";

    cin>>batas__nilai;

    for(index__nilai = 1; index__nilai <= batas__nilai; index__nilai ++) {

        cout<<"\n Masukan angka "<<index__nilai<<" : "; cin>>nilai[index__nilai];

        jumlah__nilai += nilai[index__nilai];

        if(index__nilai == 1) {
            max__nilai = nilai[index__nilai];
            min__nilai = nilai[index__nilai];
        }
        
        if(nilai[index__nilai] > max__nilai) {
            max__nilai = nilai[index__nilai];
        } 

        /*****
         * * Nilai Max
         * 
         * * Terjemah :
         *   Jika nilai masukan lebih besar dari kumpulan nilai masukan,
         *   nilai max sama dengan nilai masukan
         * 
         * * Perulangan :
         *   Jika 2 lebih besar dari 2 = false 
         *   Jika 2 lebih besar dari 3 = false
         *   Jika 3 lebih besar dari 2 = true
         *   Jika 3 lebih besar dari 3 = false
         * 
         * * Hasil nilai:
         *   Dari 2 dan 3 lebih besar = 2 
         * ******************************/        

        if(nilai[index__nilai] < min__nilai) {
            min__nilai = nilai[index__nilai];
        }

        /*****
         * * Nilai Min
         * 
         * * Terjemah :
         *   Jika nilai masukan lebih kecil dari kumpulan nilai masukan,
         *   nilai min sama dengan nilai masukan
         * 
         * * Perulangan :
         *   Jika 2 lebih kecil dari 2 = false / salah
         *   Jika 2 lebih kecil dari 3 = true / benar
         *   Jika 3 lebih kecil dari 2 = false
         *   Jika 3 lebih kecil dari 3 = false
         * 
         * * Hasil nilai:
         *   Dari 2 dan 3 lebih kecil = 2 
         * ******************************/ 

    }

    rata__nilai = jumlah__nilai/batas__nilai;

    cout<<"\n ============================ "<<endl;
    cout<<"\n Nilai Jumlah = "<<jumlah__nilai<<endl;
    cout<<"\n Nilai Rata-rata = "<<rata__nilai<<endl;
    cout<<"\n Nilai Maksimum = "<<max__nilai<<endl;
    cout<<"\n Nilai Minimum = "<<min__nilai<<endl;
    
}
```

### Penjelasan:

#### 1. Nilai Jumlah
``` bash
jumlah__nilai += nilai[index__nilai];
```
##### a. Terjemah
Nilai Jumlah 
adalah jumlah__nilai ditambah sama dengan nilai semua masukan selama perulangan.

##### b. Perulangan
jumlah__nilai += 2
jumlah__nilai += 3

##### c. Hasil
Nilai jumlah = 2 + 3
Nilai jumlah = 5


#### 1. Nilai Rata-rata
``` bash
rata__nilai = jumlah__nilai/batas__nilai;
```
##### a. Terjemah
Nilai Rata-rata 
adalah rata__nilai sama dengan Nilai jumlah dibagi nilai batas

##### b. Perulangan
jumlah__nilai = 5
batas__nilai  = 2

##### c. Hasil
Nilai Rata-rata = 5 : 2
Nilai Rata-rata = 2.5


#### 1. Nilai Maksimum
``` bash
if(nilai[index__nilai] > max__nilai) {
    max__nilai = nilai[index__nilai];
} 
```
##### a. Terjemah
Nilai Maksimum 
adalah jika nilai[index__nilai] (nilai masukan) lebih besar dari max__nilai (kumpulan nilai masukan).

##### b. Perulangan
Jika 2 lebih besar dari 2 = false 
Jika 2 lebih besar dari 3 = false
Jika 3 lebih besar dari 2 = true
Jika 3 lebih besar dari 3 = false

##### c. Hasil
Nilai maksimum = false
Nilai maksimum = 2