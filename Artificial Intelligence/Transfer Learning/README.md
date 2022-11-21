# Transfer Learning

<p align="center">
    <img src="contents/transfer learning and fine tuning.png" alt="overview cnn" width="640" style="vertical-align:middle">
</p>

Transfer learning terdiri dari mengambil fitur yang dipelajari pada satu masalah, dan memanfaatkannya pada masalah baru yang serupa.

## Alur Kerja Transfer Learning

1. Buat instance model dasar dan muat beban yang telah dilatih sebelumnya ke dalamnya.
```python
base_model = tf.keras.applications.Xception(
    weights='imagenet',  # Load weights pre-trained on ImageNet.
    input_shape=(150, 150, 3),
    include_top=False)  # Do not include the ImageNet classifier at the top.
```
2. Freeze semua layer dalam model dasar dengan mengatur trainable = False.
```python
base_model.trainable = False
```
3. Buat model baru di atas output dari satu (atau beberapa) lapisan dari model dasar.
```python
inputs = tf.keras.Input(shape=(150, 150, 3))
# Kami memastikan bahwa model_dasar berjalan dalam mode inferensi di sini,
# dengan meneruskan `training=False`.
x = base_model(inputs, training=False)
# Konversi fitur bentuk `base_model.output_shape[1:]` ke vektor
x = tf.keras.layers.GlobalAveragePooling2D()(x)
# Dense classifier dengan 1 unit output (binary classification)
outputs = tf.keras.layers.Dense(1,activation='sigmoid')(x)
model = tf.keras.Model(inputs, outputs)
```
4. Latih model baru Anda pada set data baru Anda.
```python
model.compile(optimizer=....,
              loss=....,
              metrics=[....])
model.fit(new_dataset, epochs=20, validation_data=...)
```

# Fine Tuning
Fine-tuning terdiri dari 'unfreeze' seluruh model yang Anda peroleh di atas (atau sebagian darinya), dan melatihnya kembali pada data baru dengan tingkat pembelajaran yang sangat rendah

```python
# Unfreeze base model
base_model.trainable = True
```
