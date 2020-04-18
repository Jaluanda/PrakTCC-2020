# PrakTCC-2020
Kumpulan berkas ajar Praktikum Teknologi Cloud Computing UPN "Veteran" Yogyakarta
T.A. Semester Genap 2019/2020

# Agenda Praktikum
Berikut agenda praktikum **yang terbaru** untuk Praktikum TCC berdasarkan hasil dari Surat Edaran dan pembahasan Tim Koordinator Praktikum TCC:
- ~~Pertemuan 6 (11 - 13 Maret): Kelanjutan FreeNAS dan Penyampaian Project~~
- ~~Pertemuan 7 (1 - 3 April): Submisi Progress Project 1~~
- ~~Pertemuan 8 (15 - 17 April): Revisi Laporan dan Melanjutkan Project~~
- Pertemuan 9 (29 - 30 April ~ 1 Mei): Submisi Progress Project 2 (hasil dari revisi Pertemuan 7)
- Pertemuan 10 (6 - 8 Mei): Revisi Laporan dan Melanjutkan Project
- Pertemuan 11 (13 - 15 Mei): Submisi Final Project dan Presentasi Online
- Pertemuan 12 (sesuai jadwal UAS di CBIS): Administrasi UAS (berita acara, pernyataan kejujuran, dsb.)

