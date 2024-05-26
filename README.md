# capstoneModule3
Capstone Project Module 3, JCDSOL-013(B), Roberto Benedict

## Deskripsi
Proyek python dalam ipynb ini merupakan pembuatan model Machine Learning untuk memprediksi customer churn pada bidang e-commerce.

## Pernyataan Masalah
1. Terdapat pola perilaku pelanggan tertentu yang menyebabkan kurang atau optimalnya pendapatan yang diperoleh.
2. Kesediaan armada dalam menjawab permintaan pelanggan pada waktu, tempat, dan rute populer adalah hal yang krusial dalam penyediaan servis transportasi.

## Tujuan
Sebagai *data scientist*, adapun pertanyaan yang penting untuk dijawab agar dapat menghasilkan rekomendasi bagi TLC New York City demi kepentingan stakeholder lainnya, yaitu :
1. Bagaimana karakteristik pola perilaku pelanggan ?
2. Bagaimana karakteristik pola trip pada waktu, tempat, maupun rute ?

## Stakeholders
1. Customer / Pelanggan
2. TLC New York City
3. Driver

## Alur Pengolahan Data
Berikut uraian alur program ipynb.
1. Data load dan basic info 
2. Data understanding
3. Data cleaning
4. Data analysis
5. Penarikan kesimpulan dari insight yang didapat

## Kesimpulan
1. Karakteristik pola perilaku pelanggan :
    * Sudah ada hampir 50% rute customer loyal dan best. Namun, hal sebaliknya juga benar bahwa terdapat setengah lagi potensi segmen market yang bisa dimanfaatkan jika ditinjau dengan rute pilihan pelanggan penumpang. Hal ini menjelaskan preferensi pelanggan terhadap rute populer yang kemungkinan besar potential customer akan pilih.
    * Tiga Rute paling populer pilihan customer, Manhattan-Manhattan, Queens-Queens, dan Brooklyn-Brooklyn mengindikasi bahwa customer punya preferensi untuk memilih rute inner Borough di ketiga kota besar NYC. Tentu jika kita cocokkan pada data sensus NYC, terlihat bahwa proporsi paling besar adalah Queens, Brooklyn, dan Manhattan. Namun, jika kita melihat density seperti pada tabel yang telah disusun Wikipedia dari berbagai data sensus, maka terlihat jelas Manhattan adalah yang terpadat dan didukung kontribusi GDP sangat besar. Hal tersebut punya makna aktivitas kota yang tinggi dan rute populer transportation service tentu akan mengikuti.
    * Interval jarak dan durasi yang memiliki paling banyak pelanggan trip adalah 0 - 1 jam dan 0 - 5 mil. Artinya pelanggan memiliki preferensi trip pendek dan cepat.
    * Hubungan jarak dan durasi terhadap  **Total Bayaran** adalah berbanding lurus. Jika ditinjau melalui korelasi, terlihat bahwa korelasi tinggi positif di atas 0.80 untuk keduanya terhadap **Total Bayaran**. Namun, karena count sedikit untuk interval trip panjang kemungkinan walaupun segi pendapatan tinggi, tapi dengan frekuensi yang sedikit akan cenderung lebih tidak stabil dalam pendapatan sepanjang waktu berlalu.
    * Jumlah trip sangat didominasi oleh penumpang tunggal, yang kemudian walaupun terdapat perbedaan cukup jauh diikuti oleh penumpang berdua. Hal ini berarti, penumpang lebih memilih untuk pergi dengan grup kecil di bawah 2.
    * Tambahan : Terdapat jumlah penumpang nol yang telah dibahas sekilas pada saat cleaning. Di sini kembali kita lihat dengan jumlah kedua terkecil, namun tetap ada di ratusan. Angka ini dapat dijelaskan oleh kesalahan input atau anomali praktik driver dan penumpang.
    * Metode pembayaran yang paling signifikan menurut banyak trip adalah Credit 63.9% dan Cash 35.8%. Hal ini juga berarti secara tersirat bahwa pembayaran tidak banyak terjadi masalah seperti terlihat pada tipe payment 3 sampai 6, di mana opsi 3 dan 4 tidak mencapai 1% dan metode pembayaran 5 dan 6 tidak ada sama sekali.
    * Tipe trip yang lebih banyak dipilih pelanggan adalah tipe 1, yaitu street-hail yang mencakup 99% total. Tentu dengan melihat terhadap sum total bayar, Dispatch tetap hanya mencakup di sekitar 1%.
    * Terdapat 48% atau hampir setengah pelanggan memberi tips.
    * Hanya hubungan korelasi moderat tips terhadap total bayaran sebesar 0.56.
    * Tips hanya tercatat pada pembayaran secara kredit. Namun, ada 1 entri secara cash yang merupakan human error atau machine error.

