# Analisis Sentimen dengan SVM⚙️

Proyek ini menggunakan Support Vector Machine (SVM) untuk mengklasifikasikan teks berbahasa Indonesia ke dalam kategori sentimen positif, netral, atau negatif. Proyek ini merupakan bagian dari studi untuk membandingkan performa SVM dengan Deep Learning.

## Daftar Isi

- [Pendahuluan](#pendahuluan)
- [Dataset](#dataset)
- [Instalasi](#instalasi)
- [Kesimpulan](#kesimpulan)

## Pendahuluan

Dalam proyek ini, Support Vector Machine (SVM) digunakan sebagai metode klasifikasi untuk melakukan analisis sentimen. Tujuannya adalah untuk memprediksi sentimen berdasarkan data teks yang disediakan.

## Dataset

Dataset yang digunakan sama dengan yang ada di proyek utama, yaitu dari IndoNLU, dengan label sentimen positif, netral, dan negatif.

Untuk informasi lebih lanjut tentang dataset, kunjungi [IndoNLU](https://github.com/indobenchmark/indonlu).

## Instalasi

Import seluruh library yang diperlukan:

```python
import pandas as pd

%matplotlib inline
import matplotlib.pyplot as plt
from wordcloud import WordCloud
from sklearn.feature_extraction.text import CountVectorizer, TfidfTransformer, TfidfVectorizer
from sklearn import svm
from sklearn.metrics import classification_report
```

## Kesimpulan

Hasil evaluasi menunjukkan bahwa model SVM memiliki akurasi sebesar 87%. F1-Score tertinggi diperoleh untuk kategori netral (0.91), sementara F1-Score terendah terdapat pada kategori negatif (0.74). Model ini bisa diperbaiki lebih lanjut dengan melakukan hyperparameter tuning, seperti menggunakan Grid Search untuk mencari parameter optimal.
