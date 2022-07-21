BANNER STUDY GROUP
----
<h1 align="center"> Artificial Neural Network (ANN) / Dense Neural Network </h1>

<p align="center">
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white" style="vertical-align:middle">
</p>

<p align="center">
    <img src="contents/ANN.png" alt="ANN/DNN" width="480" style="vertical-align:middle">
</p>

<br>Bagian-bagian Artificial Neural Network (ANN) / Dense Neural Network sebagai berikut:<br>
### Input Layer

  ```
    tf.keras.Input(shape=[height, width, color_channels])
  ```
  ```
    tf.keras.layers.InputLayer(input_shape=(height, width, color_channels))
  ```
  ```
    tf.keras.layers.Dense\Conv2D\Flatten(units, input_shape=(height, width, color_channels))
  ```
  - input_shape/shape → dimensi ruang input
  - units → dimensi ruang output

### Hidden Layer
  ```
    tf.keras.layers.Dense(units, activation=None)
  ```
  - units → dimensi ruang output
  - activation → fungsi aktivasi untuk digunakan → relu
  
  Dropout → proses mencegah terjadinya overfitting dan juga mempercepat proses learning.
  
  <p align="center">
    <img src="contents/dropout.jpg" alt="dropout" width="640" style="vertical-align:middle">
  </p>
  
  ```
  tf.keras.layers.Dropout(rate)
  ```
  
  
### Output Layer

  ```
    tf.keras.layers.Dense(units, activation=None)
  ```
  - units → dimensi ruang output

----
Google Colabs: https://colab.research.google.com/drive/1ZwvOVEfuFmZ7tkQq4r-1kla9xpofMF5_#scrollTo=NYt5x9HdA_Fi
