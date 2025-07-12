# Speech-Classification-Vocals-CNN
project:
  title: "Speech Classification of Vowel Sounds using CNN"
  description: >
    Klasifikasi suara vokal hewan (simulasi vokal A, I, U, E, O) menggunakan
    Convolutional Neural Network (CNN). Dataset diperoleh melalui rekaman suara
    langsung dari mikrofon, kemudian diproses dengan Voice Activity Detection (VAD)
    dan diekstraksi fitur MFCC-nya. Model dilatih untuk mengenali 5 jenis vokal:
    Moo, Meow, Woof, Mbee, dan Tweet.
features:
  - Rekaman suara langsung dari microphone
  - Preprocessing audio: VAD, padding/cropping, normalisasi amplitudo
  - Ekstraksi fitur MFCC (40 koefisien)
  - CNN sederhana untuk klasifikasi suara
  - Evaluasi model (akurasi, classification report)
  - Real-time prediksi vokal dari rekaman pengguna
dataset:
  structure: |
    data/
    ├── Moo/
    │   ├── Moo_0.wav
    │   ├── Moo_1.wav
    │   └── ...
    ├── Meow/
    ├── Woof/
    ├── Mbee/
    └── Tweet/
  notes:
    - Setiap folder vokal menyimpan 15 file .wav hasil rekaman
    - 10 file untuk data training
    - 5 file untuk data testing
installation:
  steps:
    - git clone https://github.com/alfin333/Speech-Classification-Vocals-CNN.git
    - cd Speech-Classification-Vocals-CNN
    - python -m venv venv
    - source venv/bin/activate  # di Windows: venv\Scripts\activate
    - pip install -r requirements.txt
usage:
  steps:
    - Buka dan jalankan vocal.ipynb di Jupyter Notebook atau Google Colab
    - Rekam 15 sampel suara untuk setiap vokal (otomatis tersimpan di folder data/)
    - Jalankan training model (100 epoch), hasil disimpan ke vowel_cnn.pth
    - Jalankan prediksi suara secara real-time
model:
  architecture:
    - 2x Conv2D + ReLU + MaxPool
    - 1x Fully Connected Layer (output: 5 kelas)
  input_shape: (1, 40, T)  # MFCC tensor
evaluation:
  train_accuracy: "100%"
  test_accuracy: "92%"
  classification_report: |
    precision    recall  f1-score   support
     Moo       1.00      1.00      1.00         5
    Meow       1.00      0.60      0.75         5
    Woof       1.00      1.00      1.00         5
    Mbee       1.00      1.00      1.00         5
   Tweet       0.71      1.00      0.83         5

    accuracy                           0.92        25
output_example: |
  Ucapkan vokal (A/I/U/E/O)...
  Moo: 0.00%
  Meow: 0.00%
  Woof: 0.00%
  Mbee: 0.01%
  Tweet: 99.99%

  Vokal Yang Diprediksi: Tweet
notes:
  - Dataset masih kecil (75 data audio total), sehingga model bisa overfitting
  - Disarankan menambah variasi suara dan jumlah data untuk meningkatkan generalisasi
  - Cocok sebagai proyek awal dalam pembelajaran Deep Learning berbasis audio
license: >
  Proyek ini dibuat untuk keperluan edukasi dan tidak digunakan untuk tujuan komersial.
