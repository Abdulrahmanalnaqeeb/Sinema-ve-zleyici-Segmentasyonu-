
# 🎬 Sinema ve İzleyici Segmentasyonu (YouTube Yorum Analizi – Akademik Versiyon)

## 🔍 1. Araştırma Soruları ve Amacı

Bu proje, **film pazarlaması ve izleyici psikolojisini veriyle anlamlandırmak** amacıyla tasarlanmıştır.
Çalışma, YouTube platformundan toplanan 150.000 film yorumuna dayanmaktadır ve şu üç temel soruya yanıt aramaktadır:

1. **Filmimizi kimler izliyor ve yorum yapıyor?**
   (Gençler, sinefiller, eleştirmenler veya eğlence odaklı izleyiciler mi?)
2. **Pazarlama stratejisinde hangi unsur öne çıkarılmalı?**
   (Senaryo derinliği mi, yoksa görsel efektlerin kalitesi mi?)
3. **Sadık müşteri kitlesi (fanlar) kimdir ve ortak özellikleri nelerdir?**

🎯 **Amaç:**
Film yorumlarını doğal dil işleme (NLP) teknikleriyle analiz ederek,
izleyicinin duygusal ve davranışsal eğilimlerini veriyle görünür kılmak.

---

## 🧠 2. Projenin Genel Çerçevesi

Bu çalışma, izleyici davranışını **duygusal (sentiment)** ve **segment bazlı (profil)** olarak çözümlemektedir.

| Segment                            | Tanım                                   | Temel Odak                 | Pazarlama Katkısı              |
| ---------------------------------- | --------------------------------------- | -------------------------- | ------------------------------ |
| 🎬 **Sinefil / Hikâye Odaklı**     | Derinlik, anlam, karakter gelişimi arar | Senaryo, kurgu, mantık     | Eleştirel kalite ölçütü sağlar |
| 💥 **Görsel / Aksiyon Sever**      | Tempo, görsel kalite, ses efektleri     | VFX, sahne, sinematografi  | Fragman gücünü belirler        |
| 👑 **Fan Kitlesi**                 | Oyunculara duygusal bağlılık duyar      | Oyunculuk, rol, performans | Viral etki ve sadakat yaratır  |
| 🍿 **Genel İzleyici (Hype/Tepki)** | Eğlence ve merak odaklıdır              | Fragman, trend, popülerlik | Gişe başarısının motorudur     |

---

## 🧩 3. Veri Süreci ve Teknik Altyapı

| Aşama              | Açıklama                                                                                                                        |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| **Veri Toplama**   | YouTube Data API ile 150.000 yorum çekilmiştir. Her yorum; kullanıcı, tarih, beğeni, dil ve içerik bilgileriyle kaydedilmiştir. |
| **Ön İşleme**      | Spam, link, emoji, tekrar eden yorumlar filtrelenmiştir.                                                                        |
| **Dil Tespiti**    | `langdetect` kullanılarak çok dilli yorumlar tespit edilmiştir.                                                                 |
| **Duygu Analizi**  | `TextBlob` ile pozitif, negatif veya nötr duygu etiketleri atanmıştır.                                                          |
| **Segment Atama**  | Anahtar kelimelere göre her yorum 4 ana izleyici grubuna kategorize edilmiştir.                                                 |
| **Görselleştirme** | `Matplotlib` ile duygu ve segment dağılımları görselleştirilmiştir.                                                             |

---

## 📊 4. Bulgular ve Görseller

### 🎞️ Genel Duygu Dağılımı (150.000 Yorum)

| Duygu                 | Yorum Sayısı | Oran (%) |
| --------------------- | ------------ | -------- |
| 🍿 Olumlu (Beğeni)    | 44.187       | 29.5     |
| 🍅 Olumsuz (Eleştiri) | 18.196       | 12.1     |
| 😐 Nötr / Analitik    | 87.617       | 58.4     |

📈 **Grafik 1: Genel Duygu Dağılımı (V2.0)**
<img width="571" height="387" alt="Ekran_görüntüsü_2026-01-19_011222-removebg-preview" src="https://github.com/user-attachments/assets/90a8b9d0-f80d-460b-8a40-904d05b152a4" />
> **Yorum:**
> İzleyicilerin yaklaşık üçte biri filmi beğenmiş, %12’si eleştirmiştir.
> Ancak en büyük pay nötr yorumlardadır (%58.4) — bu, izleyicilerin önemli bir kısmının duygusal değil, **analitik veya tartışmacı** tonda yazdığını göstermektedir.
> Bu sonuç, sinema deneyiminin artık sadece “duygu” değil, **düşünsel değerlendirme** süreci haline geldiğini ortaya koymaktadır.

---

### 🧠 İzleyici Segmentlerinin Davranış Profili

| Segment               | Toplam Yorum | Duygu Skoru | Sadakat    | Viral Etki |
| --------------------- | ------------ | ----------- | ---------- | ---------- |
| 🎬 **Sinefil**        | 14.690       | +0.18       | Düşük      | Orta       |
| 💥 **Aksiyon Sever**  | 1.416        | +0.55       | Orta       | Yüksek     |
| 👑 **Fan Kitlesi**    | 1.932        | +0.82       | Çok Yüksek | Orta       |
| 🍿 **Genel İzleyici** | 14.690       | +0.33       | Orta       | Çok Yüksek |

