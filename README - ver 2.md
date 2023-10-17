# E-Commerce RFM Analysis

Team Members:
* [**Nur Adhianti Heryanto**](https://github.com/nheryanto)
* [**Ari Adhi Hermawan**](https://github.com/aridiawan)
* [**Andi Muhammad Rinaldi Saputra**](https://github.com/andimrs)

Table of Contents
-------------
* [Context](#context)
* [Problem Statement](#problem-statement)
* [Scope of Problem](#scope-of-problem)
* [Goals](#goals)
* [Project Stakeholders](#project-stakeholders)
* [Analytics Approach](#analytics-approach)
* [Evaluation](#evaluation)
* [Dashboard - Tableau](#dashboard-tableau)

Context
-------------
Kemampuan perusahaan dalam menjalin dan menjaga hubungan baik dengan pelanggan merupakan kunci keberhasilan bisnis yang berkelanjutan. Hubungan yang baik membuat pelanggan tetap ingin bertransaksi, atau bahkan mereka akan memberikan rekomendasi produk atau layanan perusahaan kepada orang lain. Dalam konteks bisnis, strategi mempertahankan pelanggan agar terus membeli produk atau menggunakan layanan dari perusahaan disebut dengan retensi pelanggan. Hal ini bertujuan untuk meningkatkan profit perusahaan.

Berdasarkan sumber dari majalah Harvard Business Review, mempertahankan loyalitas pelanggan akan dapat meningkatkan total pendapatan perusahaan sebesar 25%-40%. Peran retensi pelanggan juga sangat signifikan dalam mengurangi anggaran bisnis perusahaan. Untuk mendapatkan pelanggan baru diperlukan biaya 5 hingga 25 kali lebih mahal dibandingkan mempertahankan pelanggan yang sudah ada.

Retention rate merupakan salah satu alat untuk mengukur tingkat retensi pelanggan yang memproyeksikan keuntungan dan pertumbuhan dari produk atau layanan yang dipasarkan oleh sebuah perusahaan. Retention rate adalah persentase pengguna yang terus menggunakan layanan atau produk dari perusahaan selama jangka waktu tertentu. Menurut Moran Khoubian, Direktur Senior dari Perusahaan Yotpo, yang bergerak di pemasaran konten berbasis cloud untuk bisnis e-commerce, mengatakan bahwa  retention rate untuk setiap e-commerce berbeda-beda tergantung ukuran perusahaan dan cara model perencanaan bisnisnya, tetapi biasanya rata-rata retention rate suatu perusahaan e-commerce berada di antara 15% hingga 30%.

Saat terdapat indikasi bahwa retention rate perusahaan rendah atau dengan kata lain saat bisnis kehilangan pangsa pasar atau pelanggan tidak puas dengan produk atau layanan yang ditawarkan, hal tersebut dapat menyebabkan penurunan transaksi dan berdampak pada pendapatan perusahaan. Untuk mengatasi masalah ini, perusahaan perlu meningkatkan retensi pelanggan dengan cara memahami basis pelanggan melalui segmentasi.

Dengan membagi basis pelanggan menjadi kelompok-kelompok yang lebih kecil dan lebih mudah dikelola berdasarkan karakteristik tertentu, perusahaan dapat menyesuaikan pendekatan terhadap kebutuhan dan keinginan pelanggan untuk setiap segmennya guna mencegah hilangnya pelanggan. Misalnya dengan memberikan penawaran promo yang tepat sasaran untuk meningkatkan kepuasan pelanggan sesuai kebutuhannya, yang diharapkan pelanggan tersebut akan tertarik untuk menerima tawaran tersebut dan kembali membeli produk atau menggunakan layanan dari perusahaan.

Dalam konteks ini kami sebagai seorang Data Scientist akan menganalisis data transaksi dari perusahaan Olist, sebuah e-commerce platform yang mengintegrasikan berbagai marketplace di brazil. 

Problem Statement
-------------
1. Bagaimana kondisi retensi pelanggan Olist?
2. Bagaimana cara Olist melakukan segmentasi sehingga dapat membagi pelanggan berdasarkan perilaku pembeliannya?

Scope of Problem
-------------
Asumsi saat ini tim marketing Olist melakukan pemasaran secara merata terhadap semua pelanggan karena belum menerapkan segmentasi pelanggan.

Goals
-------------
* Melakukan analisis untuk mengetahui kondisi retensi pelanggan Olist.
* Melakukan segmentasi pelanggan dan memberikan rekomendasi aksi yang sesuai (khususnya terkait pemasaran) untuk masing-masing segmentasi dengan harapan dapat meningkatkan retensi pelanggan dan mengurangi biaya operasional yang tidak diperlukan.

Project Stakeholders
-------------
1. **Tim Marketing & Sales** (Primary Stakeholder)

Bertanggung jawab dalam mengembangkan dan merencanakan usaha marketing serta mengimplementasikan kepada pelanggan secara tepat dalam upaya memaksimalkan pendapatan perusahaan.

2. **Tim Keuangan** (Secondary Stakeholder)

Bertanggung jawab dalam mengatur keuangan perusahaan yang diakibatkan oleh usaha marketing.

Analytics Approach
-------------
1. Descriptive Analysis
   * Retention Rate - Cohort Analysis

3. Segmentation
   * RFM Analysis
   * Clustering - Unsupervised Machine Learning

Evaluation
-------------
* **Metrics**
  
  Metrik yang akan digunakan untuk mengevaluasi segmentasi pelanggan adalah Silhouette score dan Davies Bouldin Score.

  Silhouette score merupakan ukuran kemiripan atau seberapa dekat sebuah sample terhadap clusternya sendiri dibandingkan terhadap cluster lainnya. Silhouette score mempunyai rentang nilai dari -1 sampai 1 di mana:
  * Semakin besar nilai maka semakin dekat sample tersebut dengan clusternya sendiri
  * Semakin kecil nilai maka sample masuk ke cluster yang kurang tepat
  * Nilai 0 berarti cluster tidak dapat dibedakan dengan jelas
  
  Davies Bouldin score merupakan ukuran kemiripan sebuah cluster terhadap cluster lain.

  Ekspektasi untuk hasil clustering adalah nilai silhouette score sebesar mungkin mendekati 1 dan nilai davies bouldin score sekecil mungkin. Ketika silhouette score semakin besar, semakin jelas segmentasi terpisah satu sama lain. Ketika nilai davies bouldin score semakin kecil, kemiripan cluster satu sama lain semakin kecil. Kedua metrik ini digunakan untuk menentukan jumlah cluster yang optimal pada pemodelan machine learning.

  Dalam konteks bisnis, nilai metrik evaluasi yang lebih baik akan menghasilkan segmentasi yang terpisah lebih jelas sehingga stakeholder terkait dapat mengambil langkah pendekatan yang lebih tepat sasaran untuk masing-masing segmentasi customer.

* **Processing Time**

  Waktu pemrosesan merujuk pada waktu yang dibutuhkan untuk melakukan pemodelan sampai menghasilkan segmentasi. Untuk pemodelan machine learning, hal ini termasuk waktu training dan tuning parameter. Aspek ini dipertimbangkan mengingat jumlah data yang digunakan besar dan berpengaruh terhadap kompleksitas waktu.
  
* **Interpretation**

  Interpretasi di sini difokuskan pada informasi yang dapat diambil dari hasil segmentasi karena tujuan dari analisis ini adalah mendapatkan segmentasi customer yang dapat memberikan actionable insights yang tepat.

Dashboard - Tableau
-------------
[Ecommerce Dashboard - RFM Segmentation](https://github.com/nheryanto](https://public.tableau.com/views/EcommerceDashboard-RFMSegmentation/ECOMMERCE?:language=en-US&:display_count=n&:origin=viz_share_link)https://public.tableau.com/views/EcommerceDashboard-RFMSegmentation/ECOMMERCE?:language=en-US&:display_count=n&:origin=viz_share_link)
