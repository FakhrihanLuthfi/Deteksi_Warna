
Project UAS Segmentasi Mendeteksi Warna

 [FakhrihanLuthfi](https://github.com/FakhrihanLuthfi)

 [Referensi Jurnal](https://www.researchgate.net/publication/356849873_Deteksi_Warna_Manggis_Menggunakan_Pengolahan_Citra_dengan_Opencv_Python)
 
Tujuan dari deteksi warna buah dalam pengolahan citra adalah untuk secara otomatis mengenali, mengklasifikasikan, memisahkan, dan menghitung buah berdasarkan warna kulitnya. Deteksi warna buah melibatkan penggunaan metode pengolahan citra dan analisis warna untuk mengidentifikasi dan memahami informasi warna yang terkandung dalam citra buah.

Proses deteksi warna buah dimulai dengan memecah citra menjadi komponen warna utama menggunakan model warna RGB atau ruang warna lain seperti HSV. Dalam model RGB, setiap piksel dalam citra memiliki komponen merah (R), hijau (G), dan biru (B). Nilai intensitas ini mencerminkan kombinasi warna yang membentuk warna kulit buah. Misalnya, kombinasi tinggi pada komponen merah dan rendah pada komponen hijau dan biru dapat menunjukkan warna kulit buah yang merah.

Selanjutnya, dilakukan teknik segmentasi warna untuk memisahkan piksel-piksel yang mewakili warna kulit buah dari latar belakang atau objek lain dalam citra. Metode segmentasi warna seperti thresholding, clustering, atau pendekatan lainnya digunakan untuk membagi piksel-piksel ke dalam dua kelas berdasarkan ambang batas warna yang ditentukan. Teknik segmentasi ini memungkinkan pemisahan warna kulit buah yang diinginkan dari komponen lain dalam citra, sehingga mempermudah identifikasi dan analisis selanjutnya.

Setelah piksel-piksel warna kulit buah berhasil tersegmentasi, langkah berikutnya adalah mengklasifikasikan buah berdasarkan warna kulitnya. Dalam proses ini, buah-buah dengan warna kulit yang serupa dikelompokkan bersama. Metode klasifikasi seperti pengenalan pola dan pengaturan kriteria warna tertentu digunakan untuk mengidentifikasi dan membedakan jenis buah berdasarkan warna kulitnya. Misalnya, buah dengan kulit merah seperti apel dan cherry dapat diklasifikasikan sebagai buah merah, sedangkan buah dengan kulit kuning seperti pisang dan lemon dapat diklasifikasikan sebagai buah kuning.

Selain itu, deteksi warna buah juga membantu dalam memisahkan buah dari latar belakang atau objek lain dalam citra. Dengan menggunakan teknik segmentasi warna yang tepat, piksel-piksel warna kulit buah dapat diisolasi dengan lebih baik, sehingga memudahkan dalam proses deteksi dan analisis selanjutnya. Pemisahan ini dapat dilakukan dengan mempertimbangkan perbedaan intensitas warna antara buah dan latar belakangnya, serta menggunakan metode morfologi untuk memperbaiki hasil segmentasi.

Salah satu manfaat penting dari deteksi warna buah adalah kemampuannya untuk menghitung jumlah buah dalam citra. Dengan mengenali dan menghitung setiap buah yang memiliki warna kulit yang sama, dapat dilakukan estimasi jumlah buah secara otomatis. Informasi ini sangat berharga dalam aplikasi pertanian, pemrosesan buah, dan

industri makanan. Misalnya, dalam industri pemrosesan buah dan sayuran, deteksi warna buah dapat digunakan untuk memisahkan buah yang tidak memenuhi standar kualitas berdasarkan warna kulitnya. Dengan adanya sistem deteksi warna buah yang akurat, buah-buah yang tidak memenuhi kriteria dapat diidentifikasi dan dipisahkan secara otomatis, sehingga meminimalkan risiko produk yang tidak memenuhi standar kualitas yang diinginkan.

Di bidang pertanian, deteksi warna buah juga dapat digunakan untuk memantau pertumbuhan dan kematangan buah. Dengan mengidentifikasi perubahan warna kulit buah dari waktu ke waktu, petani dapat memperoleh informasi tentang tahap kematangan buah dan menentukan waktu yang tepat untuk panen. Hal ini dapat membantu meningkatkan efisiensi dalam pengelolaan tanaman dan mengoptimalkan hasil panen.

Selain itu, deteksi warna buah memiliki aplikasi penting dalam industri makanan. Misalnya, dalam industri pembuatan jus buah, deteksi warna buah dapat digunakan untuk memisahkan buah yang sesuai dengan standar kualitas dan memastikan keberadaan buah yang mengandung pigmen yang diperlukan untuk menghasilkan warna jus yang diinginkan. Dengan demikian, deteksi warna buah dapat membantu meningkatkan kualitas dan konsistensi produk makanan yang menggunakan buah sebagai bahan baku.

Penggunaan OpenCV Python dalam deteksi warna buah menjadi penting karena OpenCV merupakan library yang kuat dan populer untuk pengolahan citra dan analisis warna. OpenCV menyediakan berbagai fungsi dan algoritma yang dapat digunakan untuk segmentasi warna, thresholding, morfologi, dan fitur-fitur lain yang diperlukan dalam deteksi warna buah. Dengan memanfaatkan fitur-fitur OpenCV, peneliti dan pengembang dapat mengimplementasikan sistem deteksi warna buah yang efektif dan efisien.

Dalam kesimpulannya, deteksi warna buah dalam pengolahan citra memiliki tujuan utama untuk mengoptimalkan dan mengotomatisasi proses identifikasi, klasifikasi, pemisahan, dan penghitungan buah berdasarkan warna kulitnya. Metode pengolahan citra dan analisis warna digunakan untuk mengolah citra buah, memisahkan piksel-piksel warna kulit buah, dan mengklasifikasikan buah berdasarkan warna. Deteksi warna buah memiliki berbagai aplikasi praktis dalam industri pertanian, pemrosesan buah, industri makanan, serta penelitian ilmiah dan pengembangan teknologi. Penggunaan teknologi deteksi warna buah dapat membantu meningkatkan kualitas produk, efisiensi pertanian, dan konsistensi produk makanan yang menggunakan buah sebagai bahan baku.

Langkah - Langkah Yang Dilakukan Untuk Membuat Program
Langkah 1: Persiapkan image (dataset) beberapa buah yang warnanya berbeda

Langkah 2: Install dependencies, beberapa library yang diperlukan seperti numpy, cv2, dan matplotlib

Langkah 3: Mulai lakukan proses dengan langkah-langkah seperti membaca gambar. Kemudian hasil deteksi dilakukan proses perubahan dari BGR ke HSV.

Langkah 4: Hasil output diperhatikan, jika berhasil maka selesai dan jika tidak maka balik ke langkah 1 dengan memepersiapkan dataset yang baik dan terbaca.

berikut Library yang di gunakan adalah cv2 , numpy dan matplotlib
```python
import cv2 as cv
import numpy as np
from matplotlib import pyplot as plt
```
pada program di bawah ini Kita akan memasukkan file photo yang kita sudah buat sebelumnya dengan imread

```python
img = cv.imread('./buah.jpeg')
```
program di bawah ini menggunakan OpenCV untuk mengubah citra warna dari ruang warna BGR ke HSV
Konversi dari ruang warna BGR (Blue-Green-Red) ke HSV (Hue-Saturation-Value) biasanya dilakukan karena HSV lebih sesuai untuk mendeteksi dan memanipulasi objek berdasarkan warna. Dalam ruang warna HSV, komponen utama yang digunakan adalah:

```python
hsv_layer = cv.cvtColor(img, cv.COLOR_BGR2HSV)
```
- Hue (H): Representasi sudut dalam lingkaran warna, di mana 0° dan 360° adalah merah, 120° adalah hijau, dan 240° adalah biru.
- Saturation (S): Intensitas warna. Semakin tinggi nilainya, semakin jenuh warna tersebut.
- Value (V): Intensitas kecerahan. Nilai tinggi mendekati warna murni, sementara nilai rendah mendekati warna gelap.

program di bawah ini membuat sebuah masker yang mengisolasi warna merah dalam citra berdasarkan ruang warna HSV. 
```python
lower_red = np.array([0, 100, 100])
upper_red = np.array([10, 255, 255])
red_mask = cv.inRange(hsv_layer, lower_red, upper_red)
```
- lower_red dan upper_red adalah batas bawah dan atas untuk rentang warna merah dalam ruang warna HSV.
- Nilai batas bawah [0, 100, 100] menunjukkan bahwa kita ingin mendeteksi warna merah yang memiliki hue (H) antara 0 dan 10 (karena 0 dan 10 termasuk dalam rentang inclusive), saturation (S) lebih dari atau sama dengan 100, dan value (V) juga lebih dari atau sama dengan 100.
- Nilai batas atas [10, 255, 255] menunjukkan bahwa kita ingin mendeteksi warna merah yang memiliki hue (H) antara 0 dan 10, saturation (S) kurang dari atau sama dengan 255, dan value (V) juga kurang dari atau sama dengan 255.
- cv.inRange() adalah fungsi OpenCV yang digunakan untuk membuat masker berdasarkan rentang nilai dalam ruang warna tertentu. Parameter pertama (hsv_layer) adalah citra dalam ruang warna HSV yang ingin kita proses. Parameter kedua (lower_red) adalah batas bawah rentang warna yang ingin kita deteksi. Parameter ketiga (upper_red) adalah batas atas rentang warna yang ingin kita deteksi. Hasil dari cv.inRange() adalah masker berupa citra biner di mana piksel putih menunjukkan piksel yang sesuai dengan rentang warna merah, sedangkan piksel hitam menunjukkan piksel yang tidak sesuai dengan rentang warna merah.

program di bawah ini menghilangkan atau menghapus semua piksel yang terdeteksi sebagai warna merah dalam citra asli

```python
non_red_mask = cv.bitwise_not(red_mask)
red_obj = img.copy()
red_obj[non_red_mask != 0] = [0, 0, 0]
```
- red_mask adalah masker yang telah dibuat sebelumnya untuk mendeteksi warna merah dalam citra.
- cv.bitwise_not() adalah fungsi OpenCV yang digunakan untuk menghasilkan masker kebalikan dari red_mask. Ini akan menghasilkan citra masker yang membalik piksel putih menjadi hitam dan sebaliknya.
- non_red_mask adalah citra masker yang telah dibalik.
- img.copy() digunakan untuk menduplikasi citra asli (img) sehingga tidak mengubah citra aslinya.
- red_obj adalah salinan citra asli.
- red_obj[non_red_mask != 0] = [0, 0, 0] digunakan untuk mengubah semua piksel dalam red_obj yang sesuai dengan piksel bukan merah (piksel dengan nilai bukan 0 dalam non_red_mask) menjadi nol, menghasilkan piksel hitam pada citra red_obj. Dengan kata lain, semua piksel yang terdeteksi sebagai warna merah dalam citra asli akan diubah menjadi hitam.

program di bawah ini menggunakan OpenCV dan Matplotlib untuk menampilkan citra red_obj dengan skema warna RGB menggunakan fungsi plt.imshow()

```python
non_red_mask = cv.bitwise_not(red_mask)
red_obj = img.copy()
red_obj[non_red_mask != 0] = [0, 0, 0]
```

- red_obj adalah citra yang telah diproses sebelumnya dan menghilangkan semua piksel yang terdeteksi sebagai warna merah.
- cv.cvtColor() adalah fungsi OpenCV yang digunakan untuk mengubah ruang warna citra. Parameter pertama (red_obj) adalah citra yang akan diubah. Parameter kedua (cv.COLOR_BGR2RGB) adalah flag yang menunjukkan konversi dari ruang warna BGR ke RGB.
- red_obj diubah menjadi skema warna RGB.
- plt.imshow() adalah fungsi dari Matplotlib yang digunakan untuk menampilkan citra. Parameter pertama (red_obj) adalah citra yang akan ditampilkan

## Output merah

[hasil Output merah](https://ibb.co/pnG8Dnv)

program di bawah ini menggunakan nilai batas atas (upper_yellow) dan batas bawah (lower_yellow) yang berbeda untuk mendeteksi warna kuning dalam citra berdasarkan ruang warna HSV.

```python
upper_yellow = np.array([24, 255, 255])
lower_yellow = np.array([10, 120, 80])
yellow_mask = cv.inRange(hsv_layer, lower_yellow, upper_yellow)
non_yellow_mask = cv.bitwise_not(yellow_mask)
```
- lower_yellow dan upper_yellow adalah batas bawah dan atas untuk rentang warna kuning dalam ruang warna HSV.
- Nilai batas bawah [10, 120, 80] menunjukkan bahwa kita ingin mendeteksi warna kuning yang memiliki hue (H) antara 10 dan 24, saturation (S) lebih dari atau sama dengan 120, dan value (V) juga lebih dari atau sama dengan 80.
- Nilai batas atas [24, 255, 255] menunjukkan bahwa kita ingin mendeteksi warna kuning yang memiliki hue (H) antara 10 dan 24, saturation (S) kurang dari atau sama dengan 255, dan value (V) juga kurang dari atau sama dengan 255.
- cv.inRange() adalah fungsi OpenCV yang digunakan untuk membuat masker berdasarkan rentang nilai dalam ruang warna tertentu. Parameter pertama (hsv_layer) adalah citra dalam ruang warna HSV yang ingin kita proses. Parameter kedua (lower_yellow) adalah batas bawah rentang warna yang ingin kita deteksi. Parameter ketiga (upper_yellow) adalah batas atas rentang warna yang ingin kita deteksi. Hasil dari cv.inRange() adalah masker berupa citra biner di mana piksel putih menunjukkan piksel yang sesuai dengan rentang warna kuning, sedangkan piksel hitam menunjukkan piksel yang tidak sesuai dengan rentang warna kuning.
- cv.bitwise_not() digunakan untuk membalikkan masker kuning menjadi masker non-kuning, sehingga piksel yang sesuai dengan warna kuning menjadi hitam dan sebaliknya.
- non_yellow_mask adalah citra masker yang telah dibalik.

Program di bawah ini digunakan untuk menghapus atau mengubah piksel yang tidak terdeteksi sebagai warna kuning dalam citra.

```python
upper_yellow = np.array([24, 255, 255])
lower_yellow = np.array([10, 120, 80])
yellow_mask = cv.inRange(hsv_layer, lower_yellow, upper_yellow)
non_yellow_mask = cv.bitwise_not(yellow_mask)
```
- img adalah citra asli yang ingin diproses.
- ylw_obj adalah salinan citra asli yang dibuat menggunakan img.copy(). Ini dilakukan untuk memastikan bahwa citra asli tidak berubah saat kita melakukan pemrosesan.
non_yellow_mask adalah citra masker yang menunjukkan piksel yang tidak terdeteksi sebagai warna kuning.
- ylw_obj[non_yellow_mask != 0] adalah operasi slicing yang digunakan untuk memilih piksel dalam ylw_obj yang sesuai dengan piksel non-kuning (piksel dengan nilai bukan 0 dalam non_yellow_mask).
- [0, 0, 0] adalah nilai piksel yang ditetapkan untuk piksel yang dipilih. Dalam hal ini, kita mengubah piksel non-kuning menjadi hitam dengan mengatur nilai piksel menjadi [0, 0, 0].
- Dengan menggunakan operasi slicing dan penugasan nilai, piksel-piksel yang tidak terdeteksi sebagai warna kuning dalam citra akan diubah menjadi hitam pada citra ylw_obj.

Program di bawah ini digunakan untuk mengubah skema warna citra ylw_obj dari BGR (Blue-Green-Red) ke RGB (Red-Green-Blue)

```python
ylw_obj = cv.cvtColor(ylw_obj, cv.COLOR_BGR2RGB)
```
- ylw_obj adalah citra yang telah diproses sebelumnya dan menghilangkan piksel yang tidak terdeteksi sebagai warna kuning.
- cv.cvtColor() adalah fungsi OpenCV yang digunakan untuk mengubah skema warna citra. Parameter pertama (ylw_obj) adalah citra yang akan diubah. Parameter kedua (cv.COLOR_BGR2RGB) adalah flag yang menunjukkan konversi dari skema warna BGR ke RGB.
- ylw_obj diubah menjadi skema warna RGB

Program di bawah ini menggunakan Matplotlib untuk menampilkan citra ylw_obj dengan skema warna grayscale

```python
plt.imshow(ylw_obj, cmap='gray')
```
- ylw_obj adalah citra yang ingin ditampilkan.
- plt.imshow() adalah fungsi dari Matplotlib yang digunakan untuk menampilkan citra. Parameter pertama (ylw_obj) adalah citra yang akan ditampilkan. Parameter kedua (cmap='gray') adalah argumen opsional yang menentukan skema warna yang digunakan. Dalam hal ini, 'gray' mengacu pada skema warna grayscale.
- Citra ylw_obj ditampilkan menggunakan skema warna grayscale.

##Output kuning

[hasil Output kuning](https://ibb.co/0CYHSLv)

Program di bawah ini digunakan untuk mendeteksi objek yang memiliki warna hijau dalam citra dan menampilkan hanya objek hijau 

```python
green_mask = cv.inRange(hsv_layer, (30, 50, 50), (80, 255, 255))
green_objects = cv.bitwise_and(img, img, mask=green_mask)
green_objects = cv.cvtColor(green_objects, cv.COLOR_BGR2RGB)
```

Program di bawah ini digunakan untuk mendeteksi objek yang memiliki warna hijau dalam citra dan menampilkan hanya objek hijau tersebut:

```python
green_mask = cv.inRange(hsv_layer, (30, 50, 50), (80, 255, 255))
green_objects = cv.bitwise_and(img, img, mask=green_mask)
green_objects = cv.cvtColor(green_objects, cv.COLOR_BGR2RGB)
```

1. `hsv_layer` adalah citra dalam ruang warna HSV.
2. `cv.inRange()` adalah fungsi OpenCV yang digunakan untuk membuat masker dengan membatasi rentang warna. Parameter pertama (`hsv_layer`) adalah citra dalam ruang warna HSV yang ingin kita proses. Parameter kedua adalah batas bawah (lower) dalam rentang warna hijau, yaitu (30, 50, 50) yang menunjukkan nilai Hue (H) minimal, Saturation (S) minimal, dan Value (V) minimal untuk warna hijau. Parameter ketiga adalah batas atas (upper) dalam rentang warna hijau, yaitu (80, 255, 255) yang menunjukkan nilai Hue (H) maksimal, Saturation (S) maksimal, dan Value (V) maksimal untuk warna hijau. Hasil dari `cv.inRange()` adalah masker berupa citra biner di mana piksel putih menunjukkan piksel yang sesuai dengan rentang warna hijau, sedangkan piksel hitam menunjukkan piksel yang tidak sesuai dengan rentang warna hijau.
3. `cv.bitwise_and()` digunakan untuk menerapkan masker hijau (`green_mask`) ke citra asli (`img`). Ini menghasilkan citra `green_objects` di mana hanya piksel yang sesuai dengan warna hijau yang tetap ada, sedangkan piksel non-hijau menjadi hitam.
4. `cv.cvtColor()` digunakan untuk mengubah skema warna citra `green_objects` dari BGR (Blue-Green-Red) ke RGB (Red-Green-Blue). Hal ini dilakukan agar citra dapat ditampilkan dengan benar menggunakan fungsi `plt.imshow()` dari Matplotlib.
5. `green_objects` adalah citra yang hanya menampilkan objek hijau.
6. Citra `green_objects` siap untuk ditampilkan atau digunakan untuk analisis selanjutnya.

Program di bawah ini menggunakan Matplotlib untuk menampilkan citra `green_objects` yang merupakan hasil dari deteksi objek dengan warna hijau:

```python
plt.imshow(green_objects)
```

1. Import library Matplotlib dengan alias `plt`.
2. `green_objects` adalah citra yang ingin ditampilkan. Citra ini merupakan hasil dari proses deteksi objek dengan warna hijau.
3. `plt.imshow()` adalah fungsi dari Matplotlib yang digunakan untuk menampilkan citra. Parameter pertama (`green_objects`) adalah citra yang akan ditampilkan.
4. Citra `green_objects` ditampilkan.

##Output hijau

[hasil Output hijau](https://ibb.co/SPZfWcW)

Program di atas digunakan untuk menampilkan empat gambar secara berdampingan menggunakan Matplotlib. Berikut adalah penjelasan program tersebut:

```python
img = cv.cvtColor(img, cv.COLOR_BGR2RGB)
fig, axs = plt.subplots(1, 4, figsize=(15, 5))
axs = axs.ravel()

axs[0].set_title('gambar asli')
axs[0].imshow(img)

axs[1].set_title('deteksi merah')
axs[1].imshow(red_obj)

axs[2].set_title('deteksi kuning')
axs[2].imshow(ylw_obj)

axs[3].set_title('deteksi hijau')
axs[3].imshow(green_objects)
```

1. `img` adalah citra asli yang ingin ditampilkan.
2. `cv.cvtColor()` digunakan untuk mengubah skema warna citra `img` dari BGR (Blue-Green-Red) ke RGB (Red-Green-Blue). Hal ini dilakukan agar citra dapat ditampilkan dengan benar menggunakan fungsi `plt.imshow()` dari Matplotlib.
3. `fig, axs = plt.subplots(1, 4, figsize=(15, 5))` digunakan untuk membuat satu set subplot dengan 1 baris dan 4 kolom. Ini berarti kita akan menampilkan empat gambar secara berdampingan dalam satu gambar.
4. `axs = axs.ravel()` mengubah matriks dari subplot menjadi array 1D untuk memudahkan pengindeksan.
5. Untuk setiap subplot, dilakukan pengaturan judul dan menampilkan citra menggunakan `axs[i].set_title()` dan `axs[i].imshow()`. `i` adalah indeks subplot yang berkorespondensi dengan gambar yang ingin ditampilkan.
6. Subplot pertama menampilkan citra asli dengan judul 'gambar asli'.
7. Subplot kedua menampilkan citra `red_obj` yang merupakan hasil deteksi objek dengan warna merah.
8. Subplot ketiga menampilkan citra `ylw_obj` yang merupakan hasil deteksi objek dengan warna kuning.
9. Subplot keempat menampilkan citra `green_objects` yang merupakan hasil deteksi objek dengan warna hijau.

##Hasil gabungan deteksi warna buah

[hasil Output gabungan](https://ibb.co/dWHtqvZ)

