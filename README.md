# 🔐 XSS (Cross-Site Scripting) Güvenlik Açığı - Yol Haritası

## 📌 1. XSS Nedir?

Cross-Site Scripting (XSS), web uygulamalarında kullanıcıdan alınan verilerin yeterince filtrelenmeden sayfaya yansıtılması sonucu, saldırganın zararlı JavaScript kodu çalıştırabilmesine olanak tanıyan bir güvenlik açığıdır.

---

## 🔥 2. XSS Türleri

### 2.1 Reflected XSS

* Kullanıcıdan gelen veri anlık olarak sayfada gösterilir.
* Genellikle URL parametreleri üzerinden gerçekleşir.

### 2.2 Stored XSS

* Zararlı kod veritabanına kaydedilir.
* Diğer kullanıcılar sayfayı açtığında otomatik çalışır.

### 2.3 DOM-Based XSS

* Sunucuya gitmeden, tamamen tarayıcı tarafında oluşur.
* JavaScript manipülasyonu ile gerçekleşir.

---

## ⚙️ 3. XSS Nasıl Çalışır?

1. Kullanıcı input alanına veri girer
2. Sistem bu veriyi filtrelemeden sayfaya basar
3. Tarayıcı bunu normal JavaScript olarak çalıştırır
4. Saldırgan:

   * Cookie çalabilir
   * Oturum ele geçirebilir
   * Kullanıcıyı başka sayfaya yönlendirebilir

---

## 🛠️ 4. Öğrenme Yol Haritası

### 🔹 Aşama 1: Temel Bilgiler

* HTML (formlar, inputlar)
* JavaScript (özellikle DOM)
* HTTP & Web çalışma mantığı

### 🔹 Aşama 2: Basit Testler

* Input alanlarında basit script denemeleri
* Alert tabanlı testler

### 🔹 Aşama 3: Filtre Bypass Mantığı

* Encoding teknikleri (HTML, URL)
* Farklı event kullanımları (onerror, onclick)

### 🔹 Aşama 4: Gerçek Senaryolar

* Arama kutuları
* Yorum sistemleri
* Profil sayfaları

---

## 🧪 5. Örnek Senaryo

Bir web sitesinde arama kutusu düşünelim:

Kullanıcı şu girdiyi yazıyor:

```
<script>alert('XSS')</script>
```

Eğer site bu girdiyi filtrelemeden gösterirse:

* Tarayıcı bunu çalıştırır
* XSS açığı oluşur

---

## 🛡️ 6. Korunma Yöntemleri

### ✅ Input Validation

* Kullanıcı verisini kontrol et

### ✅ Output Encoding

* HTML özel karakterlerini encode et

### ✅ Content Security Policy (CSP)

* Zararlı scriptlerin çalışmasını engelle

### ✅ Güvenli Framework Kullanımı

* React, Angular gibi frameworkler otomatik koruma sağlar

---

## 🎯 7. Sonuç

XSS, en yaygın web güvenlik açıklarından biridir. Temel web bilgisi olan herkes tarafından öğrenilebilir ve doğru şekilde analiz edildiğinde ciddi güvenlik açıkları tespit edilebilir.

Bu nedenle hem saldırı mantığını hem de korunma yöntemlerini öğrenmek kritik öneme sahiptir.

---

## 📚 8. Kaynaklar

* OWASP XSS Guide
* PortSwigger Web Security Academy
* MDN Web Docs

---
