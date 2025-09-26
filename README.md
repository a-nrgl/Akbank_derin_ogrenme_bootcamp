# Akbank Derin Öğrenmeye Giriş Bootcamp 
Bu repo, **Bootcamp** kapsamında gerçekleştirdiğim görüntü işleme projesini içermektedir.  
Seçtiğim veri seti, **Architectural Heritage Elements Image 64 Dataset** olup Kaggle üzerinde toplam **11.534 görsel (.jpg) ve 10 sınıf** içermektedir. Kaggle açıklama kısmında görsel sayısı “10.235” olarak belirtilmiş olsa da, Summary kısmı ve yapılan kontroller sonucunda güncel veri seti büyüklüğü ~11.5k görsel olarak doğrulanmıştır.  

Amaç, derin öğrenme tabanlı bir **CNN modeli** ile görsellerin *altar, apse, column, dome* vb. mimari öğelerden hangisine ait olduğunu doğru sınıflandırmaktır.  

---

## Kullanılan Araçlar
- Python  
- Google Colab  
- TensorFlow/Keras  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  
- PIL  
- os/glob/shutil (dosya işlemleri)  
- Grad-CAM (tf.GradientTape)  

---

## Kullanılan Algoritmalar ve Yöntemler
1. **Convolutional Neural Network (CNN)**  
2. **Aktivasyon Fonksiyonları** (ReLU, Softmax)  
3. **Optimizasyon Algoritması** (Adam Optimizer, learning rate=0.001)  
4. **Kayıp Fonksiyonu** (Categorical Cross-Entropy)  
5. **Regularization Teknikleri** (Dropout, L2 Regularization)  
6. **Callback’ler** (EarlyStopping, ModelCheckpoint)  
7. **Model Değerlendirme Algoritmaları** (Confusion Matrix, Classification Report, Grad-CAM)  

---

## Veri Ön İşleme ve Eğitim Süreci
Veri ön işleme adımlarında görseller boyutlandırıldı, normalize edildi, **train/validation/test setlerine** ayrıldı ve veri dağılımları görselleştirildi.  
Daha sonra CNN modeli eğitildi, sonuçlar metrikler ve görsellerle değerlendirildi.  
