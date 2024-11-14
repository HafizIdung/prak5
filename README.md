Nama: AFLAH ATHALLAH TAMAM KAPUKONG 

Kelas: TI.24.A4

NIM: 312410280

Matkul: Bahasa Pemrograman

# Latihan Praktikum

![gambar](https://github.com/Abcdeflahhh/foto-flowchart/blob/3026cc465e56bdfdfed29c8b87ebac29018e91f3/1.jpg)

# Elemen.py

```python
list_a = [1, 2, 3, 4, 5]

print(list_a[2])

print(list_a[1:4])

print(list_a[-1])

list_a[3] = 10
print(list_a)

list_a[3:] = [11, 12, 13]
print(list_a)

list_b = list_a[:2]
print(list_b)

list_b.append("misalnya")
print(list_b)

list_b.extend([14, 15, 16])
print(list_b)

list_a.extend(list_b)
print(list_a)
```

Code Program tersebut:

![gambar](https://github.com/Abcdeflahhh/foto-flowchart/blob/9dcc8811eadc8452d26aeb75398ee698ba74ec43/3.jpg)

hasil program tersebut:

![gambar](https://github.com/Abcdeflahhh/foto-flowchart/blob/c2e925fd780984ff302800e5e19a9a3e1bff4eb5/2.jpg)

# Menambah data.py

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas

    def hitung_nilai_akhir(self):
        return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3

mahasiswa = []

while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break

print("-" * 60)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 60)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 60)
```

# Penjelasan Code Menambah data

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas
```
`__init__`: Konstruktor ini digunakan untuk menginisialisasi objek Mahasiswa dengan atribut: `nama`, `nim`, `nilai_tugas`, `nilai_uts`, `nilai_uas`

```python
def hitung_nilai_akhir(self):
    return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3
```
Metode ini mengembalikan nilai akhir mahasiswa, yang merupakan rata-rata dari `nilai_tugas`, `nilai_uts`, dan `nilai_uas`.

```python
mahasiswa = []
```
Sebuah daftar kosong `mahasiswa` disiapkan untuk menyimpan objek `Mahasiswa` yang akan ditambahkan

```python
while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break
```
Meminta pengguna untuk memasukkan data mahasiswa berulang kali hingga pengguna memasukkan `t` untuk berhenti, Setiap input digunakan untuk membuat data Mahasiswa, yang kemudian ditambahkan ke dalam daftar mahasiswa

```python
print("-" * 60)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 60)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 60)
```
`Header` tabel dicetak terlebih dahulu, diikuti oleh baris-baris data untuk setiap mahasiswa, Untuk setiap mahasiswa, metode `hitung_nilai_akhir` dipanggil untuk menghitung nilai akhir, lalu data ditampilkan dalam format tabel

Code Program tersebut:

![gambar](https://github.com/Abcdeflahhh/foto-flowchart/blob/fa18f1464259cdc2241d516616f7ff1916da86ca/4.jpg)

Hasil Program tersebut:

![gambar](https://github.com/Abcdeflahhh/foto-flowchart/blob/fa18f1464259cdc2241d516616f7ff1916da86ca/5.jpg)

Dan ini flowchart nya:

![gambar](https://github.com/Abcdeflahhh/prak5/blob/b44c9cdf9b5889e2ddf732a936e3ce5b4093dc36/Image/Screenshot%202024-11-13%20083635.png)
