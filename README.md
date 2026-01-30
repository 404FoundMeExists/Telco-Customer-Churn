Customer Churn Analysis — Telco Company
Project Overview
Customer churn merupakan salah satu tantangan terbesar dalam industri layanan berbasis subscription, 
termasuk perusahaan telekomunikasi. Dalam project ini, dilakukan analisis churn pelanggan untuk memahami 
faktor-faktor utama yang menyebabkan pelanggan berhenti berlangganan serta mengidentifikasi segmen pelanggan berisiko tinggi.
Dataset yang digunakan adalah Telco Customer Churn Dataset, yang berisi informasi pelanggan seperti jenis kontrak, metode pembayaran, layanan internet, biaya bulanan, dan status churn

Business Problem
Dalam perusahaan telekomunikasi, churn dapat menyebabkan:
- penurunan pendapatan
- meningkatnya biaya akuisisi pelanggan baru
- terganggunya stabilitas bisnis
Perusahaan ingin mengetahui lebih awal pelanggan yang berpotensi churn agar dapat dilakukan strategi retensi yang tepat.


Business Objectives
Project ini bertujuan untuk:
- Mengukur baseline churn rate pelanggan
- Mengidentifikasi faktor utama penyebab churn
- Melakukan segmentasi pelanggan berisiko tinggi (High Risk Segment)
- Memberikan rekomendasi bisnis untuk menekan churn

📂 Dataset Information
Source: Kaggle — Telco Customer Churn Dataset
Total data: 7,043 customers
Total features: 21 columns

Tools & Libraries
Analisis dilakukan menggunakan Python dengan library:
- pandas
- matplotlib

🔍 Analysis Workflow
Step 1 — Data Understanding
- Mengecek ukuran dataset dan tipe data
- Memahami arti setiap kolom
- Mengidentifikasi missing values pada TotalCharges
Step 2 — Data Cleaning
- Konversi kolom TotalCharges menjadi numerik
- Menangani missing values yang muncul pada pelanggan tenure = 0
- Dataset siap digunakan untuk analisis eksploratif
Step 3 — Baseline Churn Rate
Baseline churn rate dihitung dari seluruh pelanggan:
- Churn = Yes → 26.6%
- Churn = No → 73.4%
Insight:
Sekitar 1 dari 4 pelanggan dalam dataset berhenti berlangganan.
Step 4 — Tenure vs Churn
Pelanggan churn memiliki masa berlangganan jauh lebih pendek:
- Churn → rata-rata tenure 18 bulan
- Non-churn → rata-rata tenure 38 bulan
Insight:
Pelanggan baru lebih rentan churn pada fase awal berlangganan.
Step 5 — Monthly Charges vs Churn
Pelanggan churn membayar biaya bulanan lebih tinggi:
- Churn → 74.4
- Non-churn → 61.3
Insight:
Pelanggan dengan tagihan tinggi lebih sensitif terhadap harga dan value layanan.
Step 6 — Key Drivers of Churn
Faktor dengan churn rate tertinggi:
Faktor	Churn Rate
- Month-to-month contract	(42.7%)
- Electronic check payment	(45.3%)
- Fiber optic service	(41.9%)
- No OnlineSecurity	(41.8%)
Insight:
Kontrak fleksibel dan layanan tanpa keamanan online menjadi indikator churn kuat.
Step 7 — High Risk Customer Segmentation
Segmentasi pelanggan berisiko tinggi berdasarkan kombinasi:
- Month-to-month contract
- Electronic check payment
- Fiber optic internet
- No OnlineSecurity
Churn rate pada segmen ini mencapai:
- 63% – 70%
Insight:
Churn tidak terjadi secara acak, tetapi terkonsentrasi pada segmen pelanggan tertentu.


INSIGHT 
Baseline churn rate pada dataset ini adalah 26.6%, namun churn meningkat drastis hingga lebih dari 63% pada segmen pelanggan High Risk. 
Faktor utama penyebab churn adalah kontrak bulanan, metode pembayaran electronic check, layanan fiber optic, serta pelanggan tanpa OnlineSecurity. 
Oleh karena itu, strategi retensiperusahaan sebaiknya difokuskan pada segmen pelanggan berisiko tinggi melalui promo kontrak jangka panjang, 
migrasi pembayaran otomatis, serta bundling layanan keamanan online untuk menekan churn secara efektif.
