## v1.0 (1 Januari 2024)
- Rilis pertama
Fitur:
- Waktu sholat halaman depan dengan algoritma Irsyadul Murid
- Konversi tanggal Hijriyah - Masehi dan sebaliknya
- Konversi Julian Day ke Hijriyah dan Masehi
- Grafik visibilitas hilal 1 tahun
- Waktu sholat
- Hisab awal bulan Hijriyah
- Ephemeris matahari dan bulan seperti winhisab
- dll 

## v2.0 (12 Januari 2024)
Fixs:

- Perbaikan UI
- Format jadwal waktu sholat halaman depan diubah menjadi HH:mm dengan pembulatan detik ke menit, jika detik sama atau lebih dari 30 detik
- Elevasi/tinggi tempat diatur ke 0 m, jika elevasi terdeteksi dibawah 0 (minus) dihalaman depan
- Tipe input pada TextFiled disesuaikan agar tidak terjadi potensi salah input tipe data yang bisa menyebabkan crash
Ketika tinggi hilal hakiki dibawah 0 (minus), data-data lain tidak perlu ditampilkan
- Perbaikan pada library lib-hisab-irsyadulmurid & lib-konversi

Additions:

- Penambahan fitur hisab gerhana bulan & gerhana matahari global

## v2.5.0 (26 September 2024)
add:

- Library ephemeris jean meeus
- Waktu sholat halaman depan diganti algoritma jean meeus
- Fitur generate tabel ephemeris
- Fitur generate tabel jadwal imsakiyah
- Opsi algoritma di menu waktu sholat

change:

- Perbaikan bug, improvisasi ui dan peningkatan performa aplikasi

## v2.6.0 (23 Oktober 2024)
Penambahan:

- Fitur tarik refresh untuk merefresh data lokasi & tampilan halaman depan
- Fitur cek pembaruan versi dari dalam aplikasi, jika tersedia user akan dibawa ke server GitHub untuk mendownload versi terbaru
- Fitur mode offline, saat tidak ada internet, aplikasi akan mendapatkan data lokasi dari GPS, namun nama lokasi tidak bisa ditampilkan karena geocoder tetap butuh akses internet
- Indikator progress linear dihalaman depan saat sedang mencari data lokasi
- Ephemeris detail (geosentris & toposentris), namun agak lambat membukanya, mungkin karena library tabel yang digunakan
- Support bahasa Inggris, namun sebagian kecil string yang dihardcode baik di viewmodel/library belum diganti

Perbaikan:

- Perbaikan beberapa bug kecil dan improvisasi UI

Cara update:
> Buka aplikasi Kanzul Falak -> Klik Pengaturan -> Klik Periksa pembaruan -> Klik Perbarui -> Download Kanzul Falak versi 2.6.0

## v2.7.0 (25 Desember 2024)
Additions/penambahan:

- Tasbih digital
- Algoritma VSOP87D & ELPMPP02, namun bertahap di beberapa menu
- Generate file hasil hitung waktu sholat & imsakiyah
- Salin data hasil hitung waktu sholat ke clipboard
- Keterangan tambahan di menu tips

Changes/perubahan:

- Mengganti Toast dengan Flashbar kecuali halaman depan
- Mengganti Algoritma Jean Meeus di halaman depan dengan VSOP87D

Fixs/perbaikan:

- Bug kritis fungsi gregorianToJD
- Perbaikan UI

Cara update:
> Buka aplikasi Kanzul Falak -> Klik Pengaturan -> Klik Periksa pembaruan -> Klik Perbarui -> Download Kanzul Falak versi 2.7.0

## v2.9.0 (22 Januari 2025)
Additions/penambahan:

- Algoritma VSOP87D & ELPMPP02 di menu Ephemeris, Ephemeris Detail dan Hilal (Awal bulan hijriyah)
- Menu Sinkronisasi Kalender (Awal bulan hijriyah dalam satu tahun) dengan algoritma VSOP87D & ELPMPP02
- Generate file dan copy di menu Hilal
- Generate file di menu Sync. Kalender
- Input jam, menit, detik dan time zone di menu Tahwil Tarikh (khusus mencari JD masehi)
- Input time zone dan menampilkan jam di menu Tahwil Julian Day
- Algoritma Astronomical Algorithm di menu Fase Bulan

Changes/perubahan:

