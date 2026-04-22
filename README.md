## UTS Machine Learning
<div>
  
![Profil](https://img.shields.io/badge/111-Putri%20Puspita%20%7C%206C-blue)
![TI](https://img.shields.io/badge/Teknik%20Informatika-gray)
![UIN](https://img.shields.io/badge/UIN%20Sunan%20Gunung%20Djati%20Bandung-blue)

</div>

## Data Collecting
Dataset yang digunakan dalam proyek diperoleh dari platform Kaggle

<div>

[![Dataset](https://img.shields.io/badge/Dataset-Oranges%20vs%20Grapefruit-blue)](https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit)

</div>

Dataset terdiri dari beberapa fitur yaitu:
- diameter → ukuran diameter buah
- weight → berat buah
- red → intensitas warna merah
- green → intensitas warna hijau
- blue → intensitas warna biru
- name → label kelas (orange / grapefruit)

## Exploratory Data Analysis (EDA)
**Pada tahap ini dilakukan visualisasi untuk memahami karakteristik data dengan melakukan :** 
- Visualisasi boxplot untuk melihat apakah terdapat outlier atau tidak
- Visualisasi histogram untuk melihat sebaran data terhadap label atau target

**Hasil yang diperoleh**
- Berdasarkan visualisasi boxplot, terdapat beberapa outlier atau nilai yang keluarr dari whisker pada fitur diameter, red, green, dan blue. Fitur blue menunjukan adanya outlier extrem sehingga distribusi datanya tidak merata. sedangkan untuk fitur diameter hanya memiliki sedikit outlier sehingga masih dalam batas wajar dan fitur weight tidak memiliki outlier.
- Fitur weight dan diameter memiliki distribusi yang paling jelas dalam membedakan kelas, sedangkan fitur red dan green memiliki overlap sedang. Fitur blue memiliki overlap tinggi dan distribusi miring ke kanan

## Preprocessing
- Encoding Label : Merubah data label (kolom name) menjadi numerik dengan menggunakan label encoder
- Splitting data : Membagi dataset menjadi data latihan 80% (8000 data) dan data test 20% (2000 data)
- Scalling : Melakukan standardisasi pada semua fitur numerik
- Tidak dilakukan proses penghapusan outlier dikarenakan dalam batas wajar dan merepresentasikan data alami

## Modelling & Evaluasi Model
**Decission Tree**
![Alt text](Gamba/dt.png)
