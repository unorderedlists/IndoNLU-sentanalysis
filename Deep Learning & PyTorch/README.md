# Analisis Sentimen dengan Deep Learning & PyTorch📊

Proyek ini menggunakan model Deep Learning yang dilatih menggunakan PyTorch untuk melakukan analisis sentimen pada teks berbahasa Indonesia. Proyek ini merupakan bagian dari studi untuk membandingkan performa Deep Learning dengan SVM dalam mengklasifikasikan sentimen.

## Daftar Isi

- [Pendahuluan](#pendahuluan)
- [Dataset](#dataset)
- [Instalasi](#instalasi)
- [Kesimpulan](#kesimpulan)

## Pendahuluan

Dalam proyek ini, kita akan menggunakan model Deep Learning (PyTorch) untuk mengklasifikasikan teks berbahasa Indonesia menjadi sentimen positif, netral, atau negatif. Model ini merupakan salah satu klasifikasi yang digunakan untuk mengevaluasi hasil analisis sentimen.

## Dataset

Dataset yang digunakan berasal dari IndoNLU, yang sudah melalui proses preprocessing untuk keperluan analisis sentimen. Dataset ini berisi teks yang dilabeli dengan tiga kategori sentimen: positif, netral, dan negatif.

Untuk informasi lebih lanjut tentang dataset, kunjungi [IndoNLU](https://github.com/indobenchmark/indonlu).

## Instalasi

Untuk menjalankan proyek ini, instalasi berikut diperlukan:

- torch
- transformers

Instal semua dependensi dengan perintah berikut:

```bash
pip install torch torchvision
```

```bash
pip install transformers
```

Import seluruh library yang diperlukan:

```python
import random
import numpy as np
import pandas as pd
import torch
from torch import optim
import torch.nn.functional as F
from tqdm import tqdm

from transformers import BertForSequenceClassification, BertConfig, BertTokenizer
from nltk.tokenize import TweetTokenizer

from indonlu.utils.forward_fn import forward_sequence_classification
from indonlu.utils.metrics import document_sentiment_metrics_fn
from indonlu.utils.data_utils import DocumentSentimentDataset, DocumentSentimentDataLoader
```

## Kesimpulan

Hasil dari pelatihan model Deep Learning (PyTorch) menunjukkan akurasi 94%, dengan F1-Score sebesar 0.91. Model ini memberikan performa terbaik dibandingkan dengan metode lain, terutama dalam hal sentimen netral dan positif.
