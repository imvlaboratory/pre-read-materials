<h1 align="center"> Artificial Neural Network (ANN) / Dense Neural Network </h1>

<p align="center">
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white" style="vertical-align:middle">
</p>

## Definisi Artificial Neural Network

Salah satu metode mesin pembelajaran yang terinspirasi oleh cara kerja jaringan saraf biologis di otak manusia. Konsep ANN bermula pada artikel dari Waffen McCulloch dan Walter Pitts pada tahun 1943 yaitu mencoba untuk memformulasikan model matematis sel-sel otak manusia.

<p align="center">
    <img src="contents/Definisi ANN.png" alt="ANN/DNN" width="1080" style="vertical-align:middle">
</p>

## Arsitektur Artificial Neural Network (ANN)

<p align="center">
    <img src="contents/ANN.gif" alt="ANN/DNN" width="510" style="vertical-align:left">
    <img src="contents/ANN weight.gif" width="480" style="vertical-align:left">
</p>

<br>Bagian-bagian Artificial Neural Network (ANN) / Dense Neural Network sebagai berikut:<br>

### 1. Input Layer

Ukuran input sesuai dengan jumlah fitur pada data input.

```python
tf.keras.Input(shape=[height, width, color_channels])
```
```python
tf.keras.layers.InputLayer(input_shape=(height, width, color_channels))
```
```python
tf.keras.layers.Conv2D(input_shape=(height, width, color_channels))
```
```python
tf.keras.layers.Flatten(input_shape=(height, width, color_channels))
```
```python
tf.keras.layers.Dense(input_shape=(height, width, color_channels))
```
- input_shape/shape → dimensi ruang input

### 2. Hidden Layer

Jumlah hidden layer sebaiknya disesuaikan dengan kompleksitas permasalahan.
- Semakin banyak jumlah layer memerlukan komputasi waktu yang lebih lama
- Semakin banyak jumlah node (neuron) memungkinkan mempelajari pola yang lebih rumit
- Untuk mencegah overfitting sebaiknya menambah jumlah node (neuron) secara bertahap

```python
tf.keras.layers.Dense(units, activation=None)
```
- units → dimensi ruang output
- activation → fungsi aktivasi untuk digunakan → relu
  
### 3. Output Layer

Jumlah neuron sesuai dengan permasalahan.
- Untuk `klasifikasi binary dan regresi` menggunakan `satu neuron`.
- Untuk `klasifikasi multiclass atau categorical` menggunakan `jumlah neuron sesuai jumlah kelas`.

```python
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

----

Visualisasi: [ANN](https://playground.tensorflow.org/)

Google Colabs: 
- [Fashion-MNIST](https://colab.research.google.com/drive/1ZwvOVEfuFmZ7tkQq4r-1kla9xpofMF5_?usp=sharing)
- [Handwritten Digits-MNIST](https://colab.research.google.com/drive/1U1xKoEehgWVvq5cEuf1A4LcurWSt1WFA?usp=sharing)
