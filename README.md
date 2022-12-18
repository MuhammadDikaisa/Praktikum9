# Praktikum9
---
# Nama : Muhammad Dikaisa Ibnu amin
# NIM : 312210289
# Kelas : TI.22.A.3
---
# Penanganan Eksepsi Python
## Apa itu Eksepsi Python
* Eksepsi (exception) merupakan suatu kesalahan (error)
yang terjadi saat proses eksekusi program sedang
berjalan,
* Kesalahan ini akan menyebabkan program berakhir
dengan tidak normal.
* Kesalahan-kesalahan ini dapat diidentifikasikan
dengan nama tertentu dan direpresentasikan sebagai
objek di dalam python.
* Error dapat terjadi akibat kesalahan struktur (sintaks)
program. Hal ini disebut syntax error.

Contoh nya sebagai Berikut : 

<img width="300" alt="Pertemuan13 1" src="https://user-images.githubusercontent.com/115516378/208283555-790cfe74-d2df-4337-8a2e-1055435370ee.png">

## Fitur Eksepsi

Python menyediakan dua fitur yang sangat penting untuk menangani
kesalahan tak terduga dalam program dan menambahkan kemampuan
debugging di dalamnya,
* Exception Handling
* Assertions Exception adalah sebuah peristiwa, yang terjadi selama
pelaksanaan program yang mengganggu aliran normal instruksi
program. Secara umum, ketika skrip Python menemukan situasi yang
tidak dapat diatasi, hal itu menimbulkan pengecualian. Exception
adalah objek Python yang mewakili kesalahan.

## Python Exeption

* Error dapat terjadi pada saat runtime, Error seperti ini disebut
eksepsi.
* Misalnya, bila kita membuka file yang tidak ada, maka akan muncul
pesan kesalahan FileNotFoundError.
*Bila kita membagi bilangan dengan nol akan muncul
ZeroDivisionError, dan lain sebagainya.

Contohnya sebagai berikut : 

<img width="300" alt="Pertemuan13 2" src="https://user-images.githubusercontent.com/115516378/208283745-13c0b395-5b4f-477d-ab5c-dc49283d312c.png">

## Membangkitkan Eksepsi dengan raise

* Ada banyak tipe eksepsi di dalam python, yang semuanya bisa
dibangkitkan baik pada saat penanganan kesalahan (error) atau bisa
juga kita bangkitkan secara paksa dengan menggunakan perintah
**raise**.

Contohnya sebagai berikut : 
```
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was:
{}'.format(x))
```
Outputnya : 

<img width="425" alt="Pertemuan13 3" src="https://user-images.githubusercontent.com/115516378/208284100-d1d6c9d4-39f2-4977-8285-1e49e13da908.png">

## Blok try ... except

* Setiap kode program yang memungkinkan terjadinya eksepsi, maka
perlu untuk di tempatkan di dalam blok try.
* Ketika ada kesalahan maka kode di blok except akan dieksekusi,
* sebaliknya jika program tidak memiliki kesalahan maka blok except
akan di abaikan.

Contohnya sebagai berikut : 
```
try:
  with open('file.log') as file:
    read_data = file.read()
except FileNotFoundError as fnf_error:
  print(fnf_error)
```

apabila file.log tidak ditemukan, maka akan muncul pesan error:

```
[Errno 2] No such file or directory: 'file.log'
```
