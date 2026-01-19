# 🎬 Sinema ve İzleyici Segmentasyonu (YouTube Yorum Analizi)

## 🔍 Araştırma Soruları

Bu proje aşağıdaki üç temel soruya yanıt aramaktadır:

1. **Filmimizi kimler izliyor ve yorum yapıyor?**
   (Gençler mi, sinefiller mi, yoksa sadece vakit geçirmek isteyen genel izleyiciler mi?)
2. **Pazarlama kampanyasında hangi öge öne çıkarılmalı?**
   (Senaryonun derinliği mi, yoksa görsel efektlerin kalitesi mi?)
3. **Sadık müşteri kitlesi (fanlar) kimdir ve ortak özellikleri nelerdir?**

---

## 📌 Proje Özeti

Bu proje, YouTube platformundaki film yorumlarını kullanarak **izleyici profilleri** ve **duygu eğilimlerini** analiz etmeyi amaçlamaktadır.
Amaç, bir filmin kimler tarafından, hangi duygusal ve tematik gerekçelerle beğenildiğini veya eleştirildiğini ortaya koymaktır.

Yapay zekâ destekli metin analizi ile yorumlar;

* **Pozitif / Negatif / Nötr duygu sınıflarına**
* **Sinefil, Fan Kitlesi, Görsel/Aksiyon Sever, Genel İzleyici** segmentlerine
  ayrıştırılmıştır.

---

## 🧩 1. Yöntem ve Veri Süreci

| Aşama                                                 | Açıklama                                                                                                                                                |
| ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Aşama 1: Veri Toplama**                             | YouTube API aracılığıyla film videolarındaki kullanıcı yorumları çekilmiştir. Her yorum için tarih, beğeni sayısı, dil ve yazar bilgisi kaydedilmiştir. |
| **Aşama 2: Duygu ve Segment Analizi**                 | Yorumlar otomatik olarak duygu (pozitif / negatif / nötr) ve izleyici segmentine göre sınıflandırılmıştır.                                              |
| **Aşama 3: Kampanya Kişiselleştirme (Model Önerisi)** | Her segment için özgün iletişim dili ve duygusal ton önerileri geliştirilmiştir.                                                                        |
| **Aşama 4: Geri Bildirim Döngüsü**                    | Gelecekte sistem, yeni yorumlar geldikçe kendini güncelleyecek biçimde genişletilebilir.                                                                |

---

## 📊 2. Bulgular ve Görseller

### 🎞️ Genel Duygu Dağılımı

Toplam **150.000 YouTube yorumu** analiz edilmiştir.

| Duygu              | Yorum Sayısı | Oran  |
| ------------------ | ------------ | ----- |
| Olumlu (Beğeni)    | 44.187       | %29.5 |
| Olumsuz (Eleştiri) | 18.196       | %12.1 |
| Nötr / Kararsız    | 87.617       | %58.4 |

📈 **Grafik 1: Genel Duygu Dağılımı**

<img width="571" height="387" alt="Ekran_görüntüsü_2026-01-19_011222-removebg-preview" src="https://github.com/user-attachments/assets/90a8b9d0-f80d-460b-8a40-904d05b152a4" />

*Yorumların büyük kısmı nötr tondadır; bu durum, sinema izleyicisinin yalnızca duygusal değil, analitik bir değerlendirme yaptığına işaret etmektedir.*

---

### 🧠 İzleyici Segmentlerinin Davranış Profili

📈 **Grafik 2: İzleyici Segmentlerinin Davranış Profili (Radar Analizi)**
<img width="533" height="406" alt="image" src="https://github.com/user-attachments/assets/928abfbe-cd55-40d0-b831-63dc9d3f5013" />


| Segment            | Duygu Skoru | Özellik               |
| ------------------ | ----------- | --------------------- |
| **Sinefiller**     | +0.1        | Analitik, eleştirel   |
| **Aksiyon Sever**  | +0.6        | Görsel kalite odaklı  |
| **Fan Kitlesi**    | +0.8        | Duygusal, sadık       |
| **Genel İzleyici** | +0.3        | Yüzeysel, geniş kitle |

*Fan kitlesi en yüksek sadakat ve pozitif duygu skoruna sahiptir; sinefiller daha eleştirel, aksiyon severler görsel kaliteye odaklıdır.*

---

## 💡 3. Sonuçlar ve Stratejik Öneriler

* İzleyici kitlesi **tek tip değildir**; her segment farklı duygusal ve tematik önceliklerle filmi değerlendirir.
* **Fan kitlesi** en yüksek etkileşime sahip gruptur; kampanyalar bu duygusal bağlılık üzerinden güçlendirilebilir.
* **Sinefiller** film derinliğine, **Aksiyon Severler** görsel kaliteye odaklanmaktadır.
* Film pazarlamasında **veri tabanlı kişiselleştirilmiş kampanyalar** daha etkili sonuç verecektir.
* Sistem, yeni yorumlar geldikçe kendini güncelleyecek biçimde “öğrenen model”e dönüştürülebilir.

---

## 🔭 4. Gelecek Çalışmalar İçin Öneriler

1. **Zaman Serisi Analizi:**
   Fragman öncesi–vizyon sonrası dönemlerde duygu değişimi incelenebilir.
2. **Tür Bazlı Segmentasyon:**
   Aksiyon, dram, korku gibi türlere göre izleyici davranışı kıyaslanabilir.
3. **Platformlar Arası Genişletme:**
   Bu proje yalnızca **YouTube verisine** dayanmaktadır. Gelecekte aynı model TikTok, X (Twitter) veya IMDb üzerinde uygulanabilir.
4. **Gelişmiş Duygu Modellemesi:**
   Derin öğrenme modelleriyle ironi, nostalji gibi karmaşık duygular tespit edilebilir.

---

## 🛠️ 5. Kullanılan Teknolojiler

- **Python** — temel programlama dili  
- **Google YouTube Data API** — YouTube yorumlarını çekmek için  
- **Pandas** — yorumları tablo halinde kaydetmek için  
- **TQDM** — veri çekim sürecinde işlem çubuğu göstermek için

---

## 🏁 6. Genel Sonuç

Bu proje, sinema endüstrisinde **veri temelli karar alma** kültürünün uygulanabilirliğini göstermektedir.
Yapay zekâ tabanlı analizler sayesinde izleyici davranışları daha iyi anlaşılabilir, kampanyalar kişiselleştirilebilir ve **film başarısı tahmin edilebilir hale gelir.**


