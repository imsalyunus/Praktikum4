# Praktikum4
Tugas Pertemuan ke-9
1. Install module texttable yang bisa terlebih dahulu: 
   pip install texttable
2. Pada tahap awal penulisan script, import modul yang akan kita gunakan pada program ini dengan cara memasukkan perintah:
   from texttable import Texttable
3. Buat semua variabelnya, dan jangan lupa disini beberapa variabel kita gunakan LIST (Ditandai dengan tidak ada nilai yang dimasukkan dan hanya ada symbol “[]”)
   jawab = "y"
   no = 0
   nama = []
   nim = []
   ntugas = []
   nuts = []
   nuas = []
4. Buat sebuah perulangan, tujuannya karena kita ingin memasukkan beberapa data sekaligus. Saya pakai while, dan di dalam perulangan inilah kita masukkan perintah untuk Input data yang kita butuhkan. Dengan menggunakan syntax “variabel.append”, saya bertujuan untuk memasukkan data pada variabel-variabel List yang sudah saya buat tadi. Berikut contohnya:
   while (jawab =="y"):
	 nama.append (input ("Nama : "))
	 nim.append (input("NIM : "))
	 ntugas.append (input("Nilai Tugas : "))
	 nuts.append (input("Nilai UTS : "))
	 nuas.append (input("Nilai UAS : "))
	 jawab = input ("Tambah Data (y/t)?")
	 no += 1
5. Sekarang kita buat outro-nya. Disini gua menggunakan for dan saya buat lagi variabel-variabel lokal yang dipakai hanya buat perhitungan doang. Karena ada satu bagian di dalam tabel yaitu NILAI AHIR yang merupakan perhitungan dari 30% TUGAS, 35% UTS, dan 35% UAS. Dan disini juga kita konversi nilai variabel yang tadinya string menjadi float, supaya bisa dihitung.
  print ("            Daftar MAHASISWA         ")
  for n in range (no):
	nt = float(ntugas[n])*30/100
	nu = float(nuts[n])*35/100
	na = float(nuas[n])*35/100
	akhir = nt+nu+na
6. Dan pada bagian terahir dari script ini kita masukkan perintah untuk mencetak hasilnya yaitu  print (table.draw())
