# Analisis Sentimen IndoNLU dengan Deep Learning dan SVM

Proyek ini bertujuan untuk melakukan analisis sentimen pada teks berbahasa Indonesia menggunakan IndoNLU, sebuah pre-trained language model untuk bahasa Indonesia. Kami membandingkan performa model Deep Learning yang dilatih menggunakan PyTorch dan Support Vector Machine (SVM) untuk mengklasifikasikan teks menjadi sentimen positif, netral, atau negatif.

## Daftar Isi

- [Dataset](#dataset)
- [Gambaran Proyek](#gambaran-proyek)
- [Hasil dan Evaluasi](#hasil-dan-evaluasi)
  - [Deep Learning (PyTorch)](#model-deep-learning-pytorch)
  - [Support Vector Machine (SVM)](#model-support-vector-machine-svm)
- [Kesimpulan](#kesimpulan)

## Gambaran Proyek

Proyek ini mengikuti langkah-langkah utama dalam pipeline analisis sentimen:

1. **Data Acquisition**: Mengunduh dan menyiapkan dataset dari IndoNLU.
   Text Cleaning: Membersihkan teks dari karakter atau elemen yang tidak diperlukan.
2. **Pre-Processing**: Mengubah teks menjadi format yang bisa digunakan untuk model, seperti tokenisasi dan padding.
3. **Feature Engineering**: Ekstraksi fitur teks yang relevan, seperti embedding kata.
4. **Modeling**: Membangun model Deep Learning (PyTorch) atau SVM untuk klasifikasi sentimen.
5. **Evaluation**: Mengevaluasi performa model menggunakan metrik seperti Accuracy, F1-Score, Precision, dan Recall.

## Dataset

Dataset yang digunakan berasal dari IndoNLU, yang telah di-_pre-process_ untuk keperluan analisis sentimen. Dataset ini mencakup ribuan sampel teks berbahasa Indonesia yang telah dilabeli dengan sentimen positif, netral, dan negatif.

Untuk informasi lebih lanjut tentang dataset, kunjungi [IndoNLU](https://github.com/indobenchmark/indonlu).

## Hasil dan Evaluasi

Berikut ini adalah ringkasan hasil evaluasi performa dari kedua model:

### Deep Learning (PyTorch):

- **Akurasi Validasi**: 94%
- **F1-Score**: 0.91
- **Precision**: 0.92, **Recall**: 0.91

### Support Vector Machine (SVM):

- **Akurasi**: 87%
- **F1-Score**: 0.87
- **Precision dan Recall** tertinggi pada kelas **netral** (F1-Score 0.91), sedangkan **positive** memiliki F1-Score 0.84.
- Kelas **negative** memiliki F1-Score terendah yaitu 0.74.

Model Deep Learning secara umum memiliki performa yang lebih baik dibandingkan SVM dalam hal akurasi dan F1-score.

## Kesimpulan

- Model **Deep Learning (PyTorch)** menunjukkan performa yang lebih baik dengan akurasi dan F1-score lebih tinggi dibandingkan dengan **SVM**.
- Jika diperlukan, lakukan **hyperparameter tuning** untuk meningkatkan performa lebih lanjut pada kedua model.
- Anda juga bisa mencoba teknik **Grid Search** pada SVM untuk menemukan parameter optimal.
