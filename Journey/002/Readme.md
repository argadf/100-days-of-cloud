# Chapter 2 & 3
## Chapter 2
- Dasar-Dasar Harga
- Total Biaya Kepemilikan
- AWS Organization
- Dukungan Teknis

### Dasar-Dasar Harga
#### Tiga pendorong dasar biaya dengan AWS :
##### Komputasi
- Biaya per jam atau detik
- Bervariasi sesuai tipe instans
##### Penyimpanan
- Biaya per GB
##### Transfer data
- Data keluar dijumlahkan dan dikenai biaya
- Data masuk tidak dikenai biaya dengan beberapa pengecualian
- Biaya per GB

#### Cara membayar AWS
- Bayar sesuai yang anda gunakan
- Bayar lebih sedikit ketika melakukan pemesanan
- Bayar lebih sedikit ketika menggunakan lebih banyak
- Bayar jauh lebih sedikit seiring berkembangnya AWS

#### Layanan tanpa biaya
- Amazon Virtual Private Cloud (Amazon VPC)
- AWS Identity and Access Management (IAM)
- AWS Elastic Beanstalk
- AWS CloudFormation
- AWS OpsWorks

#### Poin-poin penting
Tidak ada biaya untuk :
- Transfer data masuk
- Transfer data antarlayanan dalam wilayah AWS yang sama
- Bayar sesuai yang anda gunakan (Pay as you go)
- Mulai dan berhenti kapan saja
- Tidak memerlukan kontrak jangka panjang
- Beberapa layanan disediakan secara gratis, tetapi layanan AWS lainnya yang mereka sediakan mungkin tidak gratis

### Total Biaya Kepemilikan
Total biaya kepemilikan (TCO) adalah perkiraan keuangan untuk membantu mengidentifikasi biaya langsung dan tidak langsung dari suatu sistem.

#### Mengapa menggunakan TCO?
- Untuk membandingkan biaya menjalankan seluruh lingkungan infrastruktur atau beban kerja spesifik on-premise versus AWS
- Untuk membuat anggaran dan membangun kasus bisnis untuk berpindah ke cloud

