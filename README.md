Nama:Daffa Dhiya Ulhaq
Nim :2310432047
Shift:2

def tambah (judul,nama_penulis,nama_penerbit,tahun_terbit):
     with open("daffa.txt","a")as file:
         file.write(f"|{judul}|{nama_penulis}|{nama_penerbit}|{tahun_terbit}|\n")
         print("data telah ditambahkan")

def hapus():
     open("daffa.txt","w").close()

def tampilkan():
     with open("daffa.txt","r")as file:
          teks = file.readlines()
          for baris in teks:
               print(baris)


while True:
     print("1.tambah")
     print("2.hapus")
     print("3.tampilkan")
     print("4.Selesai")

     pilih = input("pilih menu (1/2/3/4) = ")

     if pilih == "1":
         judul = input("Judul         = ")
         nama_penulis = input("Nama Penulis  = ")
         nama_penerbit = input("Nama Penerbit = ")
         tahun_terbit = input("Tahun Terbit  = ")
         tambah (judul,nama_penulis,nama_penerbit,tahun_terbit)

     elif pilih == "2":
         hapus()
         print("data telah dihapus")
         print()

     elif pilih == "3":
         tampilkan()
         print()

     elif pilih == "4":
         print("Terima Kasih:) \n")
         print("Program Anda Telah Selesai \n")
         break

     else:
         print("Pilihan anda tidak valid dan Silahkan coba kembali")

