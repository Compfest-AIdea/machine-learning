# Machine Learning
Repositori Machine learning aplikasi Scalpsense dari AIdea Team untuk membangun model machine learning yang mengklasifikasikan penyakit kulit kepala berdasarkan data gambar dan kerontokan rambut berdasarkan data tabular klinis.

## Dataset
- Dataset gambar penyakit kulit kepala: 4800 gambar (alopecia areata, tinea capitis, seborrhoeic dermatitis, scalp psoriasis) yang didapatkan dari website Dermnetnz, Dermatology Atlas, dan Dermaamin dan telah diaugmentasi untuk memperbanyak data serta 1200 gambar kulit kepala normal dari dataset Figaro-1K dataset (https://github.com/UmarSpa/HairAnalysis). 
- Dataset tabular kerontokan rambut: 400 baris data dengan 8 atribut. Dataset mentah diambil dari Kaggle (https://www.kaggle.com/datasets/lukexun/luke-hair-loss-dataset). Setelah eksplorasi, beberapa fitur tidak digunakan.

## Model Development
### Scalp Model
Model klasifikasi gambar penyakit kulit kepala dibuat dengan Tensorflow. <br>
Arsitektur model sebagai berikut.
- Conv2D layer (filter = 32, kernel = (3,3), activation='relu', input_shape=(150,150,3))
- MaxPooling2D layer ((2,2) pool size)
- Conv2D layer (filter = 64, kernel = (3,3), activation='relu')
- MaxPooling2D layer ((2,2) pool size)
- Conv2D layer (filter = 64, kernel = (3,3), activation='relu')
- MaxPooling2D layer ((2,2) pool size)
- Conv2D layer (filter = 32, kernel = (3,3), activation='relu')
- MaxPooling2D layer ((2,2) pool size)
- Flatten layer
- Dropout layer (0.4)
- Dense layer (unit = 64, activation='relu')
- Dropout layer (0.4)
- Dense layer (unit = 5, activation='softmax')

Metrik evaluasi model sebagai berikut.
| Training loss | Training accuracy | Validation loss | Validation accuracy |
| :---: | :---: | :---: | :---: |
| 0.2059 | 0.9189 | 0.3781 | 0.8825 |

![image](https://github.com/Compfest-AIdea/machine-learning/assets/96944447/b486eeac-6465-47b5-b8a1-6715de6c956b)

Confusion matrix pada test data <br>
<img src="https://github.com/Compfest-AIdea/machine-learning/assets/96944447/8d3dca0e-ddf4-4874-94bd-b5d25929edee" width="370" />

| Rata-rata Precision | Rata-rata Recall | Rata-rata F1-Score |
| :---: | :---: | :---: |
| 0.8551768428890544 | 0.8558333333333333 | 0.8552587922242569 |

### Hairloss Model
Model klasifikasi tingkat kerontokan rambut dibuat dengan Tensorflow. <br>
Arsitektur model sebagai berikut.
- Input layer (shape = 8)
- Dense layer (unit = 64, activation = 'relu')
- Dropout layer (0.2)
- Dense layer (unit = 32, activation = 'relu')
- Dense layer (unit = 32, activation = 'relu')
- Dense(unit = 4, activation='softmax')

Metrik evaluasi model sebagai berikut. <br>
| Training loss | Training accuracy | Validation loss | Validation accuracy |
| :---: | :---: | :---: | :---: |
| 0.2251 | 0.9172 | 0.3335 | 0.89 |

<img src="https://github.com/Compfest-AIdea/machine-learning/assets/96944447/897a2ab4-8eff-47be-9b89-5324e8b613d0" width="370" />
<img src="https://github.com/Compfest-AIdea/machine-learning/assets/96944447/e5d4b179-9d55-4ba7-a2a7-5af521d8d9f2" width="370" />

Confusion matrix pada test data <br>
<img src="https://github.com/Compfest-AIdea/machine-learning/assets/96944447/a01be720-a901-49fb-80d9-a2bdc6e0dde2" width="500" />

| Rata-rata Precision | Rata-rata Recall | Rata-rata F1-Score |
| :---: | :---: | :---: |
| 0.9191921052553236 | 0.9033734939759036 | 0.9101019312758835 |