#### Pertimbangan TCO
![tco](https://github.com/argadf/100-days-of-cloud/assets/140805970/7d95ddd6-1d60-42c2-abbd-e8069c235857)

#### Beberapa biaya terkait manajemen pusat data meliputi :
- Biaya server untuk peringkat keras dan perangkat lunak, serta biaya fasilitas untuk menyimpan peralatan
- Biaya penyimpanan untuk perangkat keras, administrasi, dan fasilitas.
- Biaya tenaga kerja IT yang diperlukan untuk mengelola seluruh solusi

#### Pertimbangan manfaat tambahan
##### Manfaat langsung
- Mengurangi pengeluaran komputasi penyimpanan, jaringan, keamanan
- Pengurangan pembelian perangkat keras dan perangkat lunak
- Pengurangan biaya operasional, pencadangan, dan pemulihan bencana
- Pengurangan personel operasi
##### Manfaat tak langsung
- Menggunakan kembali layanan dan aplikasi yang memungkinkan anda menentukan dengan menggunakan layanan cloud yang sama
- Peningkatan produktivitas developer
- Peningkatan kepuasan pelanggan
- Proses bisnis yang tangkas dan dapat menanggapi peluang baru yang muncul dengan cepat
- Peningkatan pada jangkauan global

### AWS Organization
AWS Organization adalah layanan manajemen akun yang memungkinkan anda menggabungkan beberapa akun AWS ke sebuah organisasi yang anda buat dan kelola secara terpusat.

#### Manfaat utama AWS Organizations adalah :
- Mengelola kebijakan akses secara terpusat di beberapa akun AWS
- Mengontrol akses ke layanan AWS
- Mengautomasi pembuatan dan pengelolaan akun AWS
- Tagihan terkonsolidasi di beberapa akun AWS

#### AWS Organizations memungkinkan kita :
- Membuat service control policies (SCP) yang secara terpusat mengontrol penggunaan layanan AWS di beberapa akun AWS
- Membuat grup akun dan kemudian melampirkan kebijakan ke dalam grup untuk memastikan kebijakan yang benar diterapkan di seluruh akun tersebut.
- Menyederhanakan pengelolaan akun menggunakan antarmuka pemrograman aplikasi (API) untuk mengautomasi pembuatan dan pengelolaan akun AWS baru.
- Menyederhanakan proses penagihan dengan menyiapkan metode pembayaran tunggal untuk semua akun AWS di organisasi anda.

#### Keamanan dengan AWS Organizations :
- Kontrol akses dengan AWS Identity and Access Management (IAM)
- Kebijakan IAM memungkinkan anda mengizinkan atau menolak akses ke layanan AWS untuk pengguna, grup, dan peran
- Service control policies (SCP) memungkinkan anda mengizinkan atau menolak akses ke layanan AWS untuk akun individu atau grup di unit organisasi (OU)

#### AWS Support
##### Menyediakan kombinasi alat dan keahlian yang unik :
- AWS Support
- Paket AWS Support
##### Dukungan disediakan untuk
- Bereksperimen dengan AWS
- Penggunaan produksi AWS
- Penggunaan AWS untuk bisnis penting


## Chapter 3
### Infrastruktur Global AWS
- Region AWS adalah daerah geografis
  - Replikasi data di seluruh wilayah dikendalikan oleh anda
  - Komunikasi lintas wilayah menggunakan infrastruktur jaringan backbone AWS
- Setiap region AWS menyediakan redundansi dan konektivitas penuh ke jaringan
- Region biasanya berisi dua atau lebih Availability Zone 
- AWS memiiki 22 region di seluruh dunia

#### Menentukan region yang tepat berdasarkan :
- Tata kelola data, persyaratan hukum
- Kedekatan dengan pelanggan (latensi)
- Layanan yang tersedia
- Biaya (bervariasi berdasarkan region)

#### Availability Zone
- Setiap wilayah memiliki beberapa Availability Zone
- Setiap Availability Zone adalah partisi yang sepenuhnya terisolasi dari infrastruktur AWS
  - Saat ini terdapat 69 Availability Zone di seluruh dunia
  - Availability Zone terdiri dari pusat data berlainan
  - Dirancang untuk mengisolasi kesalahan
  - Saling tersambung dengan Availability Zone lainnya menggunakan link pribadi berkecepatan tinggi
  - Anda dapat memilih Availability Zone milik anda
  - AWS merekomendasi untuk mereplikasi data dan sumber daya di seluruh Availability Zone demi ketahanan

#### Pusat data AWS
- Pusat data AWS dirancang demi keamanan
- Pusat data adalah tempat data berada dan pemrosesan data terjadi
- Setiap pusat data memiliki daya, jaringan, dan konektivitas berlebih, dan ditempatkan di fasilitas yang terpisah
- Pusat data biasanya memiliki 50.000 sampai 80.000 server fisik

#### Points of Presence
- AWS menyediakan jaringan global 187 lokasi Points of Presence 
- Terdiri dari 176 edge location dari 11 Cache edge Regional
- Digunakan dengan Amazon CloudFront (Jaringan penyampaian konten global, yang menyediakan konten kepada pengguna akhir dengan mengurangi latensi)
- Cache edge Regional digunakan untuk konten dengan akses jarang

#### Poin Penting
- Infrastruktur Global AWS terdiri dari Region dan Availability Zone
- Pilihan Region biasanya berdasarkan pada persyaratan kepatuhan atau untuk mengurangi latensi
- Setiap Availability Zone terpisah secara fisik dari Availability Zone lainnya dan memiliki daya, jaringan, dan konektivitas berlebih
- Edge location dan Cache edge regional meningkatkan kinerja dengan melakukan cache konten lebih dekat dengan pengguna

### Layanan AWS
- Komputasi
- Jaringan
- Penyimpanan

#### Kategori Layanan AWS
- Penyimpanan
  - Amazon Simple Storage Service (Amazon S2)
  - Amazon Elastic Block Store (Amazon EBS)
  - Amazon Elastic Sistem File (Amazon EFS)
  - Amazon Simple Storage Service Glacier
- Komputasi
  - Amazon EC2
  - Amazon EC2 Auto Scaling
  - Amazon Elastic Container Service (Amazon ECS)
  - Amazon EC2 Container Registry
  - AWS Elastic Beanstalk
  - AWS Lambda
  - Amazon Elastic Kubernetes Service (Amazon EKS)
  - AWS Fargate
- Basis Data
  - Amazon Relational Database Service
  - Amazon Aurora
  - Amazon Redshift
  - Amazon DynamoDB
- Layanan dan Penyampaian Konten
  - Amazon VPC
  - Elastic Load Balancing
  - Amazon CloudFront
  - AWS Transit Gateway
  - Amazon Route 53
  - AWS Direct Connect
  - AWS VPN
- Keamanan
  - AWS Identity and Access Management (IAM)
  - AWS Organizations
  - Amazon Cognito
  - AWS Artifact
  - AWS Key Management Service
  - AWS Shield
- Biaya
  - Laporan Penggunaan & Biaya AWS
  - AWS Budgets
  - AWS Cost Explorer
  - Manajemen & Tata Kelola
  - AWS Management Console
  - AWS Config
  - Amazon CloudWatch
  - AWS Auto Scaling
  - AWS CLI
  - AWS Trusted Advisor
  - AWS Well-Architected Tool
  - AWS CloudTrail

## Modul Pemeriksaan Pengetahuan
### Modul 2
![modul-2-tes](https://github.com/argadf/100-days-of-cloud/assets/140805970/0acf785b-8106-4a7b-a5c6-3039d3c921a5)

### Modul 3
![modul-3-tes](https://github.com/argadf/100-days-of-cloud/assets/140805970/547377b1-edee-47b1-af8d-7864a75e8a94)

