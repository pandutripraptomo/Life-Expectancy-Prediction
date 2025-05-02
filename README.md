# Laporan Proyek Machine Learning - Pandu Tri Praptomo

## Domain Proyek
Pada proyek ini, kami berfokus pada prediksi **Life Expectancy** (harapan hidup) menggunakan teknik **Machine Learning**. Data yang digunakan mencakup berbagai faktor sosial, ekonomi, dan kesehatan yang mempengaruhi harapan hidup di berbagai negara. Dengan menggunakan teknik **predictive analytics**, proyek ini bertujuan untuk membangun model yang dapat memprediksi harapan hidup berdasarkan data yang ada.

### Rubrik/Kriteria Tambahan (Opsional):
Masalah **Life Expectancy** harus diselesaikan karena prediksi yang akurat sangat penting dalam perencanaan kebijakan kesehatan dan ekonomi di suatu negara. Memahami faktor-faktor yang mempengaruhi harapan hidup dapat membantu dalam merancang program yang lebih efektif untuk meningkatkan kualitas hidup masyarakat.

**Referensi:**
- [Smith, J. (2020)](https://mpra.ub.uni-muenchen.de/70871/). "Impact of Socio-Economic Factors on Life Expectancy." *Journal of Health Economics*  
  Referensi ini memberikan wawasan terkait faktor-faktor sosial ekonomi yang mempengaruhi harapan hidup.

---

## Business Understanding
Pada bagian ini, kami menjelaskan klarifikasi masalah yang dihadapi dalam memprediksi **Life Expectancy**. Kami berusaha untuk memahami pengaruh berbagai faktor pada harapan hidup dan bagaimana kita dapat menggunakan teknik machine learning untuk memberikan wawasan yang berguna.

### Problem Statements:
- **Pernyataan Masalah 1**: Bagaimana faktor-faktor sosial dan ekonomi dapat mempengaruhi **Life Expectancy**?
  - Penjelasan: Faktor-faktor seperti **GDP**, **polio**, **measles**, **alcohol consumption**, dan **adult mortality** dapat memiliki dampak yang signifikan terhadap harapan hidup di berbagai negara.
- **Pernyataan Masalah 2**: Faktor-faktor mana yang paling berpengaruh dalam memprediksi **Life Expectancy** suatu negara?
  - Penjelasan: Beberapa variabel sosial dan ekonomi mempengaruhi harapan hidup, namun kami perlu menentukan variabel mana yang paling signifikan berdasarkan model yang dikembangkan.

### Goals:
- **Jawaban pernyataan masalah 1**: Mengidentifikasi faktor-faktor utama yang mempengaruhi **Life Expectancy**, seperti **GDP**, **measles**, **alcohol consumption**, dan **adult mortality**.
- **Jawaban pernyataan masalah 2**: Membangun model prediktif yang dapat memprediksi **Life Expectancy** berdasarkan faktor-faktor tersebut.

### Rubrik/Kriteria Tambahan (Opsional):
#### Solution Statements:
- **Solution Statement 1**: Menggunakan **Linear Regression** untuk menganalisis hubungan linier antara fitur dan **Life Expectancy**. Linear Regression akan memberikan wawasan tentang hubungan langsung antara variabel independen dan target.
- **Solution Statement 2**: Menggunakan **Random Forest** untuk menangkap hubungan non-linear antara fitur dan **Life Expectancy**. Random Forest lebih fleksibel dan dapat menangkap interaksi kompleks antar fitur.

---

## Data Understanding

Dataset yang digunakan dalam proyek ini berasal dari berbagai sumber yang mencakup data sosial, ekonomi, dan kesehatan dari berbagai negara. Dataset ini dapat diunduh melalui [link ke dataset Kaggle](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who). Dataset ini terdiri dari 22 fitur dan target **Life Expectancy** yang ingin diprediksi.

### Variabel-variabel pada dataset adalah sebagai berikut:
- **Country**: Negara tempat data dikumpulkan.
- **Year**: Tahun pengumpulan data.
- **Life expectancy**: Harapan hidup rata-rata di negara tersebut.
- **Adult Mortality**: Angka kematian orang dewasa, yang mempengaruhi harapan hidup.
- **GDP**: Produk Domestik Bruto per kapita, sebagai indikator ekonomi.
- **Measles**: Jumlah kasus campak, yang merupakan indikator kesehatan anak.
- **Population**: Jumlah populasi negara.
- **Alcohol**: Konsumsi alkohol rata-rata per kapita.
- **Polio**: Tingkat vaksinasi polio pada anak.
- **Infant deaths**: Angka kematian bayi, menunjukkan kualitas layanan kesehatan di negara tersebut.
- [Variabel lainnya]

### Rubrik/Kriteria Tambahan (Opsional):
Proses eksplorasi data dilakukan dengan menganalisis korelasi antar fitur menggunakan heatmap. Visualisasi distribusi **Life Expectancy** menggunakan histogram juga dilakukan untuk memahami pola data dan memastikan bahwa distribusi target tidak terlalu miring atau memiliki outlier yang signifikan.

---

## Data Preparation

Tahapan persiapan data dilakukan dengan langkah-langkah berikut:
1. **Menghapus baris yang memiliki nilai kosong** untuk memastikan kualitas data yang digunakan. Ini penting untuk menghindari bias yang mungkin ditimbulkan oleh nilai yang hilang.
2. **Memilih hanya fitur numerik** untuk model, karena teknik **Linear Regression** dan **Random Forest** hanya membutuhkan data numerik.
3. **Pembersihan data** dengan menghapus nilai yang tidak relevan dan fitur yang tidak diperlukan. Misalnya, jika terdapat fitur yang tidak berkontribusi secara signifikan terhadap prediksi, fitur tersebut dihapus dari dataset.

### Rubrik/Kriteria Tambahan (Opsional):
Proses **data preparation** penting dilakukan untuk memastikan bahwa data yang digunakan bersih dan siap untuk diproses lebih lanjut. Tahapan ini penting untuk memastikan bahwa tidak ada data yang hilang atau tidak relevan yang bisa mempengaruhi hasil model. Data yang tidak dipersiapkan dengan baik dapat menyebabkan model menghasilkan prediksi yang buruk.

---

## Modeling

Kami membangun dua model **machine learning** untuk memprediksi **Life Expectancy**:
1. **Linear Regression**: Digunakan untuk menganalisis hubungan linier antara fitur dan target. Model ini digunakan sebagai baseline model karena mudah diinterpretasikan dan cepat untuk diimplementasikan.
2. **Random Forest**: Digunakan untuk menangkap hubungan yang lebih kompleks (non-linear) dan dipilih sebagai model utama.
3. **Hyperparameter Tuning untuk Random Forest**:
   Dengan menggunakan **GridSearchCV**, kami mengoptimalkan parameter model **Random Forest** seperti jumlah pohon (`n_estimators`), kedalaman pohon (`max_depth`), dan lainnya untuk mendapatkan kombinasi parameter terbaik.

### Rubrik/Kriteria Tambahan (Opsional):
- **Kelebihan** dari **Linear Regression** adalah kemudahannya dalam implementasi dan interpretasi. Namun, ia memiliki keterbatasan dalam menangkap hubungan non-linear yang lebih kompleks.
- **Random Forest** lebih fleksibel dan dapat menangkap pola yang lebih kompleks, namun membutuhkan lebih banyak waktu untuk pelatihan dan tuning parameter.

---

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

