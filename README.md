# ecommerce-analysis

> Context

> Problem Statement

Dari konteks di atas, bisa diambil problem statement:
1. Bagaimana kondisi customer retention rate Olist?
2. Bagaimana cara Olist mengembangkan retensi pelanggan sehingga dapat meningkatkan penjualan?
3. Bagaimana cara Olist meningkatkan penjualan dengan cara Cross-Selling? (Opsional)

> Scope of Problem
1. Asumsi saat ini tim marketing Olist melakukan pemasaran secara merata terhadap semua pelanggan karena belum menerapkan segmentasi pelanggan

> Goals
Berdasarkan problem statement di atas, tujuan analisa yang dilakukan adalah:
1. Melakukan segmentasi pelanggan dan memberikan rekomendasi aksi yang sesuai (misal pemasaran) untuk masing-masing segmentasi dengan harapan dapat meningkatkan retensi pelanggan dan mengurangi biaya operasional yang tidak diperlukan
2. Membuat sistem rekomendasi berbasis produk sebagai upaya untuk meningkatkan penjualan (opsional)

> Project Stakeholders

> Analytics Approach

Untuk menjawab problem statement, dapat digunakan Analytics Approach:
1. Cohort Analysis
2. Clustering - Segmentation
3. Recommendation System - Item Based

> Metrics Evaluation
Metrik yang akan digunakan untuk mengevaluasi segmentasi pelanggan dengan model berbasis clustering adalah Silhouette score, yang merupakan ukuran kemiripan atau seberapa dekat sebuah sample terhadap clusternya sendiri dibandingkan terhadap cluster lainnya. Silhouette score mempunyai rentang nilai dari -1 sampai 1 di mana:
- Semakin besar nilai maka semakin dekat sample tersebut dengan clusternya sendiri (atau clustering sudah cukup baik)
- Semakin kecil nilai maka sample masuk ke cluster yang kurang tepat
- Nilai 0 berarti cluster tidak dapat dibedakan dengan jelas
Jumlah cluster yang optimal dapat ditentukan melalui silhouette score yang terbaik. Ketika silhouette score semakin besar, semakin jelas segmentasi terpisah satu sama lain. Dengan begitu, tim marketing dapat mengambil langkah pendekatan yang lebih tepat sasaran untuk masing-masing segmentasi pelanggan.
