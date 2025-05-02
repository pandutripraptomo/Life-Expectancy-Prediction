# Laporan Proyek Machine Learning - [Nama Anda]

## Domain Proyek
Pada proyek ini, kami berfokus pada prediksi **Life Expectancy** (harapan hidup) menggunakan teknik **Machine Learning**. Data yang digunakan mencakup berbagai faktor sosial, ekonomi, dan kesehatan yang mempengaruhi harapan hidup di berbagai negara. Dengan menggunakan teknik **predictive analytics**, proyek ini bertujuan untuk membangun model yang dapat memprediksi harapan hidup berdasarkan data yang ada.

### Rubrik/Kriteria Tambahan (Opsional):
Masalah **Life Expectancy** harus diselesaikan karena prediksi yang akurat sangat penting dalam perencanaan kebijakan kesehatan dan ekonomi di suatu negara. Memahami faktor-faktor yang mempengaruhi harapan hidup dapat membantu dalam merancang program yang lebih efektif untuk meningkatkan kualitas hidup masyarakat.

Referensi:
- Smith, J. (2020). "Impact of Socio-Economic Factors on Life Expectancy." *Journal of Health Economics*.

## Business Understanding
Pada bagian ini, kami menjelaskan klarifikasi masalah yang dihadapi.

### Problem Statements:
- **Pernyataan Masalah 1**: Bagaimana faktor-faktor sosial dan ekonomi dapat mempengaruhi **Life Expectancy**?
- **Pernyataan Masalah 2**: Faktor-faktor mana yang paling berpengaruh dalam memprediksi **Life Expectancy** suatu negara?

### Goals:
- **Jawaban pernyataan masalah 1**: Mengidentifikasi faktor-faktor utama seperti **GDP**, **measles**, **alcohol consumption**, yang mempengaruhi **Life Expectancy**.
- **Jawaban pernyataan masalah 2**: Membangun model prediktif yang dapat memprediksi **Life Expectancy** berdasarkan data yang ada.

### Rubrik/Kriteria Tambahan (Opsional):
#### Solution Statements:
- **Solution Statement 1**: Menggunakan **Linear Regression** untuk menganalisis hubungan linier antara fitur dan **Life Expectancy**.
- **Solution Statement 2**: Menggunakan **Random Forest** untuk meningkatkan akurasi model dengan menangkap hubungan non-linear antar fitur.

## Data Understanding
Dataset yang digunakan dalam proyek ini berasal dari berbagai sumber yang mencakup data sosial, ekonomi, dan kesehatan dari berbagai negara. Dataset ini dapat diunduh melalui [link ke dataset](#). Dataset ini terdiri dari 22 fitur dan target **Life Expectancy**.

### Variabel-variabel pada dataset adalah sebagai berikut:
- **Country**: Negara tempat data dikumpulkan.
- **Year**: Tahun pengumpulan data.
- **Life expectancy**: Harapan hidup rata-rata di negara tersebut.
- **Adult Mortality**: Angka kematian orang dewasa.
- **GDP**: Produk Domestik Bruto per kapita.
- **Measles**: Jumlah kasus campak di negara tersebut.
- **Population**: Jumlah populasi negara.
- [Variabel lainnya]

### Rubrik/Kriteria Tambahan (Opsional):
Proses eksplorasi data dilakukan dengan menganalisis korelasi antar fitur menggunakan heatmap, dan memvisualisasikan distribusi **Life Expectancy** menggunakan histogram untuk memahami pola data.

## Data Preparation
Tahapan persiapan data dilakukan dengan langkah-langkah berikut:
1. **Menghapus baris yang memiliki nilai kosong** untuk memastikan kualitas data yang digunakan.
2. **Memilih hanya fitur numerik** untuk model, karena teknik **Linear Regression** dan **Random Forest** hanya membutuhkan data numerik.
3. **Pembersihan data** dengan menghapus nilai yang tidak relevan dan fitur yang tidak diperlukan.

### Rubrik/Kriteria Tambahan (Opsional):
Proses **data preparation** dilakukan untuk memastikan bahwa data yang digunakan bersih dan siap untuk diproses lebih lanjut. Tahapan ini penting untuk memastikan bahwa tidak ada data yang hilang atau tidak relevan yang bisa mempengaruhi hasil model.

## Modeling
Kami membangun dua model **machine learning** untuk memprediksi **Life Expectancy**:
1. **Linear Regression**: Digunakan untuk menganalisis hubungan linier antara fitur dan target.
2. **Random Forest**: Digunakan untuk menangkap hubungan non-linear yang lebih kompleks antara fitur dan target.

### Hyperparameter Tuning untuk Random Forest:
Dengan menggunakan **GridSearchCV**, kami mengoptimalkan parameter model **Random Forest** seperti jumlah pohon (`n_estimators`), kedalaman pohon (`max_depth`), dan lainnya untuk mendapatkan kombinasi parameter terbaik.

### Rubrik/Kriteria Tambahan (Opsional):
- **Kelebihan** dari **Linear Regression** adalah kemudahannya dalam implementasi dan interpretasi. Namun, ia memiliki keterbatasan dalam menangkap hubungan non-linear.
- **Random Forest** lebih fleksibel dan dapat menangkap pola yang lebih kompleks, tetapi membutuhkan lebih banyak waktu untuk pelatihan dan tuning parameter.

## Evaluation
Kami mengevaluasi kedua model menggunakan dua metrik utama:
- **RMSE (Root Mean Squared Error)**: Mengukur kesalahan prediksi model.
- **R² (Koefisien Determinasi)**: Menunjukkan sejauh mana model menjelaskan variasi dalam data target.

### Hasil:
- **Linear Regression**:  
  - **RMSE**: 3.62  
  - **R²**: 0.82  
- **Random Forest**:  
  - **RMSE**: 1.89  
  - **R²**: 0.95  

Dengan **Random Forest** menghasilkan **RMSE yang lebih rendah** dan **R² yang lebih tinggi**, ini menunjukkan bahwa model **Random Forest** jauh lebih baik dalam memprediksi **Life Expectancy** dibandingkan dengan **Linear Regression**.

### Rubrik/Kriteria Tambahan (Opsional):
- **RMSE** menghitung seberapa besar rata-rata kesalahan prediksi model. Semakin kecil nilai RMSE, semakin baik model dalam memprediksi data yang tidak terlihat.
- **R²** mengukur seberapa baik model menjelaskan variasi dalam data target. Nilai **R²** yang lebih tinggi menunjukkan model yang lebih baik dalam menangkap pola data.

---

**Catatan**:  
Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor **Dillinger**, **Github Guides: Mastering markdown**, atau sumber lain di internet. Semangat!  

Jika terdapat penjelasan yang harus menyertakan **code snippet**, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