📈 **Grafik 2: İzleyici Segmentlerinin Davranış Profili (Radar Analizi)**
<img width="533" height="406" alt="image" src="https://github.com/user-attachments/assets/928abfbe-cd55-40d0-b831-63dc9d3f5013" />
> **Analiz:**
>
> * *Fan kitlesi* en yüksek pozitif skor (+0.82) ve sadakat oranına sahip. Bu grup duygusal bağlılıkla filmi savunuyor.
> * *Sinefiller* düşük sadakat ama yüksek eleştirellik gösteriyor. Onların geri bildirimi “kalite göstergesi” olarak değerlendirilmeli.
> * *Genel izleyici* “viral yayılım” açısından en güçlü gruptur. Filmin sosyal medya görünürlüğünü artırır.

---

## 💬 5. Segment Bazlı İçerik Analizi

### 🟢 Pozitif Yorumlar

| Segment            | En Çok Kullanılan Kelimeler                      | Ana Temalar                          |
| ------------------ | ------------------------------------------------ | ------------------------------------ |
| **Genel İzleyici** | “this”, “was”, “great”, “love”, “amazing”        | Heyecan, beğeni, eğlence             |
| **Fan Kitlesi**    | “actor”, “perfect”, “love him/her”, “my idol”    | Oyuncu bağlılığı, hayranlık          |
| **Aksiyon Sever**  | “vfx”, “camera”, “scene”, “sound”, “fight”       | Görsel kalite, sinematografi         |
| **Sinefil**        | “plot”, “story”, “dialogue”, “ending”, “writing” | Senaryo derinliği, karakter gelişimi |

### 🔴 Negatif Yorumlar

| Segment            | En Çok Kullanılan Kelimeler                     | Ana Temalar                       |
| ------------------ | ----------------------------------------------- | --------------------------------- |
| **Genel İzleyici** | “boring”, “overrated”, “waste”, “disappointing” | Beklenti karşılanmaması           |
| **Fan Kitlesi**    | “shouldn’t”, “ruined”, “hate”, “bad ending”     | Karakter ölümü / değişimi tepkisi |
| **Aksiyon Sever**  | “cgi”, “cheap”, “slow”, “bad fx”                | Görsel kalite düşüşü              |
| **Sinefil**        | “cliché”, “flat”, “lazy writing”                | Senaryo yetersizliği              |

---

## 💡 6. Stratejik Çıkarımlar ve Uygulama Önerileri

### 🎯 6.1 Pazarlama Segmentasyonu Önerileri

| Segment            | Kampanya Dili               | Temel Mesaj                         | Önerilen Kanal           |
| ------------------ | --------------------------- | ----------------------------------- | ------------------------ |
| **Fan Kitlesi**    | Duygusal, karakter merkezli | “Kahraman geri döndü.”              | Instagram / TikTok       |
| **Aksiyon Sever**  | Görsel kalite vurgusu       | “Bu sahne sinemada izlenir.”        | YouTube / IMAX işbirliği |
| **Sinefiller**     | Hikaye ve metafor odaklı    | “Sadece bir film değil, bir fikir.” | Letterboxd / Reddit      |
| **Genel İzleyici** | Eğlenceli, kısa içerik      | “İzle, paylaş, konuş.”              | TikTok / Shorts          |

### 🔁 6.2 Öğrenen Sistem Modeli

Bu proje yalnızca bir analiz değil, **geri besleme mekanizması** da önerir:

1. **Veri toplanır →** yorumlar sınıflandırılır.
2. **Kampanyalar güncellenir →** hangi mesaj daha iyi etkileşim alır test edilir.
3. **Yeni yorumlar →** sistem kendini tekrar eğitir.

> Böylece ortaya çıkan yapı, “**dinamik öğrenen pazarlama modeli**” haline gelir.

---

## 🔭 7. Gelecek Çalışmalar İçin Öneriler

1. **Zaman Serisi Analizi:**
   Duyguların zamanla nasıl evrildiği incelenebilir (örneğin, fragman–vizyon–haftalar sonrası).
2. **Tür Bazlı Segmentasyon:**
   Farklı türlerde (aksiyon, dram, komedi) izleyici profilleri kıyaslanabilir.
3. **Platformlar Arası Karşılaştırma:**
   YouTube dışındaki platformlarda (X, TikTok, IMDb) aynı yöntem uygulanabilir.
4. **Derin Öğrenme Tabanlı Analiz:**
   BERT veya GPT-tabanlı modellerle “ironi”, “nostalji” gibi karmaşık duygular yakalanabilir.

---

## 🛠️ 8. Kullanılan Teknolojiler

- **Python** — temel programlama dili  
- **Google YouTube Data API** — YouTube yorumlarını çekmek için  
- **Pandas** — yorumları tablo halinde kaydetmek için  
- **TQDM** — veri çekim sürecinde işlem çubuğu göstermek için

---

## 🏁 9. Genel Sonuç

Bu proje, **150.000 izleyici yorumuna dayalı veri bilimiyle film kültürü analizi** yapmıştır.
Sonuçlar, izleyici davranışının duygusal, sosyal ve bilişsel boyutlarını ortaya koymuştur:

* **Fan kitlesi** markalaşma açısından duygusal sermaye üretir.
* **Sinefiller** kaliteyi ölçen eleştirel filtre işlevi görür.
* **Aksiyon severler** görsel üretimin standardını belirler.
* **Genel izleyici** gişe başarısını büyüten viral akışı sağlar.

🎯 Kısaca: **Film başarısı, bu dört segmentin dengeli yönetilmesiyle sağlanır.**


