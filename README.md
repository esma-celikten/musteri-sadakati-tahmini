# 🛒 Müşteri Sadakatini Tahmin Etmek: E-Ticaret Veri Analitiği Projesi

> **İstanbul Teknik Üniversitesi — Büyük Veri ve İş Analitiği Uzmanlığı Sertifika Programı Final Projesi**

---

## 📌 Proje Hakkında

Bir e-ticaret platformunda müşterilerin **tekrar satın alma davranışını** makine öğrenmesi ile tahmin etmeyi amaçlayan ikili sınıflandırma projesidir.

> 💡 Tekrar müşteri kazanmak, yeni müşteri kazanmaktan **5 kat daha ucuzdur.**
> Doğru tahmin ile kişiselleştirilmiş kampanya yönetimi ve müşteri kaybının önlenmesi mümkün olur.

---

## 📂 Proje Yapısı

```
musteri-sadakati-tahmini/
├── Eticaret_analizi.ipynb          # Python kodu (EDA + Model)
├── eticaret_veri_seti.xlsx         # Sentetik veri seti (741 kayıt)
├── Müşteri Sadakatini Tahmini Sunumu.pptx  # Final sunumu
└── README.md
```

---

## 🗃️ Veri Seti

Python ile oluşturulmuş **sentetik** bir e-ticaret veri seti kullanılmıştır.

| Özellik | Detay |
|--------|-------|
| Başlangıç kayıt sayısı | 1.000 müşteri |
| Temizleme sonrası | 741 kayıt |
| Değişken sayısı | 12 |

### Değişkenler

| Değişken | Tür |
|---------|-----|
| Yaş, Cinsiyet, Şehir | Demografik |
| Kategori, Ödeme Yöntemi | Davranışsal |
| Üyelik Süresi, Önceki Satın Alma | Geçmiş |
| İndirim Oranı, Fiyat, İade Sayısı, Müşteri Skoru | Nümerik |
| **Tekrar Satın Alma (0/1)** | 🎯 Hedef Değişken |

---

## ⚙️ Kullanılan Teknolojiler

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat&logo=googlecolab&logoColor=white)

---

## 🤖 Modeller ve Sonuçlar

Dört farklı sınıflandırma algoritması karşılaştırılmıştır:

| Model | Doğruluk | F1 (Almaz) | F1 (Alır) |
|-------|----------|------------|-----------|
| Lojistik Regresyon | %79.19 | 0.81 | 0.76 |
| Karar Ağacı | %77.18 | 0.82 | 0.69 |
| **Random Forest** | **%87.25** ✅ | **0.90** | **0.83** |
| Gradient Boosting | %100* | 1.00 | 1.00 |

> *Gradient Boosting'in %100 doğruluğu sentetik verinin deterministik yapısından kaynaklanmaktadır. Gerçek veri ile sonuçlar farklılaşacaktır.

### 🏆 En İyi Model: Random Forest
- En yüksek ve **en dengeli** sonucu üretmiştir
- Gerçek dünya uygulaması için en uygun modeldir

---

## 🔍 Temel Bulgular

- **Üyelik süresi**, indirim oranı ve müşteri skoru tekrar satın almayı en çok etkileyen faktörlerdir
- **İade sayısı** tek negatif etkili değişken olarak öne çıkmaktadır
- Müşteri memnuniyet skoru arttıkça tekrar satın alma oranı belirgin şekilde yükselmektedir

---

## 💡 Öneriler

- Model gerçek platform verisiyle yeniden eğitilebilir
- Kampanyalar, tekrar satın alma ihtimali yüksek müşterilere yönlendirilebilir
- İade sayısı yüksek müşteriler için memnuniyet programı geliştirilebilir

---

## ⚠️ Kısıtlar

- Çalışma sentetik veri üzerinde gerçekleştirilmiştir
- Gerçek dünya verisinde model performansı farklılaşabilir
- Model gerçek dünya verisiyle yeniden eğitilebilecek konumdadır

---

## 👩‍💻 İletişim

**Esma Çelikten**
🔗 [github.com/esma-celikten](https://github.com/esma-celikten)

---

*Bu proje İTÜ Büyük Veri ve İş Analitiği Uzmanlığı Sertifika Programı 99. Dönem kapsamında geliştirilmiştir.*


