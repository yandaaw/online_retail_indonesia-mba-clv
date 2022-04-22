# Online Retail Project
Project ini merupakan pembahasan mengenai market basket analysis dan customer lifetime value.

## What's Happening Here?
<p align="center">
  <img width="600" height="400" src="https://res.cloudinary.com/dyd911kmh/image/upload/f_auto,q_auto:best/v1530898580/Image_2_n05frc.png">
</p>

**Market basket analysis** adalah suatu metode analisa atas perilaku konsumen secara spesifik dari suatu golongan / kelompok tertentu. Sumber data dari market basket analysis antara lain dapat bersumber dari transaksi kartu kredit, kartu lotere, kupon diskon, panggilan keluhan pelanggan. Market basket analysis umumnya dimanfaatkan sebagai titik awal pencarian pengetahuan dari suatu transaksi data ketika kita tidak mengetahui pola spesifik apa yang kita cari. Kebutuhan market basket analysis berawal dari keakuratan dan manfaat yang dihasilkannya dalam wujud aturan assosiasi (association rules). Yang dimaksud dengan association rules adalah pola-pola keterkaitan data dalam basis data. <br><br>

<p align="center">
  <img width="800" height="500" src="https://lirp.cdn-website.com/97b2606f/dms3rep/multi/opt/customer+lifetime+value+%282%29-640w.jpg">
</p>

Sedangkan **Customer lifetime value** sering disebut sebagai nilai umur pelanggan. Dari pengertiannya, customer lifetime value merujuk pada nilai dari seorang konsumen terhadap sebuah brand selama ia menjadi pelanggan. Perlu diketahui jika customer lifetime value ini merupakan salah satu matriks yang bisa dilacak untuk mengukur seberapa berharganya konsumen dilihat dari rentang waktu ia berlangganan, yang dihitung dari pembelian pertama. Secara umum, customer lifetime value ini dapat membantu kita untuk mempertahankan konsumen yang ada. Sebab mendapatkan konsumen baru jauh lebih sulit dan membutuhkan waktu serta biaya lebih besar dibanding mempertahankan yang sudah ada. Selain itu, memahami customer lifetime value juga akan membantu bisnis Anda untuk mengembangkan strategi peningkatan penjualan sambil di sisi lain bisa mempertahankan margin keuntungan tetap stabil. Customer lifetime value ini sering disamakan dengan net promoter score (NPS), namun sebenarnya keduanya sangatlah berbeda sebab NPS hanya mengukur kepuasan pelanggan tanpa menghubungkannya dengan rentang waktu seorang konsumen dalam menjalin interaksi dengan brand Anda.

