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

├───Mbee <br>
├───Meow <br>
├───Moo <br>
├───Tweet <br>
└───Woof <br>

### 📌 Catatan Dataset
- Setiap folder vokal menyimpan **15 file `.wav`** hasil rekaman
- **10 file** untuk data training
- **5 file** untuk data testing

---

## ⚙️ Instalasi
Jalankan perintah berikut:
```bash
git clone https://github.com/alfin333/Speech-Classification-Vocals-CNN.git
cd Speech-Classification-Vocals-CNN
python -m venv venv
# Aktifkan virtual environment
source venv/bin/activate       # Untuk Linux/macOS
venv\Scripts\activate          # Untuk Windows
pip install -r requirements.txt

