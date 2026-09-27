# PENUGASAN TERSTRUKTUR: ALGORITMA DAN STRUKTUR DATA

## Studi Kasus: Sistem Transaksi & Validasi Toko Buku Modern

```text
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
```
# Trace Table 

## Kasus A
  |Langkah|is_member|jumlah_buku|total_awal|nominal_diskon|diskon|total_bayar|total_awal < 0|jumlah_buku < 1|total_awal >= 200000 AND jumlah_buku >= 3|total_awal >= 300000|
  |---|---|---|---|---|---|---|---|---|---|---|
  |Input|true|4|250000||||||||||
  |Pengecekan Input IF|||||||false|false||||
  |Pencekan Input Until|||||||false|false||||
  |Pencekan Member|true||||||||||
  |Input Diskon|||||10|||||||
  |Cek Total Awal dan Jumlah Buku|||||15|||||true||
  |Hitung Nominal Diskon||||37500||||||||
  |Output Nominal Diskon||||37500||||||||
  |Total Bayar||||||212500||||||
  |Output Total Bayar||||||212500||||||

## Kasus B
  |Langkah|is_member|jumlah_buku|total_awal|nominal_diskon|diskon|total_bayar|total_awal < 0|jumlah_buku < 1|total_awal >= 200000 AND jumlah_buku >= 3|total_awal >= 300000|
  |---|---|---|---|---|---|---|---|---|---|---|
  |Input|false|2|350000||||||||||
  |Pengecekan Input IF|||||||false|false||||
  |Pencekan Input Until|||||||false|false||||
  |Pengecekan Member|false||||||||||
  |Input Diskon|||||0|||||||
  |pengecekan total awal|||||||||||true|
  |Hitung Nominal Diskon||||17500||||||||
  |Output Nominal Diskon||||17500||||||||
  |Total Bayar||||||332500||||||
  |Output Total Bayar||||||332500||||||

  ## Kasus C
  |Langkah|is_member|jumlah_buku|total_awal|nominal_diskon|diskon|total_bayar|total_awal < 0|jumlah_buku < 1|total_awal >= 200000 AND jumlah_buku >= 3|total_awal >= 300000|
  |---|---|---|---|---|---|---|---|---|---|---|
  |Input|false|1|-50000 ||||||||||
  |Pengecekan Input IF|||||||true|false||||
  |Pencekan Input Until|||||||true|false||||
  |Input|false|1|100000||||||||||
  |Pengecekan Input IF|||||||false|false||||
  |Pencekan Input Until|||||||false|false||||
  |Pengecekan Member|false||||||||||
  |Input Diskon|||||0|||||||
  |pengecekan total awal|||||||||||false|
  |Hitung Nominal Diskon||||0||||||||
  |Output Nominal Diskon||||0||||||||
  |Total Bayar||||||100000||||||
  |Output Total Bayar||||||100000||||||

  
  
  
  
  
