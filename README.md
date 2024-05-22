# `Praktikum 4 - Basis Data`
### Nama: M Wahyudin Ardiansyah
### Kelas: Ti.23.A1
### Nim: 312210148

## `Tugas Praktikum`
- Buat 2 tabel, `tabel pegawai dan tabel hewan`.
## `Tabel pegawai`
![gambar-1](https://i.imgur.com/DT8YKxS.png)
- Tampilkan pegawai yang gajinya bukan `2.000.000 dan 1.250.000` dengan memasukan perintah
```
select * from pegawai
    where gaji not in (2000000, 1250000);
```
![gambar-3](https://i.imgur.com/olcW7vs.png)
- Menampilkan pegawai yang tunjangannya `NULL` dengan perinrah
```
select * from pegawai
    where tunjangan is null;
```
![gambar-4](https://i.imgur.com/kMi3jPZ.png)
- Menampilkan pegawai yang tunjangannya `tidak NULL` dengan perintah
```
select * from pegawai
    where tunjangan is not null;
```
![gambar-5](https://i.imgur.com/O4hQYgX.png)
- Menampilkan `jumlah baris/record tabel pegawai` dengan perintah
```
select count(*) as jumlah_pegawai
    from pegawai;
```
![gambar-6](https://i.imgur.com/tRoAgv8.png)
- Menampilkan `jumlah total gaji di tabel pegawai` dengan perintah
```
select sum(gaji) as total_gaji
    from pegawai;
```
![gambar-7](https://i.imgur.com/k0YvCvb.png)
- Menampilkan `hitung rata-rata gaji pegawai` dengan perintah
```
select avg(gaji) as rata_rata_gaji
    from pegawai;
```
![gambar-8](https://i.imgur.com/KNosAv6.png)
- Menampilkan `gaji terkecil` dengan perintah
```
select min(gaji) as gaji_terkecil
    from pegawai;
```
![gambar-9](https://i.imgur.com/WnX0DW5.png)
- Menampilkan `gaji terbesar` dengan perintah
```
select max(gaji) as gaji_terbesar
    from pegawai;
```
![gambar-10](https://i.imgur.com/rdYmGiz.png)
## `Tabel hewan`
![gambar-2](https://i.imgur.com/8PPB4Mw.png)
- Menampilkan `jumlah hewan yang dimiliki setiap owner` dengan perintah
```
select owner, count(*) as jumlah_hewan
    from hewan
    group by owner;
```
![img-1](https://i.imgur.com/Rl3SCQM.png)
- Menampilkan `jumlah hewan berdasarkan spesies` dengan perintah
```
select species, count(*) as jumlah_hewan
  from hewan
  group by species;
```
![img-2](https://i.imgur.com/w1mJFro.png)
- Menampilkan `jumlah hewan berdasarkan jenis kelamin` dengan perintah
```
select sex, count(*) as jumlah_hewan
  from hewan
  group by sex;
```
![img-3](https://i.imgur.com/UleVmqi.png)
- Menampilkan `jumlah hewan berdasarkan spesies dan jenis kelamin` dengan perintah
```
select species, sex, count(*) as jumlah_hewan
  from hewan
  group by species, sex;
```
![img-4](https://i.imgur.com/TEwbp3i.png)
- Menampilkan `jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin`
```
select species, sex, count(*) as jumlah_hewan
  from hewan
  where species in ('Cat', 'Dog')
  group by species, sex;
```
![img-5](https://i.imgur.com/HNZovNK.png)
- Menampilkan `jumlah hewan berdasarkan jenis kelamin yang diketahui saja` dengan perintah
```
 select sex, count(*) as jumlah_hewan
  from hewan
  where sex is not null
  group by sex;
```
![img-6](https://i.imgur.com/q4eq0RB.png)

## `Kesimpulan`
