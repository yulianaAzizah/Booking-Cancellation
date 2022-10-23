# Booking-Cancellation

## BUSINESS UNDERSTANDING

### Introduction
Salah satu dampak positif dari pesatnya perkembangan teknologi dan informasi bagi kehidupan manusia adalah kemudahan dalam mengakses informasi yang tidak terbatas pada ruang dan waktu. Inilah yang kemudian banyak diaplikasikan oleh penyedia produk dan jasa untuk memberikan kemudahan kepada calon pelanggan untuk mendapatkan informasi terkait produk/jasa hingga melakukan transaksi secara jarak jauh. Dalam industri perhotelan, peluang ini dimanfaatkan untuk penyediaan layanan reservasi secara online yang mememungkinkan para calon pelanggan untuk melakukan booking kamar dan servis dari jauh hari Antonio, et al (2019).<br>
Namun, keterbukaan informasi dan kemudahan dalam melakukan reservasi ini juga diiringi dengan kemudahan pelanggan untuk melakukan pembatalan reservasi. Hal ini akan memberikan ketidakpastian kepada hotel karena adanya kemungkinan pembatalan reservasi dalam waktu yang mendadak dapat menjadi kerugian yang harus ditanggung hotel karena kamar yang seharusnya terisi berakhir menjadi kamar kosong Antonio, et al (2017).<br>
Identifikasi yang dilakukan oleh Chen dan Xie (2013) dan Chen, Schwartz, dan Vargas (2011), saat ini sebagian besar pelanggan melakukan pembatalan karena pelanggan ingin mendapatkan harga yang terbaik. Terkadang setelah melakukan pemesanan, pelanggan tetap melakukan pencarian lebih lanjut untuk product/service yang sama dengan yang sudah dipesan. Perilaku pelanggan yang seperti ini tentu akan berdampak pada kerugian yang harus ditanggung oleh hotel.<br>
Oleh sebab itu, hal ini perlu diberikan perhatian yang serius supaya keputusan-keputusan yang diambil yang terkait dengan kebijakan pembatalan reservasi tidak akan merugikan hotel dan pelanggan. Namun, sebagai penyedia layanan dan jasa, hotel juga tidak boleh terlalu kaku dalam menerapkan kebijakan karena ini bisa saja merusak reputasi hotel di mata pelanggan.

### Problem Statement
Pertanyaan yang ingin dijawab dalam projek ini antara lain:
1.	Bagaimanakah parameter dan kinerja model machine learning yang dapat memprediksi pembatalan reservasi hotel dari dataset Hotel Booking?
2.	Berapa besar potensial benefit yang bisa diperoleh apabila model yang dibangun diterapkan di industri?
3.	Faktor-faktor apa sajakah yang mempengaruhi pelanggan untuk melakukan pembatalan reservasi hotel?

### Objectives
Projek ini diharapkan false negatif hasil prediksi dapat diminimalkan, yaitu prediksi bahwa pelanggan yang tidak membatalkan reservasi namun sebenarnya melakukan pembatalan reservasi. Dengan begitu, maka besarnya kerugian dan faktor penyebabnya dapat diketahui untuk menjadi bahan kajian management hotel dalam melakukan pengambilan kebijakan dan perbaikan.

### Production Scenario
Ada banyak faktor yang berpengaruh terhadap pembatalan hotel oleh pelanggan. Akan tetapi, faktor-faktor tersebut dapat berubah sesuai dengan perkembangan teknologi dan kebutuhan pelanggan. Sehingga prediksi pembatalan reservasi kamar hotel dapat dimasukan dalam analisa bisnis secara berkala. Dalam hal ini beberapa rekomendasi yang dapat diberikan diantaranya:
1.	Analisa dilakukan setelah melakukan perbaikan pada faktor paling berpengaruh sehingga dapat dilihat keefektifan perbaikan yang dilakukan terhadap kasus pembatalan reservasi kamar hotel
2.	Analisa dilakukan secara periodic setiap satu bulan sekali dan dimasukan dalam pembahasan monthly management review.<br><br>
![download](https://user-images.githubusercontent.com/106572825/191748288-fb2b0ecd-d6b8-4f3d-b1d4-04773637429f.png)

### Metric Evaluation
Untuk mengukur kinerja model yang dibangun, maka metrik evaluasi yang akan digunakan dalam model ini adalah Recall.<br>
Recall = (True Positive) / (True Positive + False Negative).<br>
False Negative (FN): Hasil prediksi ini menunjukan reservasi tidak dibatalkan akan tetapi hasil aktualnya dibatalkan. Dampak dari hasil ini adalah kehilangan pendapatan dan memberikan kerugian dari sisi efisiensi kerja dan financial hotel.
Sehingga dengan menerapkan metrik recall, maka model machine learning yang dibangun ingin meminimalkan hasil prediksi yang False Negative, yaitu hasil prediksi yang menunjukan reservasi tidak dibatalkan padahal sebetulnya dibatalkan.

### Conclusion
1.	Hasil machine learning menunjukkan :<br>
o	Model XGBoost memiliki performa paling baik<br>
o	Model dapat meminimalkan prediksi pelanggan yang melakukan pembatalan namun dianggap tidak melakukan pembatalan dengan medel matrix Recall. Dalam hal ini, model mampu memprediksi 87% yang melakukan pembatalan reservasi hotel.<br>
2.	Jika program ini diterapkan, perusahaan setidaknya dapat meningkatkan potensi pendapatan sebesar €409,482.89 selama periode 2015-2017.
3.	Berdasarkan dataset Hotel Booking faktor yang paling berpengaruh besar dalam menentukan sebuah reservasi akan dibatalkan atau tidak adalah is_room_diff (perbedaan kamar yang diminta oleh pelanggan dengan yang diberikan oleh hotel).
4.	Ada beberapa batasan yang ditarapkan dalam model prediksi ini, yaitu:<br>
o	Model hanya mampu memprediksi lead_time dengan batasan 0 sampai dengan 296 hari.<br>
o	Model hanya mampu memprediksi stays_in_all_nights dengan batasan 0 sampai dengan 10 hari.<br>
o	Model hanya mampu memprediksi adr dengan batasan €0 sampai dengan €227.<br>
o	Model hanya mampu memprediksi total of special request dengan batasan 0 sampai dengan 3

Link Tableau untuk data visualisasi: [Tableau](https://public.tableau.com/views/HotelBookings_16631504869120/Dashboard1?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link)