# Bantuan untuk Project Akhir
## Topologi
Berikut contoh pembuatan topologi untuk Proyek Akhir, dapat dikreasikan sendiri namun harus jelas (konten, tulisan, garis pembatas, objek cloudnya).
![Topologi Arsitektur](https://i.imgur.com/FjJ4odz.png) 
![Topologi Sistem](https://i.imgur.com/AW3P2BA.png) 
![Topologi Jaringan](https://i.imgur.com/m5GPgG1.png) 

## FreeNAS
Contoh yang sederhana untuk pemanfaatan Ubuntu LAMPP dengan integrasi File Storage pada FreeNAS adalah menggunakan modul FTP/SCP/SFTP (mirip seperti Samba).
1. Mengkonfigurasi penyimpanan pada FreeNAS seperti biasa (datastore, user, group, dst.)
2. Mengaktifkan modul/service pada FreeNAS untuk layanan FTP.
3. Mengubah kodingan/sistem di Ubuntu LAMPP, semisal pengambilan foto profil:
	- Foto profil yang sebelumnya di Ubuntu LAMPP dipindah ke FreeNAS. Tidak ada foto profil di Ubuntu LAMPP.
	- Menambahkan kodingan sedikit. Konsepnya ialah foto di FreeNAS di ambil (download) ke Ubuntu terlebih dahulu dengan FTP (misal ditaruh di folder image), kemudian baru ditampilkan ke user. Jadi bukan foto dari FreeNAS langsung ditampilkan ke user, salah.
	- Foto yang diambil bersifat sementara, jadi setelah ditampilkan maka dihapus. Atau setiap kali menampilkan foto profil, foto yang ada saat ini dihapus dulu, atau langsung dapat ditimpa yang baru.
4. Contoh lainnya dapat menyesuaikan. Namun pada prinsipnya adalah: User Akses -> Sistem Ubuntu LAMPP -> FTP ke FreeNAS -> Mendapatkan berkas (download via FTP) ke Ubuntu LAMPP -> Ditampilkan/Filestream/Mode Download ke User.
5. Referensi dapat dilihat di:
	- Dokumentasi CodeIgniter: https://codeigniter.com/userguide3/libraries/ftp.html
	- Dokumentasi Laravel: https://laravel.com/docs/7.x/filesystem
	- Blog pribadi: https://arjunphp.com/uploading-file-via-ftp-using-codeigniter/
	- Blog pribadi: https://garrettstjohn.com/articles/ftp-download-codeigniter-library/
	- dan dapat menggunakan library 3rd party/library custom.

## Docker
Contoh pembuatan Docker:
- Setengah proses pembuatan ada pada Modul Praktikum. Namun harap disesuaikan kembali, tidak harus menggunakan yang ada di modul.
- Panduan tutorial Digital Ocean: https://www.digitalocean.com/community/tutorials/how-to-set-up-laravel-nginx-and-mysql-with-docker-compose
- Panduan dari blog pribadi: https://linuxhint.com/lamp_server_docker/

## Lainnya
- Yang perlu diperhatikan ialah bilamana mencari tutorial, pastikan sama versi Ubuntu yang digunakan dengan yang ditunjukkan di tutorial. Bilamana berbeda mungkin akan ada kendala, atau dapat diteruskan namun disesuaikan perintah-perintah yang digunakan.
- Selalu backup VM sebelum mengutak-atik VM lebih lanjut. Bilamana salah konfigurasi, VM dapat rusak dan tidak dapat digunakan lagi. Cara paling cepat memperbaiki ialah gunakan VM backup yang sudah dibuat sebelumnya.
- Bilamana menemukan kendala, silakan dicoba disolusikan sendiri. Bilamana berhasil dapat dimasukkan ke laporan untuk tambahan penilaian, dibuat sendiri sub bab-nya dan diletakkan di tempat yang sesuai.

## Perihal Kelompok
- Bilamana terdapat anggota kelompok yang dirasa menghambat dan tidak dapat ditolerir lagi, dapat menghubungi saya (Jalu) untuk konsultasi lanjut.
- Bilamana terdapat kendala masalah komunikasi antar anggota hingga menghambat progress pengerjaan (misal kondisi ekonomi tidak dapat membeli paket data, kondisi laptop yang sangat tidak memungkinkan, dan semua usaha lainnya sudah maksimal), sehingga tidak mungkin dikerjakannya project akhir ini, hubungi saya (Jalu).

# INFORMASI TERBARU
## Rabu, 15 April 2020
Informasi perihal **hasil** submisi laporan **Progress Project 1**:
- Format penulisan laporan yang baru telah diupload dengan nama berkas `Format Laporan Cloud Computing v2`. Penulisan untuk Progress Project 2 dan seterusnya menyesuaikan berkas tersebut.
- Untuk progress pertama telah kami nilai dan hasilnya telah diupload di Repository ini. Hasilnya dapat dicek di folder `Progress Project 1` dan pilih kelas yang sesuai. Kemudian pilih nomor urut kelompoknya.
- Kami berikan waktu 2 minggu untuk memperbaiki penulisan format yang telah kami perbarui dan dilanjutkan pengerjaan sesuai target yaitu (minimal) 50% hasilnya sudah tertuang di Progress Project 2.
- Dengan demikian terdapat perubahan agenda dan dapat dilihat kembali di atas. Mohon untuk semua praktikan di praktikum ini dapat menyesuaikan kembali.
- Untuk hasil submisi kelas yang belum diupload di GitHub ini dapat dicek secara berkala.
- Tambahan info, untuk yang merasa kurang dalam hal presensi kehadiran (tidak hadir praktikum) semasa sebelum UTS dan melanjutkan dengan tidak mengumpulkan tugas yang kami berikan setelah UTS (Project Akhir) hingga terakumulasi kurangnya presensi kehadiran, maka nilai akhir kami beri E sesuai aturan praktikum. Cara penghitungan presensi kehadiran untuk Project Akhir dapat dilihat di informasi sebelumnya.

Tim Koordinator (Jaluanda Parama)

## Rabu, 8 April 2020
Informasi perihal submisi laporan **Progress Project 1**:
- Dikarenakan mayoritas tidak sesuai dengan ekspektasi format penulisan dan format yang kami berikan tidak cukup jelas, maka untuk agenda praktikum disesuaikan kembali. 
- Kami akan mempublish ulang format penulisan yang lebih jelas sebagai acuan untuk penulisan berikutnya.
- Laporan yang telah dikumpulkan tetap dapat dilanjutkan setelah menerima revisi dari kami dan menyesuaikan format penulisan berdasarkan format yang baru.
- Untuk laporan yang sudah ada saat ini akan dibagikan kembali minggu depan pada pertemuan kedelapan. 

Mohon maaf untuk kesalahan dalam penyampaian formatnya.

Tim Koordinator (Jaluanda Parama)

## Senin, 30 Maret 2020 (revised)
Informasi berikut berdasarkan *Petunjuk Teknis Pembelajaran dengan Model Daring...* yang telah dikeluarkan Kajur Teknik IF tertanggal 30 Maret 2020:

- **Agenda praktikum** TCC telah disusun dan dapat dilihat pada sub keterangan di atas.
- Dikarenakan penyampaian materi telah mencapai target capaian dan sesuai dengan standar minimal 6 kali pertemuan, untuk penyampaian materi berikutnya dalam bentuk **self-study** dengan hasil akhir Project Akhir. Untuk materi Docker diubah menjadi self-study.
- **Presensi praktikum** tetap berjalan dan sesuai dengan capaian pada setiap pertemuan. Contoh: bila mengumpulkan tugas maka mendapat nilai presensi dan dianggap hadir. Untuk pertemuan self-study/revisi laporan juga dilihat capaiannya secara subjektif berdasarkan progress project.
- Untuk memberikan hasil dan nilai yang maksimal, maka terdapat tambahan yaitu **Progress Project 2** (capaian minimal 50%).
- Perihal **Administrasi UAS** akan disampaikan dikemudian hari berdasarkan format dari Tim Koordinator Asisten.

### Perihal Submisi Progress Project 1
Berikut informasi mengenai submisi **Progress Project 1**:
- Submisi **Progress Project 1** melalui e-mail: `jaluandaparama@gmail.com`
- CC (jangan lupa): `muhammadimamalfatah@gmail.com` atau `wahyu_aji11@rocketmail.com` tergantung asisten kelasnya sesuai CBIS/jadwal semula.
- Subjek `Kelas_Kelompok_ProgressTCC1` (Contoh: A_1_ProgressTCC1)
- Lampirkan laporan dalam bentuk PDF yang telah dikerjakan dengan format nama berkas `Kelas_Kelompok_ProgressTCC1.pdf`
- Berikan keterangan singkat sejauh mana pengerjaan yang telah dilakukan dan kendalanya, dalam bentuk isian (body) email (tulisan biasa)
- **Tidak sesuai format auto-delete e-mail**, setelah kirim e-mail pastikan kembali telah sesuai format.

Batas pengumpulan **sebelum jadwal praktikum dimulai**. Dapat dikumpulkan mulai hari ini. Satu kelompok salah satu saja yang mengumpulkan.
Bentuk koreksi oleh asisten adalah dalam bentuk Comment, Highlight, atau Coretan di PDF dan akan dikirim kembali ke email pengirim maks. 1 minggu atau dipublish di Repository GitHub ini.

Tim Koordinator (Jaluanda Parama)

## Jum'at, 20 Maret 2020
Format laporan Proyek Akhir telah diunggah. Harap dapat diunduh dan dikerjakan sesuai petunjuk di laporan tersebut. Pengumpulan laporan tidak menggunakan GitHub, harap dipantau informasi berikutnya mengenai teknis pengumpulan Progress Project. Batas pengumpulan adalah sebelum jam praktikum dimulai. Contoh: Kelas E batas pengumpulan adalah sebelum jam 13:00 WIB. Lebih dari jam pengumpulan dianggap tidak menghadiri pertemuan Progress Project (tidak mendapatkan nilai kehadiran, nilai presentasi, dan nilai pada pertemuan).

Pengerjaan Progress Project **setidaknya** 25%, lebih dari itu lebih baik. Identitas harus sudah lengkap beserta Bab 1.
Selamat mengerjakan. #staysafe

Tim Koordinator (Jaluanda Parama)

## Rabu, 18 Maret 2020
Update terbaru mengenai informasi perkuliahan Praktikum Teknologi Cloud Computing berdasarkan hasil rapat koordinasi FTI (Senin, 16 Maret 2020; 12:30WIB) terkait Surat Edaran (SE) No. 9/UN62/SE/TA.05.14/2020 terutama pada klausa praktikum/akademik adalah:

- Kegiatan Praktikum Teknologi Cloud Computing untuk pertemuan ketujuh (sesudah UTS) sampai dengan seterusnya (praktikum berakhir) adalah **tetap ada**, namun dilakukan secara daring (online classroom) atau pembelajaran jarak jauh (PTTM).
- Tidak ada presentasi (Progress Project dan Final Project) secara tatap muka. **Bentuk presentasi diubah** menjadi dalam bentuk teks tertulis (laporan soft copy dan hard copy), dalam bentuk audio visual (video pemaparan project), dan berkas pendukung (VM/konfigurasinya).
- Seperti yang telah dijelaskan pada pertemuan pertama, definisi dari Responsi (UAS) di Praktikum Teknologi Cloud Computing adalah **Project Akhir**.
- Tim Koordinator Praktikum Cloud Computing akan terus memantau bilamana terdapat peraturan terbaru yang dikeluarkan pihak kampus dan akan mengubah aturan ataupun informasi yang telah disampaikan di sini.
- Informasi yang telah **disampaikan sebelumnya tetap berlaku** hingga dikeluarkan informasi berikutnya yang menyatakan informasi tersebut tidak berlaku lagi.
- Berkas pendukung untuk pengerjaan Project Akhir (Format Laporan, dsb.) akan segera di sampaikan di GitHub, mohon selalu dipantau.

Tim Koordinator (Jaluanda Parama)

## Senin, 16 Maret 2020
Menanggapi beberapa hal terkait pelaksanaan Praktikum Teknologi Cloud Computing berdasarkan Surat Edaran (SE) No. 9/UN62/SE/TA.05.14/2020 yang dikeluarkan oleh pihak kampus maka:

- Tim Koordinator Praktikum Cloud Computing masih menunggu hasil rapat dari Prodi dan Ka. Lab. perihal kegiatan praktikum/perkuliahan setelah UTS.
- Bahwa pada prinsipnya, Proyek Akhir yang telah disampaikan **tetap dikerjakan** dan tidak ada pembatalan.
- Jadwal presentasi perihal Progress Project adalah **tetap sesuai jadwal**. Teknis mengenai presentasi diubah menjadi pengumpulan secara online.
- Perihal pertemuan berikutnya dan tahapan administrasi setelah Progress Project akan disampaikan di waktu mendatang berdasarkan hasil rapat.
- Informasi berikut **hanya berlaku untuk Praktikum Teknologi Cloud Computing** T.A. 2019/2020 di semua kelas praktikum tersebut.
- Diharapkan untuk dapat mengikuti informasi terbaru perkembangan perkuliahan Praktikum Teknologi Cloud Computing hanya pada GitHub ini. Bilamana terdapat update terbaru dari pihak kampus yang berkaitan dengan pelaksanaan praktikum ini, maka akan segera disampaikan di sini.

Tim Koordinator (Jaluanda Parama)
