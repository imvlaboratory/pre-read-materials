BANNER STUDY GROUP
----
<h1 align="center"> Convolutional Neural Network (CNN) </h1>

<p align="center">
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white" style="vertical-align:middle">
</p>

## Defini Convolutional Neural Network

## Arsitektur Convolutional Neural Network

<p align="center">
    <img src="contents/overview cnn.ppm" alt="overview cnn" width="480" style="vertical-align:middle">
</p>

### Convolution Backbone

#### Convolution Layer

Convolutional layer merupakan proses konvolusi citra input dengan filter yang 
menghasilkan `feature map` (fitur-fitur penting sebuah gambar).

Proses konvolusi citra dengan filter dilakukan `sliding filter` mulai dari kiri atas dari 
matrik citra sampai kanan bawah

<p align="center">
    <img src="contents/convolution.gif" alt="convolution" width="360" style="vertical-align:left">
    <img src="contents/convolution.png" alt="convolution" width="640" style="vertical-align:right">
</p>

```
tf.keras.layers.Conv2D(
    filters,
    kernel_size,
    strides=(1, 1),
    padding='valid',
    activation=None,
    input_shape=(height, width, color_channels)
)
```

- filters → dimensi ruang output → jumlah filter output dalam konvolusi
- kernel_size → ukuran spasial dari filter (lebar/tinggi)
- stride → besar pergeseran filter dalam konvolusi
- padding → jumlah penambahan nol pada gambar
    - valid → tidak ada padding
    - same → padding nol merata kiri/kanan/atas/bawah
- activation → fungsi aktivasi untuk digunakan
- input_shape → input gambar

#### Batch Normalization
Batch Normalization → mengurangi pergeseran kovarian atau menyamakan distribusi setiap nilai input yang selalau berubah karena perubahan pada layer sebelumnya selama proses training.

```
tf.keras.layers.BatchNormalization()
```

#### Pooling Layer

Pooling layer berperan untuk memperkecil dimensi feature image (downsampling) dan menyimpan informasi penting.

<p align="center">
    <img src="contents/pooling.png" alt="pooling" width="640" style="vertical align:middle">
</p>

```
tf.keras.layers.MaxPool2D(
    pool_size=(2, 2),
    strides=None,
    padding='valid',
)
```

- pool_size → ukuran pool
- strides → besar pergeseran
- padding → jumlah penambahan nol pada gambar
    - valid → tidak ada padding
    - same → padding nol merata kiri/kanan/atas/bawah

### Classifier Head (ANN)

#### Flatten dan Global Average Pooling

Flatten dan Global Average Pooling berperan sebagai `input layer`.

<p align="center">
    <img src="contents/fully connected layer vs global average pooling.png" alt="fully connected layer vs global average pooling" width="640" style="vertical align:middle">
</p>

|   Flatten    |    Global Average Pooling                |
|            ---             |                       ---                |
|      hxwxd (1 dimension)   |               d (1 dimension)            |
| tf.keras.layers.Flatten()  | tf.keras.layers.GlobalAveragePooling2D() |

### Hidden Layer

```
tf.keras.layers.Dense(units, activation=None)
```
- units → dimensi ruang output
- activation → fungsi aktivasi untuk digunakan → relu
  
  
### Output Layer

Jumlah neuron sesuai dengan permasalahan.
- Untuk `klasifikasi binary dan regresi` menggunakan `satu neuron`.
- Untuk `klasifikasi multiclass atau categorical` menggunakan `jumlah neuron sesuai jumlah kelas`.

```
tf.keras.layers.Dense(units, activation=None)
```
- units → dimensi ruang output
  - binary → satu neuron.
  - categorical → jumlah neuron sesuai jumlah kelas.
- activation → fungsi aktivasi untuk digunakan

| activation  | output/class mode | loss function | 
|     ---     |        ---        |     ---       |
|   sigmoid   |      binary       |  binary_crossentropy → 0/1 |
|   softmax   |   categorical     |     categorical_crossentropy → [1 0] [0 1]|
|   softmax   |   categorical     |  sparse_categorical_crossentropy → [0] [1] |

## Stratego Proses Pembelajaran

### Modifikasi Network
- Merubah arsitektur, misalnya menambah jumlah hidden layer, jumlah neuron, atau jenis arsitektur lain
- Merubah fungsi aktivasi, misalnya menggunakan ReLU

### Optimasi parameter
Nilai learning rate berpengaruh pada perhitungan bobot baru, umumnya penggunaan learning rate yang menyesuaikan nilai gradien (adaptive learning rate) menunjukkan kinerja model yang lebih baik. Contoh algoritma adaptive learning rate Adagrad, Adadelta, Adam, AdaSecant, dan RMSprop. 

### Mencegah Overfitting

- Regularisasi dilakukan untuk mengurangi generalization error dengan mencegah model lebih 
kompleks.
    - Regularization L1 norm dan Regularization L2 norm (weight decay)
    
- Dropout adalah proses mencegah terjadinya overfitting dan juga mempercepat proses learning.
  
    <p align="center">
      <img src="contents/dropout.jpg" alt="dropout" width="640" style="vertical-align:middle">
    </p>

    ```
    tf.keras.layers.Dropout(rate)
    ```
- Early Stopping adalah iterasi pada saat training dihentikan jika `generalization error/loss validation` mulai naik.

- Augmentasi Data adalah menambah data training.

---
- [cat vs dog](https://colab.research.google.com/drive/1N3W4rkGrEUKcbdDKAeKGEIOGRgVPiOXF?usp=sharing)
- [human vs horse](https://colab.research.google.com/drive/1SxLHH0gJlhjg08Dc7apYDzo49qseKxT0?usp=sharing)
- [rps](https://colab.research.google.com/drive/1sh8FrF8U16PJGaw-rmc7mgQ9NJzmBEKw?usp=sharing)
