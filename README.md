# Writing-Test-Week7
Writing Test Week 7

**Senin, 7 November 2022**
### Sequelize


#### Sequelize
- ORM atau Object Relational Mapping adalah teknik memetakan object perangkat lunak ke tabel database tanpa harus menulis query basis data apapun,orm juga mampu mendukung banyak database seperti Postgree,MYSQL,SQLite, dll
- cara menggunakan sequelize ada 2 yaitu :
1. Tanpa Migration Jika tanpa menggunakan migration maka kita bisa melakukan install 
a. npm install --save sequelize
b. npm install --save mysql2 (tergantung menggunakan db apa) untuk selanjutnya dapat dilihat di link yang sudah tercantum di atas
2. Dengan Migration Migration adalah menyimpan history perubahan pada table yaitu dengan cara setiap create/hapus/edit kolom otomatis disimpan perubahan dan bisa balik lagi ke versi tabel sebelumnya dengan menggunakan undo adapun untuk tahapan migration 

#### Associate
- Associate atau yang biasa kita sebut relation berfungsi untuk menghubungkan satu tabel dengan tabel lainnya adapun beberapa argumen Association sebagai berikut :
1. hasOne(one to one),perbedaan dengan belongsTo adalah kunci asing(FK) akan ditentukan pada model target dapat dilakukan dengn cara menambahkan kunci asing ke target dan mixin asosiasi tunggal ke sumbernya.
2. belongsTo(one to one),dapat dilakukan dengan cara menambahkan kunci asing dan campuran asosiasi tunggal ke sumbernya.
3. hasMany(one to many),dapat dilakukan dengan cara menambahkan kunci asing ke target dan campuran asosiasi jamak ke sumbernya.
4. belongsToMany(Many to Many),dapat dilakukan dengan cara membuat asosiasi N:M dengan tabel gabungan dan menambahkan mixin asosiasi jamak ke sumbernya. Tabel persimpangan dibuat dengan sourceId dan targetId.\


**Selasa, 8 November 2022**
### MongoDB

- MongoDB adalah salah satu database open source NoSQL yang cukup populer. 
- MongoDB sering dipakai untuk aplikasi berbasis Cloud, Big Data maupun Grud Computing
- Pada SQL menyimpan data menggunakan relasi tabel, sedangkan pada MongoDB menggunakan dokumen dengan format JSON
- NoSQL sendiri artinya bisa mengolah database dengan fleksibel dan tidak membutuhkan query yang dimana kita memiliki skalabilitas yang tinggi sesuai dengan perkembangan data kita

1. Kelebihan
a. Sistem tidak membutuhkan tabel
b. Tidak perlu menggunakan tabel yang terstruktur
c. By Default sudah menggunakan JSON sehingga memudahkan integrasi dengan JavaScript
d. Perfoma lebih cepat dengan kemampuan menampung banyak data yang bervariasi

2. Kekurangan
- Tidak mendukung transaksi
- Masalah konsistensi data
- Menggunakan banyak memory
- Hanya bisa menampung maksimal 16MB setiap dokumen

##### Anatomi komponen dari Database MongoDB
- Database adalah wadah untuk menyimpan berbagai macam Collection
- Collection adalah tempat kumpulan dari berbagai macam dokumen, sehingga collection sering disamakan dengan tabel pada SQL
- Document adalah unit terkecil yang berada pada MongoDB


##### Schema Mongodb
Desain schema mongoDB bekerja sangat berbeda dari desain skema relasional seperti mysql,dengan desain ini maka mongodb :
- Tidak ada proses formal
- Tidak ada algoritma
- Tidak ada peraturan khusus




**Rabu, 9 November 2022**
### Mongoose

#### MongoDB
- MongoDB adalah salah satu produk database noSQL Open Source yang menggunakan struktur data JSON untuk menyimpan datanya
- MongoDB sering dipakai untuk aplikasi berbasis Cloud, Grid Computing, atau Big Data


#### Mongoose
- Mongoose adalah library yang bisa dibilang sebagai Object Modelling MongoDB untuk NodeJS
- Mongoose bisa digunakan untuk mengelola hubungan antar data, menyediakan validasi
- Bisa juga digunakan untuk menerjemahkan antar objek dalam kode dan representasi Objek tersebut di MongoDB


#### Populate
- Populate ada kaitannya dengan relasi database
- Populate adalah proses penggabungan 2 collection atau lebih menjadi satu objek JSON



**Kamis, 10 November 2022**
### Docker

- Docker adalah software yang menjalankan suatu aplikasi menggunakan container
- Aplikasi yang berjalan didalam container docker tidak berpengaruh oleh faktor luar karena terisolasi
- Docker berfungsi sebagai penyedia layanan virtual bagi aplikasi yang diinstall pada sebuah host
- Docker akan menyediakan hal-hal yang diperlukan untuk aplikasi mulai dari akses file, koneksi internet, hingga port agar aplikasi dapat berjalan dengan mulus
- Cara kerjanya adalah Docker men-sharing kernel dari host OS serta melakukan atau membuat container suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja serta bersifat terisolasi sehingga tidak terpengaruh oleh faktor luar.

##### perintah dasar docker
- melihat image `$ docker images`
- Download Images `$ docker pull [option]`
- melihat Docker containe yang running `$ docker cotainer ls`
- Membuat docker container `$ docker container create --name`
- Mencari images `$ docker search name_find`
- Menghapus container `$ docker container rm name`
- mengetahui version docker `$ docker --version[option]`
- Membuat container dari image `$ docker run [options] image [command] [arg...]`
- melakukan push dari image/repo ke registry `$ docker push [option]`


