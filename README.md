## Team Member - ML

| Bangkit ID | Name | Learning Path | University |LinkedIn |
| ---      | ---       | ---       | ---       | ---       |
| M312B4KY1803 | Humam Alwi Ahmad | Machine Learning| Universitas Sebelas Maret | [![text](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/humam-alwi-ahmad-46a440311) |
| M312B4KY1487 | Ferdy Rizkiawan | Machine Learning|	Universitas Sebelas Maret  | [![text](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ferdyrizkiawan) |
| M312B4KX1981 | Inge Najwa Aqiilah | Machine Learning| Universitas Sebelas Maret| [![text](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/inge-najwa-aqiilah-226667310) |

## Deskripsi Proyek
Divisi Machine Learning bertanggung jawab untuk mengembangkan model klasifikasi yang mendukung aplikasi utama. Proyek ini mencakup dua model utama:

1. **Model Klasifikasi Jenis Kulit** (`model_skintype.h5`) - Mengidentifikasi jenis kulit dari gambar wajah.
2. **Model Klasifikasi Kondisi Kulit** (`model_skinconditions.h5`) - Mendeteksi kondisi kulit seperti jerawat, noda, atau masalah lainnya dari gambar wajah.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki:

1. **Python 3.8 atau lebih baru**
2. **TensorFlow**
3. **Jupyter Notebook** (opsional, jika ingin mengedit atau menjalankan file `.ipynb`)

### Instalasi Dependensi
Gunakan perintah berikut untuk menginstal semua dependensi yang diperlukan:

```bash
pip install tensorflow numpy matplotlib
```

## Struktur Proyek

- `Face_condition_classifier.ipynb` : Notebook untuk melatih dan menguji model kondisi kulit.
- `Face_type_classifier.ipynb` : Notebook untuk melatih dan menguji model jenis kulit.
- `model_skintype.h5` : File model untuk klasifikasi jenis kulit.
- `model_skinconditions.h5` : File model untuk klasifikasi kondisi kulit.

## Cara Menggunakan

### 1. Melatih Model (Opsional)
Jika Anda ingin melatih ulang model, ikuti langkah-langkah ini:

1. Buka file `.ipynb` di Jupyter Notebook atau IDE yang mendukung notebook seperti VSCode.
2. Ikuti setiap sel untuk:
   - Memuat dataset.
   - Melakukan preprocessing data.
   - Melatih model.
3. Simpan model dengan format `.h5`:
   ```python
   model.save("model_skintype.h5")
   ```

### 2. Menggunakan Model
Untuk memuat model yang telah dilatih, gunakan kode berikut:

```python
import tensorflow as tf

# Memuat model jenis kulit
model_skintype = tf.keras.models.load_model("model_skintype.h5")

# Memuat model kondisi kulit
model_skinconditions = tf.keras.models.load_model("model_skinconditions.h5")
```

### 3. Mengekspor Model ke TensorFlow SavedModel
Gunakan perintah berikut untuk mengekspor model ke format SavedModel:

```python
model.save("saved_model/model_skintype", save_format="tf")
model.save("saved_model/model_skinconditions", save_format="tf")
```

## Catatan Penting

- **Format Dataset**: Pastikan dataset telah diorganisasi dengan benar sebelum memulai pelatihan. Dataset harus dibagi ke dalam folder berdasarkan labelnya.
- **Kompabilitas TensorFlow**: Model ini kompatibel dengan TensorFlow versi 2.6 atau lebih baru.



