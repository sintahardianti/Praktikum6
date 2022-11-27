### Nama : Sinta Hardianti Wijaya

### NIM : 312210342

### Kelas : TI.22.A3

# Latihan 1 

## ∘ Dictionary daftar kontak

### Dictionary adalah Koleksi item yang berasosiasi dimana setiap pasangan terdiri key dan value.

'Nama' sebagai key, dan ''Nomor' sebagai value.

## -> Dictionary ditulis dengan dipisahkan koma dalam {}

```
telepon = {'Ari' : '081267888', 'Dina' : '087677776'}
```

## -> Untuk menampilkan kontak

```
print(telepon['Ari'])
```

## -> Menambahkan elemen dictionary

```
telepon['Riko' :'087654544']
```

## -> Untuk mengubah dictionary caranya hampir sama dengan menambahkannya

```
telepon['Dina'] = '088999776'
```

## -> Perintah menampilkan semua nama/key

```
print(telepon.keys())
```

## Outputnya :

![menampilkan nama](https://user-images.githubusercontent.com/115516473/204115549-95705a43-1b0a-461b-9482-95e4e199ff17.png)


## -> Perintah menampilkan semua nomor/value

```
print(telepon.values())
```

## Outputnya :

![menampilkan nomor](https://user-images.githubusercontent.com/115516473/204115561-0b04875e-ad19-4082-9e13-decf4a2e218d.png)


## -> Perintah menampilkan daftar nama dan nomornya (gunakan 'for)

```
for nama,nomor in telepon.items():
    print("%s \t| %s " % (nama,nomor))
```

## Outputnya :

![nama dan nomor](https://user-images.githubusercontent.com/115516473/204115577-1f08e182-2895-44fd-9d4a-2930bcf2f422.png)


## -> Menghapus kontak Dina

```
del telepon['Dina']
```

## Kontak Dina akan terhapus, dan outputnya sebagai berikut :

![kontak dina terhapus](https://user-images.githubusercontent.com/115516473/204115599-3323328e-a700-4c4d-8c19-a6839352a390.png)

# Tugas Praktikum

### Membuat dictionary kosong

```
mahasiswa {}
```

### Buat program untuk melihat datanya

```
def show():
    if mahasiswa.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in mahasiswa.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
            .format (a[0][: 14],a[1][0],a[1][1],a[1][2],a[1][3],a[1][4], no = i))
        print("=================================================================================")
        
    else:
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                                TIDAK ADA DATA                                 |")
        print("=================================================================================")
 ``` 

```else``` digunakan untuk menampilkan yang terjadi jika Nama yang diketik tidak ada

### Buat program untuk tambah datanya

```
def add():
    print("Tambah Data")
    nama = input("Nama\t : ")
    nim = input("NIM\t : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
    mahasiswa[nama] = nim, tugas, uts, uas, akhir
```

### Buat program untuk hapus data

```
def delete():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")
    
    if nama in mahasiswa.keys():
        del mahasiswa[nama]
    
    else:
        print("Nama tidak ditemukan")
 ```
 
 ### Buat program untuk ubah data
 
 ```
 def update():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in mahasiswa.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30/100) + (uts * 35/100) + (uas * 35/100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir

    else:
        print("Nama tidak ditemukan ")
  ```

### Buat program untuk cari data

```
def search():
    print("Cari Data")
    a = input("Masukkan Nama : ")
    if a in mahasiswa.keys():
        print("===========================================================================")
        print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
        print("===========================================================================")
        print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
            .format (a , mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4] ))
        print("===========================================================================")

    else:
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                          DATA TIDAK DITEMUKAN                                 |")
        print("=================================================================================")
```

program ini berbeda dengan melihat data, program ini akan memunculkan nama yang diketik pada input

### Buat Program untuk menu nya

```
def menu():
    print("\n")
    print("================================")
    print("      Program input nilai       ")
    print("================================\n")

    x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
    print("\n")

    if x == 'L':
        show()
    elif x == 'T':
        add()
    elif x == 'U':
        update()
    elif x == 'H':
        delete()
    elif x == 'C':
        search()
    elif x == 'K':
        print("==========================================================================")
        print('\n')
        print("> You exit the code                        ")
        print("\n")
        print("==========================================================================")

        exit()

    else:
        print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")
```

Program berisikan menu, jika ketik L/T/U/H/C/K maka akan menjalankan perintah program program yang diketik di atas seperti ```show()```,``` add()```,``` update()```,``` delete()```,``` search()```

### Kodenya akan berjalan dengan perintah

```
while True:
    menu()
```


### Outputnya :

-> Lihat tanpa data 

![tanpa data](https://user-images.githubusercontent.com/115516473/204116333-9ba85f73-c0cd-4a6f-9cff-e3e2ebc5fd56.png)

-> Tambah data

![tambah data](https://user-images.githubusercontent.com/115516473/204116403-49b4085f-51e0-47c7-abf5-ca919af041d1.png)

-> Lihat dengan data

![lihat data](https://user-images.githubusercontent.com/115516473/204116451-b444700c-e67b-4d09-902d-8429a21a1b47.png)

-> Ubah data

