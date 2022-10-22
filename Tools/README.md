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

[Jupyter](https://algorit.ma/blog/cara-menggunakan-jupyter-notebook-2022/) merupakan singkatan dari tiga bahasa pemrograman, yakni Julia (Ju), Python (Py), dan R. Jupyter Notebook adalah sebuah aplikasi web gratis yang paling banyak dipakai oleh data scientist. Aplikasi ini dipakai untuk membuat dan membagikan dokumen yang memiliki kode, hasil hitungan, visualisasi, dan teks. Ketiga bahasa pemrograman pada Jupyter Notebook sendiri adalah sesuatu yang penting bagi seorang data scientist.

Sederhananya, Jupyter Notebook berfungsi membantu data scientist dalam membuat narasi komputasi. Narasi komputasi sendiri menjelaskan makna dari data di dalamnya dan memberikan insight (wawasan) tentang data tersebut. 

JupyterLab adalah antarmuka pengguna generasi berikutnya termasuk notebook. Ini memiliki struktur modular, di mana Anda dapat membuka beberapa buku catatan atau file (misalnya HTML, Text, Markdowns, dll) sebagai tab di jendela yang sama. Ini menawarkan lebih banyak pengalaman seperti IDE. JupyterLab menawarkan lebih banyak fitur dan antarmuka yang disempurnakan daripada Jupyter Notebook, yang dapat diperluas melalui ekstensi: [Ekstensi JupyterLab (GitHub)](https://github.com/search?q=topic%3Ajupyterlab-extension&type=Repositories).

## Bagian Esensial pada Jupyter Notebook

<p align="center">
    <img src="contents/fitur jupyter.png" style="vertical-align:middle">
</p>

## Instalasi

Instalasi pada `jupyter-lab` dapat dilakukan dengan command pip dan conda untk Anaconda. Untuk Anaconda, Jupyterlab dan Jupyter Notebook sudah termasuk didalamnya. Untuk Instalasi Anaconda dapat dilihat [disini]()

### 1. Install dengan command `pip` atau `conda`
Gunakan command `pip install jupyterlab` untuk install jupyterlab dan `pip install jupyter` untuk install jupyter notebook pada cmd

### 2. Jalankan dengan command:
Gunakan command `jupyter-lab` pada cmd untuk jupyterlab dan `jupyter-notebook` untuk jupyter notebook

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
