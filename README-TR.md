## ⚙️ Lindley Dağılımı ile CLM Süreç Yeterlilik Analizi  

## 📊 Üretim Süreçlerinde Asimetrik Dağılımlar İçin Yeni Bir Yaklaşım  


## 🎯 Proje Özeti

Bu proje, üretim süreçlerinde **asimetrik (non-normal)** dağılımları dikkate alarak, **süreç yeterliliğini daha doğru ölçmek** amacıyla geliştirilmiş bir istatistiksel analiz çalışmasıdır.  

Klasik süreç yeterlilik indeksleri (**Cp, Cpk**) genellikle **normal dağılım varsayımı** altında hesaplanır.  
Ancak gerçek üretim ortamlarında (otomotiv, savunma, medikal cihaz, kimya vb.) veriler çoğunlukla **asimetrik özellik gösterir**.  

Bu nedenle proje kapsamında, **Lindley Dağılımı** kullanılarak **CLM (Capability Life Measurement)** adı verilen yeni bir endeks önerilmiştir.  
Bu endeks, klasik PCI ölçütlerine kıyasla **daha doğru, esnek ve güvenilir** sonuçlar sunmaktadır.


## 💼 Uygulama Odaklı Bakış

Bu çalışma, farklı sektörlerdeki üretim ve kalite yönetimi süreçlerinde kullanılabilecek, ölçeklenebilir ve güvenilir bir süreç değerlendirme modeli geliştirmeyi amaçlamaktadır.

Proje; özellikle otomotiv, savunma, enerji ve imalat sektörlerinde kullanılan kalite kontrol analizlerine katkı sağlayacak şekilde tasarlanmıştır.
Gerçek üretim verileri üzerinde yapılan analizler, klasik yöntemlere göre daha düşük hata oranı ve daha yüksek model uyumu göstermiştir.

## 🔹 Gerçek Hayat Uygulaması

Bir otomotiv parçası üretim süreci üzerinde 60 örneklem değeriyle analiz yapılmıştır:  

| Parametre       |   eğer   |
|-----------------|----------|
| Alt Limit (LSL) | 1.4      |
| Üst Limit (USL) | 2.3      |
| Hedef Değer (T) | 1.75     |
| Ortalama (μ)    | 1.7375   |
| Varyans (σ²)    | 0.0169   |
| **CLM İndeksi** | **1.15** |

**Sonuç:**  
Süreç kontrol altında, varyans düşük ve ortalama hedefe çok yakındır.  
CLM > 1 olduğundan süreç **kabul edilebilir kalite düzeyinde**, ancak **iyileştirmeye açık** durumdadır.


## 🧠 Akademik ve Teknik Arka Plan

## 🔸 CLM İndeksi Nedir?
CLM (Capability Life Measurement) sürecin hem **kalitesini hem de ömür performansını** ölçen bir metriktir.  
Lindley dağılımı, klasik normal dağılımlara kıyasla **asimetrik ve daha esnek** bir yapı sunar.

1) Lindley olasılık yoğunluk fonksiyonu:
<img width="424" height="73" alt="image" src="https://github.com/user-attachments/assets/3a125105-a0a7-4f3f-b9a7-2b2dacb18552" />


2) Önerilen CLM formülü:
  <img width="532" height="68" alt="image" src="https://github.com/user-attachments/assets/88cf8c15-d95e-49f8-9f14-729ee92682d8" />

Burada:
- \( M \): Medyan  
- \( L \): Alt spesifikasyon limiti  
- \( δ = \frac{M - μ}{σ} \)

Bu yaklaşım, sürecin asimetrisini hesaba katarak **gerçek kalite performansını** daha doğru biçimde yansıtır.


## 💻 Kullanılan Teknolojiler
| Araç / Kütüphane | Açıklama |
|------------------|-----------|
| **R (v4.3)** | İstatistiksel hesaplama ve simülasyon |
| **VGAM** | Lindley dağılımı modelleme |
| **lamW** | Lambert W fonksiyonu ile hesaplama |
| **ggplot2** | Görselleştirme |
| **Monte Carlo Simulation** | Parametre tahmini ve hata analizi |
| **Bootstrap** | Güven aralığı oluşturma |


## 📈 Simülasyon Sonuçları

| θ (Theta) | Bias | MSE | ABB | MRE |    Performans     |
|-----------|------|-----|-----|-----|-------------------|
| 0.2       | ↓    | ↓   | ↓   | ↓   | Tutarlı model     |
| 0.5       | ↓↓   | ↓↓  | ↓   | ~0  | En iyi performans |
| 0.7       | ↑↑   | ↑↑  | ↑↑  | ↑↑  | Tutarsız model    |

🔹 Özet:

- Küçük ve orta θ değerlerinde (0.2–0.5) model **yüksek doğruluk** sağlar.  
- Yüksek θ değerlerinde (0.7) sapma ve hata artar → model kararlılığı azalır.  
- CLM, klasik Cp–Cpk endekslerine göre **asimetrik süreçlerde daha güvenilir** sonuçlar verir.

## 📊 Görselleştirmeler

Analizlerde şu grafikler kullanılmıştır:  
- **Bias, MSE, ABB, MRE** değişim grafikleri  
- **Süreç dağılımı ve spesifikasyon sınırları** (histogram)  
- **CLM vs Cp/Cpk karşılaştırması**


## 🧩 Öne Çıkan Kazanımlar

✅ Asimetrik veriler için klasik PCI’lara göre daha doğru analiz  
✅ Monte Carlo simülasyonu ile parametrik doğrulama  
✅ Gerçek üretim verisinde uygulama ve görselleştirme  
✅ R, istatistik ve veri bilimi araçlarının entegre kullanımı  


## 👤 Yazar

**Yunus Ahmet Dokazoğlu**  
🎓 Selçuk Üniversitesi – İstatistik Bölümü  
📍 Türkiye  

🔗 [GitHub Profilim](https://github.com/AhmetDokazoglu)  
🔗 [LinkedIn Profilim](https://www.linkedin.com/in/ahmet-dokazo%C4%9Flu-9660b2346/)


## 📎 Ek Dökümanlar  
📄 [Proje Raporunun Word Versiyonu (İndir)](https://github.com/AhmetDokazoglu/Lindley-Dagilimi-ile-CLM-Surec-Yeterlilik-Analizi/raw/refs/heads/main/Lindley%20Dagilimi%20ile%20CLM%20Surec%20Yeterlilik%20Analizi.docx)   


## 💬 Kısa Değerlendirme
> Bu proje, klasik süreç yeterlilik analizlerinin ötesine geçerek, **asimetrik veri yapıları altında daha gerçekçi kalite ölçümü** sağlar.  
> Hem **akademik araştırmalarda** hem de **üretim, kalite ve veri analitiği projelerinde** kullanılabilecek güçlü bir istatistiksel altyapı sunmaktadır.
