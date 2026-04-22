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
<h2>Decision Tree</h2>

<p align="center">
  <img src="Gambar/dt.png" height="250"/>
  <img src="Gambar/cm_dt.png" height="250" />
</p>

**Precission (Ketepatan)**
- Grapefruit : Dari semua buah yang ditebak grapefruit oleh model 95% itu benar dan 5% yang seharusnya orange malah ditebak grapefruit
- Orange : Dari semuah buah yang ditebak orange oleh model 94% itu benar

**Recall (Keberhasilan Menangkap)**
- Dari seluruh data grapefruit yang seharusnya ada yaitu sebanyak 1011 data, model berhasil mengidentifikasi sekitar 94% atau ±950 data sebagai grapefruit. Sementara itu, sekitar 6% atau ±61 data tidak berhasil dikenali sebagai grapefruit dan salah diklasifikasikan sebagai orange.
-Dari seluruh data orange yang seharusnya ada yaitu sebanyak 989 data, model berhasil mengidentifikasi sekitar 95% atau ±939 data sebagai orange. Sementara itu, sekitar 5% atau ±50 data tidak berhasil dikenali sebagai orange dan salah diklasifikasikan sebagai grapefruit.

**F1-Score**
Nilai f1-score yang diperoleh untuk kedua kelas berada di kisaran 0.94–0.95, yang menunjukkan bahwa model memiliki keseimbangan yang baik antara precision dan recall.

**Support**
- Grapefruit : Jumlah Data 10111
- Orange : Jumlah Data 989

**Confussion Matrix**
- Pada kelas grapefruit, model berhasil mengklasifikasikan 952 data dengan benar. Namun terdapat 59 data yang seharusnya termasuk grapefruit tetapi diprediksi sebagai orange.
- Pada kelas orange, model berhasil mengklasifikasikan 938 data dengan benar. Namun terdapat 51 data yang seharusnya termasuk orange tetapi diprediksi sebagai grapefruit
