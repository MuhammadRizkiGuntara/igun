#PENUGASAN TERSTRUKTUR: ALGORITMA DAN STRUKTUR DATA

##Studi Kasus: Sistem Transaksi & Validasi Toko Buku Modern


PROGRAM Sistem Transaksi & Validasi Toko Buku Modern
DEKLARASI : 
  is_member: boolean
  jumlah_buku: integer
  total_awal: real
  nominal_diskon: real 
  diskon: integer
  total_bayar: real
ALGORITMA :
  
  REPEAT
    INPUT(total_awal, jumlah_buku, is_member)
    IF  total_awal < 0 OR jumlah_buku < 1 THEN 
      OUTPUT("input data salah")
    ENDIF
  UNTIL total_awal < 0 OR jumlah_buku < 1

  OUTPUT("input berhasil")

  IF is_member = True THEN 
    diskon ← 10
    IF total_awal >= 200000 AND jumlah_buku >= 3 THEN
      diskon ← diskon + 5 
    ENDIF
  ELSE 
    diskon ← 0
    IF total_awal >= 300000 THEN
      diskon ← 5
    ENDIF
  ENDIF

  nominal_diskon ← total_awal*diskon/100
  OUTPUT (nominal_diskon)
  total_bayar ← total_awal - nominal_diskon
  OUTPUT (total_bayar)

#Trace Table 

##Kasus A
  |Lankah|is_member|jumlah_buku|total_awal|nominal_diskon|diskon|total_bayar|
  |Input|true|4|250000|0|0|0|

  
