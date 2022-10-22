<h1 align="center"> Tools </h1>

# Google Colaboratory

<p align="center">
    <img src="contents/logo colab.png" width="360" style="vertical-align:middle">
</p>

Colab atau "Colaboratory", digunakan untuk menulis dan mengeksekusi Python melalui browser dengan keuntungan sebagai berikut:
- Tidak perlu konfigurasi
- Akses ke GPU secara gratis
- Mudah berkolaborasi dengan orang banyak (easy sharing)

Google Colaboratory dapat diakses pada https://colab.research.google.com

## Bagian Esensial pada Colab

<p align="center">
    <img src="contents/fitur colab 1.png" width="700" style="vertical-align:middle">
</p>

<p align="center">
    <img src="contents/fitur colab 2.png" width="720" style="vertical-align:middle">
</p>

## Workflow

### 1. Buka Google Colab pada: https://colab.research.google.com
### 2. Buat file

<p align="center">
    <img src="contents/tampilan awal colab.png" width="800" style="vertical-align:middle">
</p>

### 3. Pilih jenis runtime

<p align="center">
    <img src="contents/tipe runtime 1.png" width="700" style="vertical-align:middle">
</p>

<p align="center">
    <img src="contents/tipe runtime 2.png" width="700" style="vertical-align:middle">
</p>

    GPU dipilih karena dengan menggunakan GPU proses komputasi akan semakin cepat

### 4. Connect runtime
    Klik connect/reconnect atau "save" saat memilih jenis runtime
### 5. Tulis Code
    Tuliskan code atau text pada cell yang tersedia atau dengan membuat cell baru
### 6. Eksekusi code
    Klik tombol run yang berada pada samping kiri setiap cell code
   
<p align="center">
    <img src="contents/contoh output.png" width="700" style="vertical-align:middle">
</p>

    Gambar di atas menampilkan contoh output jika code terdapat error, tidak ada perintah output, dan terdapat perintah output

### 7. Save
    Colab akan melakukan saving secara otomatis melalui fitur auto-saving pada Google Drive setiap ada perubahan pada code

<p align="center">
    <img src="contents/saving.png" width="800" style="vertical-align:middle">
</p>

## Additional Resources

Video: [Introduction to Colab](https://www.youtube.com/watch?v=inN8seMm7UI&ab_channel=TensorFlow)

Written Tutorial: 
[Basic Feature Overview](https://colab.research.google.com/notebooks/basic_features_overview.ipynb)

# Jupyter Notebook

<p align="center">
    <img src="contents/logo jupyter.svg" width="360" style="vertical-align:middle">
</p>

[Jupyter Notebook](https://algorit.ma/blog/cara-menggunakan-jupyter-notebook-2022/) merupakan singkatan dari tiga bahasa pemrograman, yakni Julia (Ju), Python (Py), dan R. Jupyter Notebook adalah sebuah aplikasi web gratis yang paling banyak dipakai oleh data scientist. Aplikasi ini dipakai untuk membuat dan membagikan dokumen yang memiliki kode, hasil hitungan, visualisasi, dan teks. Ketiga bahasa pemrograman pada Jupyter Notebook sendiri adalah sesuatu yang penting bagi seorang data scientist.

Sederhananya, Jupyter Notebook berfungsi membantu data scientist dalam membuat narasi komputasi. Narasi komputasi sendiri menjelaskan makna dari data di dalamnya dan memberikan insight (wawasan) tentang data tersebut. 

Kemudahan aspek menulis dan berbagi teks maupun kode dalam aplikasi ini juga membuatnya cocok digunakan untuk kolaborasi. Jupyter Notebook membuat kerja sama antara insinyur dan data scientist lebih mudah dan lancar. Aplikasi ini juga memudahkan data scientist melakukan kolaborasi dengan sesama data scientist, data researchers, maupun data engineers lainnya.

## Bagian Esensial pada Jupyter Notebook

<p align="center">
    <img src="contents/fitur jupyter.png" style="vertical-align:middle">
</p>

## Instalasi

### 1. Install dengan command `pip`
Gunakan command `pip install jupyterlab` pada cmd

### 2. Jalankan dengan command:
Gunakan command `jupyter-lab` pada cmd

Tampilan setelah berhasil menjalankan:

<p align="center">
    <img src="contents/cmd jupyter.png" width="700" style="vertical-align:middle">
</p>

## Workflow
### 1. Jalankan Jupyter Notebook 
    Gunakan command `jupyter-lab` pada cmd
### 2. Akses local host
    Jupyter Notebook dapat di akses pada `http://localhost:8888/`
### 3. Tulis code
    Tuliskan code atau text pada cell yang tersedia atau dengan membuat cell baru
### 4. Eksekusi Code
    Klik tombol run yang berada pada samping kiri setiap cell code
<p align="center">
    <img src="contents/output jupyter.png" width="700" style="vertical-align:middle">
</p>

    Gambar di atas menampilkan contoh output jika code terdapat error, tidak ada perintah output, dan terdapat perintah output
### 5. Save
    Lakukan saving dengan menekan tombol save
### 6. Close CMD
    Close CMD untuk mematikan akses ke Jupyter Notebook

## Additional Resources

Documentation: [Jupyter Project Documentation](https://docs.jupyter.org/en/latest/)
