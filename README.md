# labspy08
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <table border="1">
        <tr>
            <th> Nama</th>
            <th>NIM</th>
            <th>Kelas</th>
        </tr>
        <tr>
            <td>Putra Megantara</td>
            <td>312110251</td>
            <td>TI.21.A.1</td>
        </tr>
    </table>
</body>
</html>

## Tugas Praktikum
- Buatlah program sederhana dengan mengaplikasikan penggunaan class. Buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan;
> - Method *tambah()* untuk menambahkan data
> - Method *tampilkan()* untuk menampilkan data
> - Method *hapus(nama)* untuk menghapus data berdasarkan nama
> - Method *ubah(nama)* untuk mengubah data berdasarkan nama
> - Buatlah diagram class, flowchart dan penjelasan program pada README.md

### Penjelasan
- Untuk mengimport dan mendapatkan clear system pada os
```bash
from os import system
```

- Untuk membuat class beserta untuk menampung data mahasiswa dan atributnya
```bash
class mahasiswa:
    nim=""
    nama=""
    tugas=""
    uts=""
    uas=""
    akhir=""
```

- Untuk variabel untuk menampung list dari dari object mahasiswa
```bash
pilih=0
datasiswa=[]
```

- Untuk menampilkan daftar menu mahasiswa dapat menggunakan
```python
def menu():
    system("cls")
    print("PROGRAM INPUT NILAI MAHASISWA")
    print("Menu Utama");
    print("-"*43)
    print("1. Tambah Data")
    print("2. Lihat Data")
    print("3. Ubah Data")
    print("4. Hapus Data")
    print("5. Keluar")
    pilih= int(input("Masukan Pilihan Anda : "))
    if pilih == 1:
        pilih1()
        menu()
    elif pilih == 2:
        tampil()
        input("Kembali Menu Utama")
        menu()
    elif pilih == 3:
        index_update=-1
        tampil()
        id_edit = int(input("Input NIM yang akan diupdate "))
        for a in range(0, len(datasiswa)):
            if id_edit==datasiswa[a].nim:
                index_update=a
                break
        if (index_update > -1):
            print("INPUT DATA YANG DI UPDATE")
            siswa=mahasiswa()
            siswa.nim=(int(input("Msdukan NIM: ")))
            siswa.nama=(input("Masukan Nama Mahasiswa:"))
            siswa.tugas=(float(input("Masukan Nilai Tugas:")))
            siswa.uts=(float(input("Masukan Nilai Uts:")))
            siswa.uas=(float(input("Masukan Nilai Uas:")))
            siswa.akhir=siswa.tugas*0.30+siswa.uts*0.35+siswa.uas*0.35
            datasiswa=[index_update]=siswa
            print("Berhasil Update Data Mahasiswa")
        else : print("NIM Tidak Ditemukan")
        input("Kembali Menu Utama")
        menu()
    elif pilih ==4:
        system("cls")
        tampil()
        index_update=-1
        id_hapus = int(input("Input NIM Yang Akan Dihapus"))
        for a in range (0, len(data)):
            if id_hapus==datasiswa[a].nim:
                index_delete = a
                break
        if(index_delete > -1):
            del datasiswa[index_delete]
            print("Data Telah Dihapus")
        else: 
            print("NIM Tidak Ditemukan")
            input("Kembali Menu Utama")
            menu()
            menu()
    elif pilih ==5 :
        exit()
```

- Untuk menambahkan data mahasiswa
```bash
def pilih1():
    ulang = "Y"
    while ulang in("y","Y"):
        system("cls")
        siswabaru=mahasiswa()
        print("INPUT DATA MAHASISWA")
        siswabaru.nim=(int(input("Masukan NIM            : ")))
        siswabaru.nama=(input("Masukan Nama Mahasiswa : "))
        siswabaru.tugas=(float(input("Masukan Nilai Tugas    : ")))
        siswabaru.uts=(float(input("Masukan Nilai UTS      : ")))
        siswabaru.uas=(float(input("Masukan Nilai UAS      : ")))
        siswabaru.akhir=siswabaru.tugas*0.30 + siswabaru.uts*0.35 + siswabaru.uas*0.35
        datasiswa.append(siswabaru)
        ulang=input("Apakah Anda Ingin Mengulang (Y/T)? ")
menu()
```

- Input untuk menampilkan data yang sudah tersimpan ,cara mengaksesnya dengan memilih angka yang sudah disedikan di daftar menu
```python
def tampil():
    system("cls")
    print("DATA MAHASISWA")
    for data in datasiswa:
        print("Nim          : "+str(data.nim)) 
        print("Nama         : "+data.nama)
        print("Nilai Tugas  : "+str(data.tugas))
        print("Nilai UTS    : "+str(data.uts))
        print("Nilai UAS    : "+str(data.uas))
        print("Nilai Akhir  : "+str(data.akhir))
        print("-"*18)
```

- Untuk menghapus data mahasiswa yang sudah dimasukan kedalam menu
```bash
elif pilih ==4:
        system("cls")
        tampil()
        index_update=-1
        id_hapus = int(input("Input NIM Yang Akan Dihapus"))
        for a in range (0, len(data)):
            if id_hapus==datasiswa[a].nim:
                index_delete = a
                break
        if(index_delete > -1):
            del datasiswa[index_delete]
            print("Data Telah Dihapus")
        else: 
            print("NIM Tidak Ditemukan")
            input("Kembali Menu Utama")
            menu()
            menu()
```

- Untuk keluar dari program
```bash
  elif pilih ==5 :
        exit()
```


#OUTPUT

![Screenshot (78)](https://user-images.githubusercontent.com/92736847/146949586-6633abd7-4fff-4053-93ec-7efc31c9cc37.png)
![Screenshot (79)](https://user-images.githubusercontent.com/92736847/146949566-6ad6f9c3-cb04-40cd-8b7f-8e11cc70e463.png).
![Screenshot (80)](https://user-images.githubusercontent.com/92736847/146949622-c5e4e991-4ded-4a84-957c-8109af634696.png)

![png](https://user-images.githubusercontent.com/92736847/146951619-a83767d5-b45b-494e-be5b-42d420a40365.png)
