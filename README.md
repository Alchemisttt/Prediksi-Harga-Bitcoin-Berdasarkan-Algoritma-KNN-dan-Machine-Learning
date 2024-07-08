# Prediksi Harga Bitcoin Berdasarkan Algoritma KNN dan Machine Learning


### Data Source

Data csv berada pada folder "Data/Bitcoin Historical Data Daily 5yr.csv", data tersebut didapatkan dari investing.com [Download](https://www.investing.com/crypto/bitcoin/historical-data)

### Tools 

   - Python3.12 [Download](https://www.python.org/downloads/)
   - Jupiter Notebooks [Download](https://jupyter.org/)
   - Anaconda Navigator [Download](https://www.anaconda.com/download)
   - Chrome [Download](https://www.google.com/intl/id/chrome/browser-tools/)

### Data Loading

Data historis Bitcoin bisa diunduh dari situs web Investing.com, yang menyediakan data historis akurat dan lengkap mengenai harga Bitcoin, termasuk informasi harga pembukaan, penutupan, tertinggi, terendah, serta volume perdagangan harian. Data dimuat kedalam jupiter notebook agar bisa diolah.


### Data Pre-processing

Data pre-processing bertujuan untuk mempersiapkan data historis Bitcoin agar siap digunakan dalam model prediksi. Proses ini melibatkan beberapa langkah penting:

1.  Pembersihan Data (Data Cleanning): Menghapus atau memperbaiki data yang hilang, duplikat, atau tidak valid untuk memastikan kualitas data yang tinggi.
2.  Transformasi Variabel (Feature Engineering): Memilih dan membuat fitur atau variabel baru yang relevan untuk model prediksi.
3.  Konversi Tipe Data (Data Type Conversion): Mengubah tipe data tertentu agar sesuai dengan kebutuhan analisis, seperti mengonversi string ke format datetime atau mengubah tipe data numerik ke format yang lebih sesuai.

Proses pre-processing ini sangat penting untuk memastikan bahwa data yang digunakan dalam model KNN bersih, terstruktur, dan siap untuk analisis lebih lanjut. Hal ini juga membantu meningkatkan keakuratan dan keandalan prediksi harga Bitcoin.


### Data Splitting

data splitting bertujuan untuk membagi dataset yang telah diproses menjadi dua bagian yaitu training dataset dan testing dataset. Training dataset digunakan untuk melatih model KNN sehingga model dapat mengenali pola dan hubungan dalam data historis. Testing dataset digunakan untuk menguji dan mengevaluasi kinerja model setelah dilatih. Proses ini melibatkan langkah-langkah berikut:

1.	Pembagian Data (Data Splitting): Dataset dibagi menjadi dua set terpisah, dengan rasio 80:20 dimana 80% data digunakan untuk pelatihan (training) dan sisanya untuk pengujian (testing). 
2.	Model Pelatihan (Training Model): Model KNN dilatih menggunakan training dataset untuk mengenali pola dan tren dalam data historis Bitcoin.
3.	Model Pengujian (Testing Model): Model yang telah dilatih kemudian diuji menggunakan testing dataset untuk mengevaluasi keakuratannya dalam memprediksi harga Bitcoin yang belum pernah dilihat sebelumnya.

Pendekatan ini memastikan bahwa model KNN yang dikembangkan dapat menghasilkan prediksi yang andal dan akurat dengan menghindari overfitting dan memastikan bahwa model dapat memgeneralisasi dengan baik pada data baru.


### Model Trainning

Tahap model training bertujuan untuk melatih model KNN menggunakan training dataset yang telah dipisahkan. Pada tahap ini, model belajar mengenali pola dan hubungan dalam data historis Bitcoin agar dapat digunakan untuk membuat prediksi di masa mendatang. Proses model training melibatkan langkah-langkah berikut:

1.	Inisialisasi Model KNN (KNN Model Intialization): Menentukan nilai "k", yaitu jumlah tetangga terdekat yang akan digunakan oleh model untuk membuat prediksi. Nilai "k" yang optimal biasanya ditemukan melalui eksperimen dan validasi silang (cross-validation).
2.	Model Pelatihan (Training Model): Model KNN dilatih dengan menggunakan training dataset, di mana model akan menghitung jarak antara data yang akan diprediksi dan setiap titik data dalam training set, kemudian memilih "k" tetangga terdekat untuk menentukan nilai prediksi.
3.	Performa Evaluasi Model (Evaluate Performa): Selama proses pelatihan, model dievaluasi menggunakan metrik performa Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), R-Squared, Normalized Root Mean Squared Error (NRMSE) untuk memastikan bahwa model belajar dengan baik dan tidak mengalami overfitting atau underfitting.

Proses training ini penting untuk memastikan bahwa model KNN dapat menghasilkan prediksi yang akurat dan dapat diandalkan berdasarkan data historis yang telah disediakan.





