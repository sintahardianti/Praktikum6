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

Membuat dictionary kosong

```
mahasiswa {}
```

