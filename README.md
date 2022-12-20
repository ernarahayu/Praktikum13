# Praktikum13
Pertemuan 13
## Penanganan Eksepsi
# What is Python Exeption?
• Eksepsi (exception) merupakan suatu kesalahan (error)
yang terjadi saat proses eksekusi program sedang
berjalan,
• Kesalahan ini akan menyebabkan program berakhir
dengan tidak normal.
• Kesalahan-kesalahan ini dapat diidentifikasikan
dengan nama tertentu dan direpresentasikan sebagai
objek di dalam python.
• Error dapat terjadi akibat kesalahan struktur (sintaks)
program. Hal ini disebut syntax error.

## Python Exeption
error dapat terjadi pada saat runtime, error seperti itu disebut eksepsi Fitur membangkitkan eksepsi dengan raise atau dibangkitkan secara paksa dengan perintah RAISE 
``` bash
>>> x = 10
>>> if x > 5:
>>> raise Exception('x should not exceed 5. The value of x was:
{}'.format(x))
Traceback (most recent call last):
File "<input>", line 4, in <module>
Exception: x should not exceed 5. The value of x was: 10
```

## Blok try ... except
• Setiap kode program yang memungkinkan terjadinya eksepsi, maka
perlu untuk di tempatkan di dalam blok try.
• Ketika ada kesalahan maka kode di blok except akan dieksekusi,
• sebaliknya jika program tidak memiliki kesalahan maka blok except
akan di abaikan.
# Contoh :
``` bash
try:

with open('file.log') as file:
read_data = file.read()

except FileNotFoundError as fnf_error:

print(fnf_error)
```
apabila file.log tidak ditemukan, maka akan muncul pesan error:
``` [Errno 2] No such file or directory: 'file.log' ```

## File Open
• Fungsi open() mengambil dua parameter; nama file, dan
mode.
• Ada empat metode (mode) berbeda untuk membuka file:
• "r" - Read - Nilai default. Membuka file untuk membaca, error jika file
tidak ada
• "a" - Add - Membuka file untuk ditambahkan, membuat file jika tidak
ada
• "w" - Write - Membuka file untuk ditulis, membuat file jika tidak ada
• "x" - Create - Membuat file yang ditentukan, mengembalikan kesalahan
jika file tersebut ada

• Syntax
``` f = open("demofile.txt") ```
atau
``` f = open("demofile.txt","rt") ```

## File Read
• Syntax
``` fileObject.read() ```
• Contoh
``` bash
f = open("demofile.txt",
"r")

print(f.read()) 
``` 

## Read Line
• Mebaca file per baris
• Syntax

• Contoh
``` bash 
fileObject.readline()

f = open("demofile.txt",
"r")

print(f.readline())
print(f.readline())
```
## FIle Write
• Syntax
``` fileObject.write("content") ```

• Contoh
``` bash
f = open("demofile.txt",
"a")

f.write("Hello this is first line message")
f.write("Hello this is 2nd line message")
``` 

Parameter:
• "a" - Add - akan ditambahkan ke akhir file
• "w" - Write - akan menimpa konten yang ada

Contoh
``` bash 
f = open("demofile.txt","w")
f.write("Woops! I have deleted the content!")
```