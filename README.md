# Kararlarin-Temsillerin-Birlestirilmesi
# 📌 Temsillerin ve Kararların Birleştirilmesi Projesi

Bu proje, **Türkçe metin verileri üzerinde farklı temsil yöntemleri ve ensemble (birleştirme) teknikleri kullanarak sınıflandırma performansını artırmayı** hedeflemektedir. Spam mesaj tahmini ve duygu analizi problemleri üzerinde çalışılmıştır.

## 📖 Proje Açıklaması

Metin verilerini temsil etmek için **farklı gömme modelleri (embeddings)** kullanılmış, ardından **Destek Vektör Makineleri (SVM), Rastgele Ormanlar (RF) ve Çok Katmanlı Algılayıcılar (MLP)** ile sınıflandırma gerçekleştirilmiştir.  

Bireysel model performansları değerlendirilmiş, ardından **temsillerin ve modellerin kararları birleştirilerek** sonuçların nasıl değiştiği analiz edilmiştir.

## 📊 Kullanılan Veri Kümeleri

1. **Spam Mesaj Tahmini:**
   - 5768 satırdan oluşan Türkçe mesaj veri kümesi.
   - Spam ve normal mesajlar dengeli bir dağılıma sahiptir.

2. **Duygu Analizi:**
   - 8491 satırdan oluşan müşteri yorumları veri kümesi.
   - Olumlu ve olumsuz yorumlar dengeli bir dağılıma sahiptir.

Veri kümeleri %80 eğitim ve %20 test seti olarak ayrılmıştır. Eksik veriler temizlenmiş ve sınıflar dengeli tutulmuştur.

## 🔍 Kullanılan Temsil Yöntemleri (Embeddings)

- `all-MiniLM-L12-v2`
- `multilingual-e5-large-instruct`
- `gte-large`
- `bert-base-turkish-uncased`
- `jina-embeddings-v3`

Bu yöntemler, metinleri **anlamsal vektörlere dönüştürerek** sınıflandırma algoritmalarına uygun hale getirmiştir.

## 🏆 Kullanılan Sınıflandırma Modelleri

- **Destek Vektör Makineleri (SVM)**
- **Rastgele Ormanlar (Random Forest - RF)**
- **Çok Katmanlı Algılayıcı (Multilayer Perceptron - MLP)**

**Ensemble yöntemiyle** aynı temsil yöntemine ait sonuçlar, aynı modele ait sonuçlar ve tüm sonuçlar birleştirilerek sınıflandırma performansı artırılmaya çalışılmıştır.

## 📊 Deneysel Sonuçlar

- **Spam Mesaj Tahmini:** 
  - En iyi temsil yöntemleri: `multilingual-e5-large-instruct`, `bert-base-turkish-uncased`, `jina-embeddings-v3`
  - Tüm sonuçlar birleştirildiğinde test veri seti için **accuracy: 0.97** olarak elde edilmiştir.

- **Duygu Analizi:**  
  - En iyi temsil yöntemleri: `multilingual-e5-large-instruct`, `jina-embeddings-v3`
  - Tüm sonuçlar birleştirildiğinde test veri seti için **accuracy: 0.93** olarak elde edilmiştir.

Detaylı sonuçlar için **[📄 Proje Raporu](rapor/Kolektif Öğrenme Rapor 2.pdf)** dosyasını inceleyebilirsiniz.
