#PENUGASAN TERSTRUKTUR: ALGORITMA DAN STRUKTUR DATA

##Studi Kasus: Sistem Transaksi & Validasi Toko Buku Modern


PROGRAM Sistem Transaksi & Validasi Toko Buku Modern
DEKLARASI : 
  is_member : boolean
  jumlah_buku: integer
  total_awal: real
  nominal_diskon
  total_bayar
ALGORITMA :
  
  REPEAT
    INPUT(total_awal, jumlah_buku)
    IF  total_awal < 0 OR jumlah_buku < 1 THEN 
      OUTPUT("input data salah")
    ENDIF
  UNTIL total_awal < 0 OR jumlah_buku < 1

  OUTPUT("input berhasil")

  IF is_member = True THEN 
    