- Direktori penyimpanan file txt dari folder files ke dalam folder TXT di direktori non-SAF (Android/data/com.nama.paket.aplikasi/files/TXT)
- Algoritma Irsyadul Murid di menu Grafik Visibilitas Hilal diganti dengan VSOP87D & ELPMPP02
- Prediksi awal bulan hijriyah di menu Hilal sekarang menggunakan kriteria IRNU (VSOP87D & ELPMPP02 dan Irsyadul Murid), SK LF-PBNU No. 001/SK/LF-PBNU/III/2022, tinggi hilal mar'i minimal 3° dan elongasi geocentric minimal 6.4°
- Improvisasi tata letak data dibeberapa file yang dihasilkan

Fixs/perbaikan:

- Leak memory (kebocoran memori)
- Perbaikan UI

Cara update:
> Buka aplikasi Kanzul Falak -> Klik Pengaturan -> Klik Periksa pembaruan -> Klik Perbarui -> Download Kanzul Falak versi 2.9.0

## v3.0.0 (3 Februari 2025)
Additions/penambahan:

- Algoritma/model JPL DE405 & IAARAS EPM2021 di menu Ephemeris, Ephemeris Detail, dan Waktu Sholat (perlu instalasi mandiri, cara instalasi file biner DE405 & EPM2021 ada di menu Tips)
- Data arah matahari dan hilal di menu Sinkronisasi/penyerasian kalender
- Dokumentasi & info instalasi file biner JPL DE405 & EPM2021 IAARAS di menu Tips

Fixs/perbaikan:

- Selamatan/peringatan orang meninggal

Cara update:
> Buka aplikasi Kanzul Falak -> Klik Pengaturan -> Klik Periksa pembaruan -> Klik Perbarui -> Download Kanzul Falak versi 3.0.0

## v3.1.1 (3 Maret 2025)
Additions/penambahan:

- Algoritma/model JPL DE405 & IAARAS EPM2021 di menu Imsakiyah (perlu instalasi mandiri, cara instalasi file biner DE405 & EPM2021 ada di menu Tips)
- Pengecekan cakupan waktu JPL DE405 & EPM2021 IAARAS agar tidak crash jika input diluar batas cakupan
- Input ihtiyat zuhur & menampilkan nilai ihtiyat zuhur & lainnya di menu Waktu Sholat

Fixs/perbaikan:

- Earth heliocentric longitude algoritma VSOP87D tidak sengaja termodulus
- Fungsi gregorianToJD

Cara update:
> Buka aplikasi Kanzul Falak -> Klik Pengaturan -> Klik Periksa pembaruan -> Klik Perbarui -> Download Kanzul Falak versi 3.1.1

## v3.5.0 (7 September 2025)
Penambahan (Additions):

- Data koordinat rectangular Sun barycentric, Earth barycentric, Sun geocentric, & Moon geocentric (x,y,z serta kecepatan/velocity vx, vy, vz satuan km/day) dalam sistem & kerangka acuan langit ICRS/ICRF (Mean J2000), dan beberapa data lain di menu Ephemeris Detail
- Jam Astronomi (menampilkan data realtime jam lokal & UT, GST/LST, & beberapa data matahari & bulan)
- Algoritma/model JPL DE405 & IAARAS EPM2021 di menu Hilal (perlu instalasi mandiri, link & cara instalasi file biner DE405 & EPM2021 ada di menu Tips)
- Tombol custom warna aksen tema (ada 19 tema warna rekomendasi google material desain)
- Deteksi otomatis cek update rilis di halaman depan
- Menu pembulatan detik di menu Imsakiyah
- Ikon fase-fase bulan di menu Fase Bulan
- Opsi pengaturan ikuti sistem (tema gelap/terang mengikuti sistem perangkat)

Perbaikan (Fixes):

- Modulus data durasi hilal di menu Hilal
- Beberapa warna text disesuaikan (warna & logo masih dipertahankan ungu) di halaman tentang
- Kebocoran memori
- Beberapa perbaikan kecil

Perubahan (Changes):

- URL file biner JPL DE405 & EPM2021 di menu Tips kini dapat diklik, user akan langsung dapat mengunduhnya
- Adaptasi ikon support tema dinamis (Material You)

Total koefisien JPL DE405 sebanyak 7.015.038, namun hanya 3.142.296 untuk menghitung data ephemeris Matahari dan Bulan, yakni:

- Sun (454.806)
- Moon (2.149.992)
- dan EMB/Earth-Moon Barycenter (537.498)

sedangkan untuk IAARAS EPM2021 Total koefisien sebanyak 4.962.750, namun hanya 2.223.000 koefisien untuk menghitung data ephemeris Matahari & Bulan, yakni:

- Sun (321.750)
- Moon (1.521.000)
- EMB/Earth-Moon Barycenter (380.250)