## Background
Pada dokumentasi kali ini, penulis hanya akan membahas mengenai proses-proses pada market basket analyisis saja. Untuk dokumentasi mengenai customer life time value bisa anda baca pada [**link berikut**](https://blog.usetada.com/id/apa-itu-customer-lifetime-value-dan-seberapa-penting-bagi-bisnis-anda#:~:text=Dalam%20bahasa%20Indonesia%2C%20customer%20lifetime,brand%20selama%20ia%20menjadi%20pelanggan.). 

## Outline
Analisis asosiasi atau association rule mining adalah teknik data mining untuk menemukan aturan assosiatif antara suatu kombinasi item (Mengetahui hubungan antara satu atribut dengan yang lainnya). Contoh aturan assosiatif dari analisa pembelian di suatu pasar swalayan contohnya adalah dapat diketahuinya berapa besar kemungkinan seorang pelanggan membeli roti bersamaan dengan susu. Dengan pengetahuan tersebut pemilik pasar swalayan dapat dengan mudah mengatur penempatan barangnya atau merancang kampanye pemasaran dengan memakai kupon diskon untuk kombinasi barang tertentu. Beberapa hal yang perlu diperhatikan dalam aturan assosiatif, diantaranya. Dua parameter berupa Support dan Confidence. Support atau nilai penunjang yang merupakan persentase kombinasi item tersebut dalam database sedangkan confidence atau nilai kepastian yaitu kuatnya hubungan antar item dalam aturan assosiatif. <br>

Market basket analysis merupakan suatu analisa atas perilaku konsumen secara spesifik dari suatu golongan / kelompok tertentu yang bersumber dari data transaksi penjualan barang, kartu kredit, kartu lotere, kupon diskon, maupun panggilan keluhan pelanggan. Market basket analysis umumnya dimanfaatkan sebagai titik awal pencarian pengetahuan dari suatu transaksi data ketika kita tidak mengetahui pola spesifik apa yang kita cari. Kebutuhan market basket analysis berawal dari keakuratan dan manfaat yang dihasilkannya dalam wujud aturan assosiasi (association rules). Yang dimaksud dengan association rules adalah pola-pola keterkaitan data dalam basis data. Data hasil proses market basket analysis dapat dimanfaatkan untuk menentukan product bundling maupun product placement dari toko retail maupun online yang kita miliki. 

## Dataset Information
Dataset yang digunakan dapat langsung di download pada link website [berikut](https://bit.ly/2USHhwA). Atau anda dapat mendownload file dataset pada repository ini. <br>
Berikut merupakan informasi tabel-tabel pada dataset yang digunakan :
- Variable-variable dalam dataset yang digunakan:
- InvoiceDate = Tanggal dan waktu pembelian barang
- BRANCH_SPLR = ID dari cabang suplier
- BRANCHNAME_SPLR = Merupakan kota cabang dari suplier
- warehouseProductsID = Merupakan kode Gudang stok dari sebuah barang
- BARCODEID = Merupakan kode barcode distribusi dari sebuah barang
- StockCode = Merupakan kode stok dari sebuah barang
- PRODUCT = Deskripsi dari produk
- PRODUCT_CATEGORY = Kategori dari produk
- Quantity = Jumlah barang yang dibeli pada sebuah transaksi
- UnitPrice = Harga per unit barang dalam satuan dolar
- UnitPriceRupiah = Harga per unit barang dalam satuan rupiah
- oldCUSTID = ID lama dari pelanggan
- CustomerID = ID dari pelanggan
- CUSTNAME = Nama dari pelanggan
- ADDRESS = Deskripsi alamat
- KOTA = Deskripsi kota
- PROVINSI = Deskripsi provinsi
- NEGARA = Deskripsi Negara
- CHANNELID_SPLR = ID dari suplier
- CHANNELNAME_SPLR = Jenis channel suplier
- SUBDISTID = ID dari distributor
- SUBDIST_NAME = Nama dari distributor

## Process Life Cycle
**1. Define Problem Statement**
- Ruang Lingkup yang digunakan adalah Product Purchases.
- Permasalahan yang ingin di selesaikan adalah membantu pihak retail dalam menentukan product bundling dan product placement dari data transaksi yang hendak digunakan.
- Algoritma yang digunakan adalah Algoritma apriori. Algoritma ini digunakan agar komputer dapat mempelajari aturan asosiasi, mencari pola hubungan antar satu atau lebih item dalam suatu dataset.

**2. Data Collection**
- Data collection merupkan proses pengumpulan data dari berbagai sumber internal maupun eksternal, dan memastikan bahwa informasi pada variable of interest (subjek yang akan dilakukan uji coba) pada data dapat digunakan secara sistematis yang memungkinkan seseorang dapat menjawab pertanyaan yang telah diidentifikasi sebelumnya.
- Dataset yang digunakan pada project ini merupakan data transaksi penjualan dan distribusi berbagai macam produk dari tangan supplier, distributor kepada kustomer.

**3. Data Modeling**
- Data modeling adalah hubungan berbagai elemen data berbeda untuk mengetahui informasi yang dibutuhkan serta menekankan pada data apa yang dibutuhkan dan apa yang akan dilakukan pada data tersebut untuk suatu keperluan bisnis.
- Pada data transaksi penjualan terdapat 4 variable utama yang akan digunakan dalam menyelesaikan project market basket analytics menggunakan algoritma apriori dengan aturan asosiasi, yaitu variable provinsi, Invoice No, Product Category dan Quantity.
- Konsep logika database yang digunakan dalam project ini di desain kedalam 3 thapan yaitu Conceptual Design, Logical Design, dan Physical Design. Penggambaran desain database ini dibuat berdasarkan aturan DBMS (Database management system).

**4. Data Quality Check and Remediation**
- Proses ini merupakan tahap yang berhubungan dengan mendiagnosis serta mengevaluasi masalah kualitas data. Proses ini dekat kaitannya dengan melakukan profiling terhadap data, memeriksa kualitas informasi yang terdapat pada data, mengidentifikasi dan menghilangkan informasi yang redudant atau kecatatan lainnya yang telah teridentifikasi sebelumnya.
- Pre-coding, beberapa library python yang wajib ada dan digunakan pada project ini diantaranya pandas, mlxtend, dan apyori.
- Data Pre-processing, merupakan proses mengubah data mentah atau biasa dikenal dengan raw data yang dikumpulkan dari berbagai sumber menjadi informasi yang lebih bersih dan bisa digunakan untuk pengolahan selanjutnya.

**5. Exploratory Data Analysis**
Secara definitive exploratory data analysis mengacu pada proses kritis dalam melakukan investigasi awal pada data untuk menemukan pola, untuk menemukan anomali, untuk menguji hipotesis dan untuk memeriksa asumsi dengan bantuan statistik ringkasan dan representasi grafis.

**6. Data mining**
- Setelah melakukan EDA, kita dapat lebih memahami kondisi dataset yang dimiliki. Sehingga, kita dapat memulai pembentukan model machine learning dengan lebih baik. Pembuatan model machine learning ini dapat masuk kedalam tahap data mining.
- Data mining sendiri adalah proses mencari pola atau informasi menarik dalam data terpilih dengan menggunakan teknik atau metode tertentu. Teknik, metode, atau algoritma dalam data mining sangat bervariasi. Pemilihan metode atau algoritma yang tepat sangat bergantung pada tujuan dan proses data mining secara keseluruhan.

**7. Data Communication**
- Proses pengiriman dan penerimaan data secara elektronik dari dua atau lebih alat yang terhubung kedalam sebuah jaringan (network) melalui suatu media.
- Interpretation / evalution yang merupakan pola informasi yang dihasilkan dari proses data mining perlu ditampilkan dalam bentuk yang mudah dimengerti oleh pihak yang berkepentingan. Tahap ini mencakup pemeriksaan apakah pola atau informasi yang ditemukan bertentangan dengan fakta atau hipotesis yang ada sebelumnya.

## Results and Conclusion
Dari result table yang telah di filter, dapat kita tarik kesimpulan bahwa produk-produk yang dibeli secara bersamaan oleh customer di daerah JAWA TENGAH terhadap rule asosiasi pada dataset dengan min_support 0.1 / 10%, min_threshold = 1, dan nilai lift sebesar lebih dari samadengan 1 serta tingkat confidence minimal yang diperhitungkan sebesar 0.8 (80%) diantaranya adalah:
- sabun, shampoo, obat-obatan, parfum dengan kosmetik.
- kosmetik, susu, obat-obatan dengan minuman.
- kosmetik, alat rumah tangga, minuman dengan sabun dan samphoo. <br>

Yang mana nilai conviction dari hasil-hasil yang didapat bernilai lebih dari 1, artinya hasil nilai rules yang dibangun dapat di anggap akurat. Kemudian sebagai tambahan, produk atau barang yang menjadi kombinasi produk pertama untuk frekuensi yang paling banyak adalah kosmetik, minuman, sabun dan samphoo.

Untuk dokumentasi market basket analysis pada project ini secara lengkap, dapat dibaca pada [Link Berikut](https://yandaafrida.medium.com/association-rule-market-basket-analysis-menggunakan-python-a9c49b4bfc69)
