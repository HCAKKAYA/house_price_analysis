# 🏠 House Prices: Advanced Regression Techniques

Bu proje, Kaggle üzerindeki [House Prices](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) yarışması kapsamında gerçekleştirilmiştir. Amaç, Ames Housing veri setinden yararlanarak ev satış fiyatlarını tahmin etmektir.

## 📁 Veri Seti

- `train.csv`: Eğitim verisi (etiketli, `SalePrice` mevcut)
- `test.csv`: Tahmin yapılacak test verisi
- `sample_submission.csv`: Kaggle'a gönderilecek tahmin formatı

## 🔧 Uygulanan Adımlar

### 1. 📊 Veri Keşfi (EDA)
- `head()`, `info()`, `describe()` gibi fonksiyonlarla temel veri analizi
- Eksik verilerin tespiti (`isnull().sum()`)

### 2. 🧼 Veri Ön İşleme
- Eksik veriler `median` veya `mode` ile dolduruldu
- Gereksiz sütunlar (`PoolQC`, `MiscFeature`, `Fence`, vb.) çıkarıldı
- One-hot encoding (kategori değişkenler için)

### 3. 🧠 Modelleme
- `LinearRegression` modeli kullanıldı
- `SalePrice` değişkenine log dönüşümü (`np.log1p()`) uygulandı
- Eğitim ve doğrulama setlerine ayırma (`train_test_split`)

### 4. ✅ Değerlendirme
- Modelin doğruluğu RMSE metriği ile değerlendirildi
- En iyi RMSE değeri: **~25,000**

### 5. 📤 Tahmin ve Gönderim
- Test verisine model uygulandı
- Tahminler `np.expm1()` ile orijinal formuna döndürüldü
- Sonuçlar `submission.csv` olarak kaydedildi

## ⚙️ Kullanılan Kütüphaneler

- pandas
- numpy
- matplotlib / seaborn (EDA için)
- scikit-learn

## 👤 Yazar

**Hüseyin Akkaya**

Bu proje, veri bilimi alanındaki pratik becerilerimi geliştirmek ve portföyüme katkıda bulunmak amacıyla gerçekleştirilmiştir.
