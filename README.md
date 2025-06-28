# 🏠 Melbourne Konut Fiyat Tahmini

Bu proje, Melbourne bölgesine ait konut verisi kullanılarak çeşitli regresyon modelleriyle ev fiyatlarının tahmin edilmesini amaçlamaktadır.

---

## 📋 Proje Özeti

- **Veri seti:** Melbourne konutlarına ait detaylı veri (`Melbourne_housing_FULL.csv`)
- Eksik değerlerin işlenmesi ve veri temizliği yapılmıştır.
- Kategorik değişkenler `One-Hot Encoding` ile sayısal forma dönüştürülmüştür.
- Bağımlı değişken: `Price` (ev fiyatı)
- Özellikler: Oda sayısı, ev tipi, konum, arazi büyüklüğü gibi değişkenler.
- Eğitim ve test verisi olarak %70-%30 bölünmüştür.
- Modeller:
  - Basit Doğrusal Regresyon (Linear Regression)
  - Lasso Regresyon (L1 ceza terimi ile)
  - Ridge Regresyon (L2 ceza terimi ile)
  - LassoCV (Çapraz doğrulamalı Lasso)
- Modellerin başarımı R^2 skoru ile değerlendirilmiştir.

---

## 🛠️ Kullanılan Kütüphaneler

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

---

## 🔍 Veri İşleme Adımları

1. Verinin yüklenmesi ve ilk inceleme (`head()`, `nunique()`, `shape`)
2. Analiz için kullanılacak sütunların seçilmesi
3. Eksik verilerin işlenmesi:
   - Bazı sütunlar 0 ile dolduruldu (`Propertycount`, `Distance`, `Bedroom2`, `Bathroom`, `Car`)
   - Bazı sütunlarda ortalama değer kullanıldı (`Landsize`, `BuildingArea`)
   - Kalan satırlar düşürüldü
4. Kategorik değişkenler `One-Hot Encoding` ile sayısallaştırıldı

---

## 📈 Modeller ve Performansları

- **Linear Regression:** Basit doğrusal regresyon modeli
- **Lasso Regression:** L1 cezası ile özellik seçimi ve düzenleme
- **Ridge Regression:** L2 cezası ile düzenleme
- **LassoCV:** 5 kat çapraz doğrulama ile en iyi alfa parametresi bulunan Lasso

Modellerin eğitim ve test skorları (R^2) hesaplanarak karşılaştırılmıştır.

---

## 🚀 Çalıştırma Talimatları

1. Gerekli paketleri yükleyin:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
