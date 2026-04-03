# skin-canser
# 🩺 Skin Cancer Classification using CNN (PyTorch)

Ushbu loyiha Kaggle'dagi "Skin Cancer" datasetidan foydalangan holda teri saratoni turlarini klassifikatsiya qilish uchun Convolutional Neural Network (CNN) modelini qurish va o'qitishga bag'ishlangan.

## 📁 Dataset Haqida
Dataset Kagglehub orqali yuklab olingan va quyidagi klasslarni o'z ichiga oladi:
* `mel`: Melanoma
* `nv`: Melanocytic nevi
* `bcc`: Basal cell carcinoma
* `akiec`: Actinic keratoses
* `bkl`: Benign keratosis-like lesions
* `df`: Dermatofibroma
* `vasc`: Vascular lesions

## 🛠 Texnologiyalar
* **Python 3.12+**
* **PyTorch** & **Torchvision**
* **Kagglehub** (Dataset yuklash uchun)
* **Matplotlib** (Vizualizatsiya uchun)

## 🚀 Loyihani Ishga Tushirish

### 1. Kutubxonalarni o'rnatish
```python
pip install torch torchvision kagglehub matplotlib pillow
2. Model ArxitekturasiModel 3 ta konvolyutsion qatlamdan iborat bo'lib, har bir qatlamdan keyin ReLU aktivatsiya funksiyasi va MaxPool2d qo'llanilgan. Oxirida esa 2 ta to'liq bog'langan (Fully Connected) qatlam va Dropout (0.5) mavjud.3. Modelni O'qitish (Training)O'qitish jarayoni GPU (CUDA) yordamida amalga oshirildi.Loss Function: CrossEntropyLossOptimizer: Adam (Learning Rate = 0.001)Batch Size: 32Epochs: 5Python# Modelni o'qitish kodi
for epoch in range(epochs):
    model.train()
    # ... training loop logic
📊 NatijalarModel o'qitilgandan so'ng, test to'plamidagi aniqlik (Accuracy) tekshirildi.Ko'rsatkichQiymatTrain Loss~0.45 (taxminan)Test Accuracy85% +🖼 Bashorat Qilish (Prediction)Tayyor modeldan foydalanib, yangi rasmlarni quyidagicha bashorat qilish mumkin:Pythonpredict_image("path/to/image.jpg")
💾 Modelni SaqlashO'qitilgan model vaznlari keyinchalik ishlatish uchun saqlandi:Pythontorch.save(model.state_dict(), "skin_cancer_model.pth")
Muallif: [Sizning Ismingiz]Sana: 2026-yil, Aprel
