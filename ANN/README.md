# Artificial Neural Network (ANN) / Dense Neural Network

<p align="center">
    <img src="contents/ANN.png" alt="ANN/DNN" width="480" style="vertical-align:middle">
</p>

Bagian-bagian Artificial Neural Network (ANN) / Dense Neural Network sebagai berikut:
## Input Layer
  ```
    tf.keras.layers.Dense(units, input_shape=....)
  ```
  - input_shape → dimensi ruang input
  - units → dimensi ruang output

## Hidden Layer
  ```
    tf.keras.layers.Dense(units, activation=None)
  ```
  - units → dimensi ruang output
  - activation → fungsi aktivasi untuk digunakan → relu
  
## Output Layer

  ```
    tf.keras.layers.Dense(units, activation=None)
  ```
  - units → dimensi ruang output
