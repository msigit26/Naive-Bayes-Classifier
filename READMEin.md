# Naive Bayes Classifier

Algoritma Naive Bayes merupakan salah satu algoritma yang terdapat pada teknik klasifikasi. Klasifikasi adalah salah satu teknik data mining untuk mengelompokkan data berdasarkan kelas atau label yang telah ditentukan. Data mining adalah penambangan atau penemuan informasi baru dengan mencari pola atau aturan tertentu dari sejumlah data yang sangat besar. Data mining juga disebut sebagai serangkaian proses untuk menggali nilai tambah berupa pengetahuan yang selama ini tidak diketahui secara manual dari suatu kumpulan data.

Naive Bayes merupakan pengklasifikasian dengan metode probabilitas dan statistik yang dikemukan oleh ilmuwan Inggris Thomas Bayes, yaitu memprediksi peluang di masa depan berdasarkan pengalaman dimasa sebelumnya sehingga dikenal sebagai Teorema Bayes. Pendekatan yang digunakan Teorema Bayes yaitu menghitung probabilitas sebuah kejadian pada kondisi tertentu (Lukito & Chrismanto, 2015). 

## Penggunaan

Data yang digunakan diatas yaitu data numerik/ kontinyu dan menggunakan fungsi `GaussianNB` pada library `scikit-learn`. Proses memasukkan data latih dan data uji yaitu pada:
```
datalatih = pd.read_excel("data training numerik.xlsx")
datauji = pd.read_excel("data testing numerik.xlsx")
```


__Pelatihan data__
```
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import GaussianNB
modelnb = GaussianNB()
nbtrain = modelnb.fit(x, y)
```

__Membuat Prediksi__
```
Y_predict = nbtrain.predict(x_test)
print("Prediksi Naive Bayes : ",Y_predict)
```

__Menghitung Akurasi__
```
from sklearn.metrics import accuracy_score
accuracy= accuracy_score(y_uji, Y_predict)
print("Akurasi Naive Bayes : ",accuracy)

from sklearn.metrics import classification_report
print(classification_report(y_uji, Y_predict))
```


Sumber yang digunakan sebagai referensi dapat diakses [disini](https://github.com/edy-kurniawan/naive-bayes-classifier-python).
