# Giriş 
Bu repo, **Bootcamp** kapsamında gerçekleştirdiğim görüntü işleme projesini içermektedir.  
Seçtiğim veri seti, **Architectural Heritage Elements Image 64 Dataset** olup Kaggle üzerinde toplam **11.534 görsel (.jpg) ve 10 sınıf** içermektedir. Kaggle açıklama kısmında görsel sayısı “10.235” olarak belirtilmiş olsa da, Summary kısmı ve yapılan kontroller sonucunda güncel veri seti büyüklüğü ~11.5k görsel olarak doğrulanmıştır.  

Amaç, derin öğrenme tabanlı bir **CNN modeli** ile görsellerin *altar, apse, column, dome* vb. mimari öğelerden hangisine ait olduğunu doğru sınıflandırmaktır.  
Veri ön işleme adımlarında görseller boyutlandırıldı, normalize edildi, **train/validation/test setlerine** ayrıldı ve veri dağılımları görselleştirildi.  
Daha sonra CNN modeli eğitildi, sonuçlar metrikler ve görsellerle değerlendirildi.  

---

## Kullanılan Araçlar
- Python  
- Google Colab  
- TensorFlow/Keras  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  

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

# Metrikler

Bu çalışmada modelin performansı, hem doğruluk (accuracy) hem de sınıf bazlı metrikler (precision, recall, F1-score) kullanılarak değerlendirilmiştir.  

- **Accuracy (Doğruluk):** Eğitim sürecinde en iyi epoch’ta model yaklaşık **%84 validation accuracy** değerine ulaşmıştır. Test setinde ise genel doğruluk oranı **%64** seviyesinde kalmıştır. Bu durum, modelin eğitim/validation verilerinde öğrendiklerini test verisine genellemede kısmen zorlandığını göstermektedir.

- **Makro F1:** ≈ **0.60**  
- **Ağırlıklı F1:** ≈ **0.63**  
- **Mikro F1:** ≈ **0.64**  

Bu sonuçlar, sınıflar arası dengesizlikleri dikkate aldığımızda modelin **orta seviyede genelleme başarısı** gösterdiğini ortaya koymaktadır.  

Özellikle bazı sınıflarda (*stained_glass* ve *gargoyle*) yüksek F1 skorları elde edilirken, diğer sınıflarda (*apse*, *flying_buttress*) skorlar daha düşük kalmıştır.  

- **Yüksek F1 skorları (ör. stained_glass, gargoyle):** Bu sınıflar daha belirgin görsel özelliklere sahip olduklarından ve daha fazla örnek içerdiğinden model tarafından daha doğru sınıflandırılmıştır.  
- **Düşük F1 skorları (ör. apse, flying_buttress):** Bu sınıflar hem daha az örnek içermekte hem de diğer mimari öğelerle yüksek görsel benzerlik göstermektedir. Bu nedenle modelin ayırt etmesi zorlaşmıştır.

- ## Sonuç ve Gelecek Çalışmalar

Bu çalışma kapsamında mimari öğelerin sınıflandırılmasına yönelik bir CNN tabanlı model geliştirilmiş ve değerlendirilmiştir. Hiperparametre optimizasyonu sürecinde yapılan Random Search denemelerinde yalnızca **accuracy** metriği dikkate alınmış, sınıf bazlı **precision–recall–F1** analizleri yapılmamıştır.  
 
Gelecek çalışmalarda, **hiperparametre optimizasyonunun** daha kapsamlı uygulanması ve  **veri artırma (data augmentation) yöntemlerinin** kullanılması projenin kalitesini ve genellenebilirliğini artıracaktır.

## Linkler  

- **Veri Seti:** [Architectural Heritage Elements Image 64 Dataset](https://www.kaggle.com/datasets/ikobzev/architectural-heritage-elements-image64-dataset)  
- **Kaggle Hesabım:** [Profilime Gitmek için Tıklayın](https://www.kaggle.com/nurglabut)  

