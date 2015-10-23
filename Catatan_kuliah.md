# Instalasi Drupal

1 Download Drupal CORE from drupal website,  in this class we will used drupal version 7.39 (https://www.drupal.org/)
2 Extract drupal code in your LOCAL apache web server.    XAMPP: under 'htdocs' folder, WAMP: under 'www' folder. example:
	'C:\wamp\www\class'  
3 to access drupal locally used the following link:    http://localhost/class/drupal-7.39


# Pertemuan-03

## Manajemen USER

meliputi: Create, delete & Edit user, Update Status, Searching

1 login sebagai administator
2 Click menu 'people' (Manage user, roles, and permission)
3 Terdapat tiga jenis kelompok user :
	* Administrator  : user yang memiliki hak untuk mengatur keseluruhan sistem
	* Registered user: user yang secara resmi terdaftar dalam sistem
	* anonymous user: public user, tidak memiliki account dalam sistem kita.
4 Membuat user baru:
	* Click menu  '+Add user' 
	* masukan informasi USERNAME, EMAIL, PASSWORD, status(block atau active), roles(Registered user, Administrator), Notify user (kirim email ke user baru jika user sudah di tambahkan).
	* tekan 'SAVE'

5 Mengatur 'permission' (hak akses) untuk 'Registered User'

## Menambah CONTENT
CONTENT (konten) adalah data/informasi yang akan di tampilkan dalam web site. Drupal memilik dua jenis KONTEN, yaitu 
* ARTICLE (Digunakan untuk konten yang memiliki inforasi histori, contoh: Berita harian, event rutin dll)
* Basic PAGE (untuk halaman web yang tidak memiliki informasi tentang waktu)

Cara membuat content baru:

1 Login as Administrator
2 Click menu 'Content' (top bar)
3 Click menu '+Add content'
4 Memilih jenis konten (Article atau Basic Page)
5 masukan informasi yang diperlukan , Title (Judul), Tags (kata kunci), Body (Isi konten)
6 Lampirkan GAMBAR (image) jika perlu


### Tugas:

Re-Design (Merancang ulang) website ums (ums.ac.id)
a Rancangan tampilan (screenshoot), menu dsb, boleh menggunakan software DIA (Free opensource) (http://dia-installer.de/  ) .  Semua dokumen terkait di upload di http://github.com/[NIM]
b website dengan drupal untuk rancangan baru web site ums, diupload di FreeWeb Hosting, (www.idhostinger.com).  Menggunakan domain seperti berikut  http://[NIM].esy.es


## Jenis Content type:

1 Article  (default): Berbasis pada waktu (konten dimana waktu menajdi parameter penting)
2 Basic Page (default): Halaman web statik (waktu pembuatan tidak penting)
	
	Tiga jenis konten berikut sudah diinstall (by default) tetapi belum diaktifkan
	
	3. Poll : Angket online (survey)
	4. Blog : User's blog (Terikat pada user yang posting)
	5. Book Page: Ditampilkan deperti buku (dilengkapi dengan navigasi ke halaman yang lain, yang dibuat oleh sistem drupal secara automatis)
	6. Forum: Untuk forum diskusi antar user dalam sistem drupal



## ontoh membuat konten jenis Poll:

	1. Mengaktifkan module Poll:  Login sebagai admin > Module > tick pada modul 'Poll' > klik button 'Save Configure' (ada di bawah).
	2. Menambah konten baru: Menu 'Content' > '+ add content' > Pilih jenis konten 'Poll'
	3. Masukan Jenis pertanayaan pada isian form 'Question' (wajib)
	4. Masukan alternatif jawaban (by default ada 2, tetapi bisa di tambah sampai unlimited, dengan cara klik pada button 'More Choices')
	5. Jika diiingikan pada kolom sebelah kanan ('VOTE CONTENT') terdapat form untuk mengisi nilai awal dari setiap jawaban.
	6. Pilih jangka waktu 'Poll' ditampilkan (Poll Duration: 1 hari s/d 1 year)
	7. selanjutnya tekan button 'Save'
	
## Contoh Membuat Blog:

	1. Aktifkan module 'Blog' 
	2. Menambah 'Content Baru' dengan tipe 'Blog Entry'
	3. Drupal Secara automatis akan menampilkan posting baru pada Blog.
Note: Setiap user akan memiliki Blog-nya sendiri-sendiri

Link navigasi untuk mengakses posting tipe konten Blog dapat di aftifkan dari menu 'Structure>Block'

Contoh Membuat Book Page:

	1. Aktifkan Modul 'Book'
	2. Menambah content baru dengan tipe 'Book Page'
	

Materi kuliah akan di upload di sini:
https://github.com/handaga/drupal

Menambah bahasa Indnesia dalam drupal

	1. Download file bahasa indonesia di alamat berikut: https://localize.drupal.org/translate/languages/id
	2. Pilih Versi Drupal yang sesuai … drupal-7.39.id.po … letakan pada folder xx 
	3. Aktifkan module   .. Locale & Content Translation
	4. Masuk ke menu  … 'Configuration'>Languages
	5. klik menu 'Add Languages'



	1. Buat sebuah folder dengan nama sama dengan nama theme yang akan di buat, di bawah folder  ../sites/all/themes ..  contoh:  ` [drupal folder]/sites/all/themes/mytheme `  (hindari SPASI dalam memberi nama folder)
	
	2. Didalam folder baru tersebut buatlah sebuah file dengan nama ` mytheme.info `  
	3. Kemudian tuliskan baris-baris data berikut dalam file tersebut

	name = My theme
	description = Ini theme yang saya buat pertama
	core = 7.x
	
	; sub theme tambah baris berikut 
	base theme  = zen
	
	dengan menggunakan editor teks yang anda punya (NOTEPAD / NOTEPAD++)
	
	4. Simpan file
	5. Selanjutnya dapat dilakukan ujicoba untuk mengaktifkan theme dari menu ` Home > Administrator > Appearance `.
	6. Pilih theme ' MyTheme ` dan klik menu ` Enable and set default `

Membuat Subtheme dengan menggunakan template theme Zen 

	1. Download template theme Zen dari link berikut  .. http://drupal.org/project/zen .. kemudaian extract dalam folder  sites/all/themes/…
	2. copy folder sites/all/themes/zen/STATERKIT  dalam folder ` sites/all/themes/myzen `, kemudian lakukan beberapa modifikasi sebagai berikut:
	
	
	
	3. Dalam folder MyZen terdapat file  STARTERKIT.info.txt , rename menjadi 'myzen.info'.
	4. Open file ` myzen.info ` dan modifikasi bagian description dengan data berikut ' My Custom Zen sub-theme'.
	5. Buka file ` template.php ` dan gantikan kata ` STARTERKIT_` dengan ` MyZen_ ` gunakan fungsi replace dalam editor. 
	6. Ulangi langkah tersebut untuk file ` theme-settings.php  `
	7. Simpan file. 

TOOL untuk membantu proses pengembangan website dengan drupal

Module devel  "https://www.drupal.org/project/devel"


MID SEMESTER:

	1. System requirement
	2.  Setup & instalasi drupal 
	3. Fungsi2 utama drupal terkait CMS
	4. Istilah2 penting dalam drupal
	5. Ide aplikasi yang sesuai dengan Drupal.
	
	
lihat materi kuliah selengkapnya:
http://github.com/handaga/drupal
