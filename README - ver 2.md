# E-Commerce RFM Analysis

Context
-------------
Kemampuan perusahaan dalam menjalin dan menjaga hubungan baik dengan pelanggan merupakan kunci keberhasilan bisnis yang berkelanjutan. Hubungan yang baik membuat pelanggan tetap ingin bertransaksi, atau bahkan mereka akan memberikan rekomendasi produk atau layanan perusahaan kepada orang lain. Dalam konteks bisnis, strategi mempertahankan pelanggan agar terus membeli produk atau menggunakan layanan dari perusahaan disebut dengan retensi pelanggan. Hal ini bertujuan untuk meningkatkan profit perusahaan.

Berdasarkan sumber dari majalah Harvard Business Review, mempertahankan loyalitas pelanggan akan dapat meningkatkan total pendapatan perusahaan sebesar 25%-40%. Peran retensi pelanggan juga sangat signifikan dalam mengurangi anggaran bisnis perusahaan. Untuk mendapatkan pelanggan baru diperlukan biaya 5 hingga 25 kali lebih mahal dibandingkan mempertahankan pelanggan yang sudah ada.

Dalam konteks ini kami sebagai seorang Data Scientist akan menganalisis data transaksi dari perusahaan Olist, sebuah departement store di Brasil yang beroperasi di segmen e-commerce. Kami akan mencoba memaksimalkan penjualan ritel pada e-commerce olist dengan melakukan customer segmentation yang dapat meningkatkan retensi pelanggan. Retention rate yang tinggi mengartikan bahwa pelanggan tersebut menghargai produk atau layanan yang diberikan perusahaan dan memberikan sumber pendapatan berkelanjutan kepada perusahaan tersebut.

Problem Statement
-------------
1. Bagaimana kondisi customer retention rate Olist?
2. Bagaimana cara Olist mengembangkan retensi pelanggan sehingga dapat meningkatkan penjualan?
3. Bagaimana cara Olist memonitor performa bisnis, retensi dan segmentasi pelanggan sehingga dapat mengambil tindakan lebih cepat dan tepat?

Scope of Problem
-------------
Asumsi saat ini tim marketing Olist melakukan pemasaran secara merata terhadap semua pelanggan karena belum menerapkan segmentasi pelanggan.

Goals
-------------
* Melakukan segmentasi pelanggan dan memberikan rekomendasi aksi yang sesuai (khususnya terkait pemasaran) untuk masing-masing segmentasi dengan harapan dapat meningkatkan retensi pelanggan dan mengurangi biaya operasional yang tidak diperlukan.
* Membuat dashboard visualisasi untuk memonitor performa bisnis, retensi dan segmentasi pelanggan.

Project Stakeholders
-------------
1. Tim Marketing & Sales (Primary Stakeholder)

Bertanggung jawab dalam mengembangkan dan merencanakan usaha marketing serta mengimplementasikan kepada pelanggan secara tepat dalam upaya memaksimalkan pendapatan perusahaan.

2. Tim Keuangan (Secondary Stakeholder)

Bertanggung jawab dalam mengatur keuangan perusahaan yang diakibatkan oleh usaha marketing.

Analytics Approach
-------------
1. Diagnostic Analysis
> - Retention Rate
Retention rate merupakan salah satu alat untuk mengukur tingkat retensi pelanggan yang memproyeksikan keuntungan dan pertumbuhan dari produk atau layanan yang dipasarkan oleh sebuah perusahaan. Retention rate adalah persentase pengguna yang terus menggunakan layanan atau produk dari perusahaan selama jangka waktu tertentu. Menurut Moran Khoubian, Direktur Senior dari Perusahaan Yotpo, yang bergerak di pemasaran konten berbasis cloud untuk bisnis e-commerce, mengatakan bahwa  retention rate untuk setiap e-commerce berbeda-beda tergantung ukuran perusahaan dan cara model perencanaan bisnisnya, tetapi biasanya rata-rata retention rate suatu perusahaan e-commerce berada di antara 15% hingga 30%.

Saat terdapat indikasi bahwa retention rate perusahaan rendah atau dengan kata lain saat bisnis kehilangan pangsa pasar atau pelanggan tidak puas dengan produk atau layanan yang ditawarkan, hal tersebut dapat menyebabkan penurunan transaksi dan berdampak pada pendapatan perusahaan. Untuk mengatasi masalah ini, perusahaan perlu meningkatkan retensi pelanggan dengan cara memahami basis pelanggan melalui segmentasi.
> - Cohort Analysis

2. Segmentation
Dengan membagi basis pelanggan menjadi kelompok-kelompok yang lebih kecil dan lebih mudah dikelola berdasarkan karakteristik tertentu, perusahaan dapat menyesuaikan pendekatan terhadap kebutuhan dan keinginan pelanggan untuk setiap segmennya guna mencegah hilangnya pelanggan. Misalnya dengan memberikan penawaran promo yang tepat sasaran untuk meningkatkan kepuasan pelanggan sesuai kebutuhannya, yang diharapkan pelanggan tersebut akan tertarik untuk menerima tawaran tersebut dan kembali membeli produk atau menggunakan layanan dari perusahaan.
 
> - RFM Analysis
> - Clustering - Unsupervised Machine Learning

Evaluation
-------------
* Metrics
  
  Metrik yang akan digunakan untuk mengevaluasi segmentasi pelanggan dengan model berbasis clustering adalah Silhouette score dan Davies Boudlin Score. Silhouette score merupakan ukuran kemiripan atau seberapa dekat sebuah sample terhadap clusternya sendiri dibandingkan terhadap cluster lainnya. Silhouette score mempunyai rentang nilai dari -1 sampai 1 di mana:
  * Semakin besar nilai maka semakin dekat sample tersebut dengan clusternya sendiri (atau clustering sudah cukup baik)
  * Semakin kecil nilai maka sample masuk ke cluster yang kurang tepat
  * Nilai 0 berarti cluster tidak dapat dibedakan dengan jelas
  
  Jumlah cluster yang optimal dapat ditentukan melalui silhouette score yang terbaik. Ketika silhouette score semakin besar, semakin jelas segmentasi terpisah satu sama lain. Dengan begitu, tim marketing dapat mengambil langkah pendekatan yang lebih tepat sasaran untuk masing-masing segmentasi pelanggan.

  Davies Boud

* Processing Time
  Waktu pemrosesan 
  
* Interpretation
