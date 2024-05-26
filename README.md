# capstoneModule3
Capstone Project Module 3, JCDSOL-013(B), Roberto Benedict

## Deskripsi
Proyek python dalam ipynb ini merupakan pembuatan model Machine Learning untuk memprediksi customer churn pada bidang e-commerce. Sebuah perusahaan yang bergerak di bidang E-commerce ingin mengurangi jumlah customer yang berpotensi untuk churn. Churn yang dimaksud adalah keadaan seorang customer yang berhenti menggunakan produk atau jasa perusahaan, dalam hal ini berupa platform E-commerce perusahaan. Berhenti menggunakan dapat mengimplikasikan kekecewaan customer maupun customer yang lebih memilih produk competitor. Perusahaan ingin mengetahui kandidat customer churn. Hal ini dapat membantu perusahaan dalam menyusun strategi minimalisasi customer churn seperti dengan mengurangi biaya promosi dengan alokasi biaya yang lebih fokus terhadap kandidat customer churn. Informasi mengenai customer didapatkan dari data pendaftaran dan transaksi historikal customer. 

**Target :**  

* 0 : Tidak churn
* 1 : Churn

## Pernyataan Masalah
Customer churn berkaitan langsung dengan pendapatan perusahaan, oleh karena itu adalah sangat penting untuk meminimalisasi customer yang kemungkinan akan churn berdasarkan ciri tertentu. Perusahaan perlu melakukan sebuah kategorisasi customer yang kemungkinan akan churn sehingga sumber daya, waktu, maupun anggaran dapat dialokasikan dengan efisien dan efektif terhadap kategori customer yang berpotensi churn tersebut dalam upaya mencegah customer-customer tersebut melakukan churn. Alokasi yang dimaksud dapat berupa anggaran promosi yang fokus terhadap customer yang berpotensi untuk churn. Jika dibandingkan dengan anggaran promosi untuk semua customer, tentunya ada porsi anggaran yang kurang tepat guna, yaitu alokasi anggaran promosi yang sama untuk customer yang tidak berpotensi untuk churn.

## Analytic Approach
Analisis data customer akan dilakukan untuk menemukan pola tertentu yang dapat membedakan customer yang berpotensi akan churn atau tidak. Tahap selanjutnya, model klasifikasi akan dibuat untuk membantu perusahaan agar dapat melakukan prediksi kemungkinan seorang customer akan melakukan churn atau tidak.

## Tujuan
Jika dibandingkan dengan biaya promosi untuk semua customer, tentu akan ada biaya yang bisa dihemat jika alokasi biaya difokuskan untuk customer churn saja atau alokasi yang lebih kecil untuk customer yang tidak berpotensi churn.
Dengan mempertimbangkan masalah tersebut, perusahaan ingin memiliki kemampuan untuk memprediksi potensi seorang customer akan melakukan churn atau tidak. Setelah mengatahui prediksi customer yang akan churn, perusahaan dapat memfokuskan alokasi anggaran promosi kepada para customer tersebut. 
Tentunya, untuk jangka panjang, perusahaan tertarik untuk mengetahui tentang karakteristik atau faktor tertentu yang membuat customer melakukan churn atau tidak. Hal ini dapat digunakan untuk merencanakan strategi pendekatan atau reaching out terhadap customer yang berpotensi churn.

## Stakeholders
1. Perusahaan E-Commerce
2. Customer / Pelanggan

## Alur Machine Learning
Berikut uraian alur program ipynb.
1. Data Cleaning
2. Data Analysis
3. Data Preparation
4. Modeling dan Evaluasi
5. Penarikan kesimpulan dari insight yang didapat

## Kesimpulan
Berdasarkan hasil classification report dari model, dapat disimpulkan jika model digunakan untuk prediksi list customer yang akan churn, maka model ini dapat mengurangi 93% customer yang berpotensi loyal atau tidak churn untuk tidak perusahaan fokuskan dalam alokasi biaya promosi atau bahkan bisa ditiadakan, dan model ini mendapatkan 78% customer yang churn dari seluruh customer churn berdasarkan recall.

Model ini memiliki presisi prediksi customer yang churn sebesar 70%. Hal ini berarti setiap kali model memprediksi bahwa seorang customer akan churn, kemungkinan tebakannya benar itu sebesar kurang lebih 70%. Oleh karena itu, masih ada False Positive atau akan ada customer yang sebenarnya tidak churn tetapi diprediksi model sebagai customer yang churn sebanyak 7% dari keseluruhan customer yang tidak churn berdasarkan recall.

Bila diandaikan biaya promosi per customer itu 50 USD dan jumlah customer dalam suatu kurun waktu sebanyak 200 orang di mana 100 orang churn, maka dalam kasus bisnis bisa dihitung sebagai berikut :

Tanpa Model (semua customer dianggap potensi churn dan ditawarkan promosi) :
- Total Biaya promosi = 200 x 50 USD = 10,000 USD
- Biaya yang terbuang = 100 x 50 USD = 5,000 USD
- Jumlah penghematan = 0 USD

Dengan Model (hanya customer yang diprediksi oleh model churn yang kita check dan tawarkan) :
- Total Biaya promosi = (78 x 50 USD) + (7 x 50 USD) = 3050 USD + 760 USD = 4,250 USD
- Biaya yang terbuang = (100-(78+7)) x 50 USD = 750 USD 
- Jumlah penghematan = 10,000 - 4,250 = 5,750 USD

Berdasarkan contoh hitungan sederhana tersebut, terlihat bahwa dengan menggunakan model klasifikasi dan memprediksi berapa banyak porsi customer yang kemungkina churn, maka perusahaan tersebut dapat menghemat biaya yang cukup besar tanpa mengorbankan terlalu banyak customer yang churn.


## Rekomendasi
Hal-hal yang bisa dilakukan untuk developer untuk mengembangkan proyek dan modelnya :
1. Membuat kebijakan dan sistem penjagaan input yang mendorong setiap kandidat untuk mengisi semua data yang diperlukan.
2. Memberi opsi input untuk yang memang tidak ada atau nol.
3. Menambahkan fitur baru yang kemungkinan bisa berhubungan dengan churn, seperti informasi yang terkait dengan pembayaran order dan deskripsi lain customer.
4. Mencoba algoritma ML lain dan melakukan hyperparameter tuning yang lebih advanced.
5. Mencoba grid search untuk metode fill pada cleaning.
6. Menganalisa data yang model masih salah tebak untuk mengetahui karakteristik data tersebut, yang pada akhirnya akan dialurkan untuk menambah fitur atau feature engineering lagi.

Rekomendasi terhadap stakeholder atau perusahaan :
1. Memperbanyak survey demi pengumpulan data yang lebih banyak secara volume maupun lebih beragam.
2. Menawarkan promosi atau strategi lain yang menawarkan sebuah insentif pada customer atau pelanggan agar tertarik dan tidak churn.
3. Berdasar feature importance, cashback dapat ditingkatkan untuk customer yang berpotensi untuk churn.
4. Customer yang memiliki tujuan pengiriman jauh dapat diberi promo agar dapat mengurangi churn akibat alasan terkait seperti biaya delivery mahal ataupun lamanya delivery.
5. Berdasarkan Tenure, perusahaan dapat mengadakan strategi marketing yang mendorong insentif untuk orang yang baru-baru memesan.

<br/>
Copyright &copy; 2024, Roberto Benedict.