2. Karakteristik pola trip pada waktu, tempat, maupun rute :
    * Tempat pickup berpengaruh besar pada pendapatan ditinjau dari rata-rata total bayaran.
    * Waktu berpengaruh besar pada banyak trip dengan pola siklik mingguan sepanjang bulan Januari 2023, pola hari dalam minggu adalah menurun dengan minimum pada weekend, dan untuk pola jam harian memiliki maksimum di jam 15-18.
    * Waktu berpengaruh besar pada pendapatan ditinjau dari total bayaran dengan pola serupa dengan pola banyak trip untuk fungsi agregat sum. Sum dipilih untuk mewakili total pendapatan pada kurun waktu tersebut.
    * Rute paling populer sesuai dengan analisa RFM preferensi rute pelanggan.
    * Rute inner Borough memang lebih signifikan ditinjau secara count trip ataupun total bayaran dengan persentase 91% count trip dan 83% dari sum total bayaran.
    * Ditemukan waktu yang paling sibuk untuk rute paling populer adalah Afternoon (jam 12-18). Posisi kedua rute adalah Morning (jam 6-12) dan  Evening (jam 18-21) tergantung rute, namun perbedaan antara kedua dan ketiga paling sibuk tidak banyak.


## Rekomendasi
1. Strategi marketing yang cocok untuk mengoptimasi pendapatan transportation service New York mempertimbangkan pola perilaku pelanggan :
    1. **Memanfaatkan Preferensi Pelanggan terhadap Rute Populer**: Mengingat preferensi pelanggan terhadap rute populer seperti Manhattan-Manhattan, Queens-Queens, dan Brooklyn-Brooklyn, strategi pemasaran dapat difokuskan pada promosi yang menargetkan pelanggan dalam rute-rute ini. Kampanye iklan yang menyoroti keunggulan layanan di wilayah-wilayah ini dapat menarik lebih banyak pelanggan potensial.
    2. **Memperluas Penawaran untuk Trip Pendek dan Cepat**: Karena banyak pelanggan memiliki preferensi untuk trip pendek dan cepat, memperluas penawaran untuk layanan sejenis seperti layanan jarak dekat dengan tarif yang kompetitif bisa menjadi strategi yang efektif. Ini bisa meliputi penawaran spesial untuk trip pendek, paket langganan untuk perjalanan rutin sehari-hari, atau promosi untuk mendorong penggunaan layanan untuk perjalanan sehari-hari.
    3. **Mendorong Penggunaan Metode Pembayaran Tertentu**: Mengingat bahwa sebagian besar pembayaran dilakukan melalui kartu kredit, dapat dipertimbangkan untuk memberikan insentif khusus untuk pembayaran dengan kartu kredit. Ini bisa berupa diskon atau bonus poin setiap kali pelanggan menggunakan kartu kredit untuk pembayaran, sehingga mendorong penggunaan metode pembayaran yang lebih menguntungkan bagi NYC TLC.


2. Strategi operasional logistik dalam mengatasi kesediaan armada pada waktu, tempat, maupun rute populer :
    1. **Optimalkan Posisi Armada pada Tempat Pickup yang Berpengaruh Besar**: Mengingat bahwa tempat pickup memiliki pengaruh besar pada pendapatan, NYC TLC dapat menggunakan analisis data untuk menentukan lokasi-lokasi yang paling strategis mengoptimasi distribusi driver dan alokasi kendaraan. Dengan mengalokasikan armada lebih banyak di tempat-tempat ini pada waktu-waktu yang strategis, seperti saat permintaan tinggi atau dalam rangka mengantisipasi pola perilaku pelanggan, NYC TLC dapat memaksimalkan peluang untuk meningkatkan pendapatannya.
    2. **Penjadwalan Armada Berdasarkan Pola Waktu yang Signifikan**: Memahami pola siklik mingguan dan harian dari waktu berpengaruh besar pada banyak trip dan pendapatan dapat membantu dalam penjadwalan armada. NYC TLC dapat mengatur jadwal armada untuk menyesuaikan dengan pola ini, dengan meningkatkan ketersediaan armada pada jam-jam yang diprediksi memiliki permintaan tinggi, seperti jam 15-18 pada hari-hari tertentu dalam seminggu.
   
Dengan menggabungkan rekomendasi-rekomendasi ini dan terus memantau perubahan dalam perilaku pelanggan serta dinamika pasar, NYC TLC dapat mengembangkan strategi pemasaran yang kokoh untuk mengoptimalkan pendapatan transportasi di New York City.

<br/>
Copyright &copy; 2024, Roberto Benedict.