Cara update:
> *Bagi yang sudah menginstal Kanzul Falak sejak versi 2.6.0, anda dapat mengecek update versi melalui ->
> Buka aplikasi Kanzul Falak -> Klik Pengaturan -> Klik Periksa pembaruan -> Klik Perbarui -> Download Kanzul Falak versi 3.5.0

## v3.6.0 (30 Oktober 2025)
Add: splash screen
Fix: memperbaiki mesin tema/theme engine & beberapa menu hisab tidak dapat bekerja/some hisab menu not working

## v3.6.1 (7 November 2025)
Fix: lama hilal/hilal duration

## v3.7.2 (7 Januari 2026)
Penambahan (Additions):

- Algoritma Jean Meeus pada menu Hilal (hisab awal bulan hijriyah)

Perbaikan (Fixes):

- Lama hilal/muktsul hilal rumus taqribi
- Beberapa perbaikan kecil

Perubahan (Changes):

- Upgrade target SDK ke 35 (android 15, minimal android 8/Oreo)
- Upgrade library lib-vsop87d-elpmpp02 ke versi 12.0.11
- Upgrade library lib-jeanmeeus ke versi 3.2.0
- Upgrade versi AGP ke 8.6.0
- Upgrade versi Gradle ke 8.12.0

Total koefisien JPL DE405 sebanyak 7.015.038, namun hanya 3.142.296 untuk menghitung data ephemeris Matahari dan Bulan, yakni:

- Sun (454.806)
- Moon (2.149.992)
- dan EMB/Earth-Moon Barycenter (537.498)

sedangkan untuk IAARAS EPM2021 Total koefisien sebanyak 4.962.750, namun hanya 2.223.000 koefisien untuk menghitung data ephemeris Matahari & Bulan, yakni:

- Sun (321.750)
- Moon (1.521.000)
- EMB/Earth-Moon Barycenter (380.250)

## v3.9.0 (28 Januari 2026)
Penambahan (Additions):

- Pengelola file biner JPL DE & EPM IAARAS, pengguna sekarang dapat menginstal file biner dengan sangat mudah (Pengaturan -> Kelola File Biner DE -> Unduh)
- Algoritma Ad-Durrul Aniq pada menu Hilal (sementara hanya untuk target tahun 1411 H keatas, karena data tabel sanah majmuah belum selesai ditambahkan, lihat pesan pada menu Hilal)
- Tampilan baru hasil hisab awal bulan, ditampilkan lebih banyak data
- Fitur zoom in/out pada tampilan hasil hisab awal bulan dengan dicubit (sementara hanya di menu Hilal)

Perbaikan (Fixes):

- Fix: Lama hilal metode Irsyadul Murid
- Fix: GST & LST pada real-time halaman depan
- Beberapa perbaikan kecil

Perubahan (Changes):

- Beberapa perubahan adapatasi fitur baru

NB: Hasil hisab dengan metode Ad-Durrul Aniq untuk target di bawah tahun 1411 H akan tidak sesuai dikarenakan:
Data tabel pada program Ad-Durrul Aniq masih belum lengkap, yaitu:

1. di tabel jadwal harokat sinin majmuah litholabil ijtima hal 156 dari tahun 420 sampai 1380 belum ditambahkan
2. di tabel jadwal harokat fi sinin majmuah li harokat syams wal qomar hal 166 dari tahun 0 sampai 1380 belum ditambahkan

Kekurangan data tabel tersebut akan ditambahkan seiring waktu.
Untuk target tahun 1411 H keatas InshaAlloh aman.

## v3.10.0 (6 Februari 2026)
Penambahan (Additions):
- Button Change Log di pengaturan untuk melihat catatan rilis

Perubahan (Changes):
- UI baru di menu Waktu Sholat, support zoom in/out
- Logo halaman depan diganti Nusantara Astronomical Laboratory (NAL)

Perbaikan (Fixes):
- Perbaikan kecil

NB: Hasil hisab dengan metode Ad-Durrul Aniq untuk target di bawah tahun 1411 H akan tidak sesuai dikarenakan:
Data tabel pada program Ad-Durrul Aniq masih belum lengkap, yaitu:

1. di tabel jadwal harokat sinin majmuah litholabil ijtima hal 156 dari tahun 420 sampai 1380 belum ditambahkan
2. di tabel jadwal harokat fi sinin majmuah li harokat syams wal qomar hal 166 dari tahun 0 sampai 1380 belum ditambahkan

Kekurangan data tabel tersebut akan ditambahkan seiring waktu.
Untuk target tahun 1411 H keatas InshaAlloh aman.
