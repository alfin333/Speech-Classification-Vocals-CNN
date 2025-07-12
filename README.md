# Speech-Classification-Vocals-CNN
# 🎤 Speech Classification of Vowel Sounds using CNN

## 📌 Deskripsi
Klasifikasi suara vokal hewan menggunakan **Convolutional Neural Network (CNN)**.  
Dataset diperoleh melalui rekaman suara langsung dari mikrofon, kemudian diproses dengan **Voice Activity Detection (VAD)** dan diekstraksi fitur **MFCC**-nya.  
Model dilatih untuk mengenali **5 jenis vokal**:
- Moo
- Meow
- Woof
- Mbee
- Tweet

---

## ✨ Fitur
- Rekaman suara langsung dari microphone
- Preprocessing audio: VAD, padding/cropping, normalisasi amplitudo
- Ekstraksi fitur MFCC (40 koefisien)
- CNN sederhana untuk klasifikasi suara
- Evaluasi model (akurasi, classification report)
- Real-time prediksi vokal dari rekaman pengguna

---

## 📁 Struktur Dataset
├───Mbee
├───Meow
├───Moo
├───Tweet
└───Woof
