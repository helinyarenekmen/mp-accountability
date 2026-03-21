#  Milletvekili Hesap Verebilirlik Portalı

** [helinyarenekmen.github.io/mp-accountability](https://helinyarenekmen.github.io/mp-accountability/)**

Türkiye Büyük Millet Meclisi'nde görev yapmış milletvekillerinin yasama faaliyetlerini karşılaştırmalı olarak sunan interaktif bir veri portalı.

---

## Ne Gösteriyor?

Her milletvekili için şu üç kaynaktan derlenen veriler:

| Veri | Kaynak | Kapsam |
|------|--------|--------|
| **Yazılı Soru Önergeleri** | TBMM resmi kayıtları | 2002–2026 |
| **Meclis Konuşmaları** | ParlaMint-TR + TBMM tutanakları | 2011–2026 |
| **Kanun Teklifleri** | TBMM resmi kayıtları | 2002–2026 |

**266.219 yazılı soru · 363.292 meclis konuşması · 17.605 kanun teklifi · 1.460 milletvekili**

---

## Özellikler

- **MV Arama** — İsim veya ile göre arama; parti ve aktivite düzeyine göre filtre
- **Aktivite Skoru** — YSÖ, konuşma, kanun teklifi ve yasalaşma oranından oluşan bileşik skor
- **MV Detay Sayfası** — Yıllık aktivite grafiği, konu dağılımı, karma konuşma analizi
- **Karşılaştırma** — İki veya daha fazla MVyi yan yana kıyasla
- **Parti Analizi** — Parti bazında toplam performans grafikleri
- **İl Haritası** — İl bazında YSÖ yoğunluğu
- **Sıralama Tablosu** — Dönem ve yıla göre filtrelenebilir aktivite sıralaması
- **Türkçe / İngilizce** dil desteği

---

## Aktivite Skoru Nasıl Hesaplanıyor?

```
Skor = YSÖ/Yıl (%40) + Kanun Teklifi/Yıl (%25) + Konuşma/Yıl (%20) + Yasalaşan Teklif (%15)
```

Her bileşen tüm MVler arasında **yüzdelik sıraya** (percentile rank) dönüştürülür. Böylece farklı dönemlerde aktif olan milletvekilleri adil biçimde karşılaştırılır.

---

## Veri Kaynakları

- **Yazılı Soru Önergeleri:** TBMM.gov.tr resmi arama sistemi
- **Meclis Konuşmaları (2011–2022):** [ParlaMint-TR v5.0](https://www.clarin.eu/parlamint) — CLARIN projesi, JSI
- **Meclis Konuşmaları (2022–2026):** TBMM genel kurul tutanaklarından web scrape
- **Konu Etiketleme:** Anthropic claude-3-haiku ile otomatik sınıflandırma (5 kategori: İnsan Hakları, Ekonomi, Güvenlik, Çalışma, Diğer)

---

## Bağlam

Bu portal, *"Parliamentary Discourse Coalitions in Hybrid Regimes: Evidence from Turkey (2011–2026)"* başlıklı yüksek lisans tez projesinin bir parçası olarak geliştirilmiştir. Tezin amacı TBMM'deki söylem koalisyonlarını ağ analizi yöntemleriyle incelemektir.

**Ana tez veri deposu:** [github.com/helinyarenekmen/thesis](https://github.com/helinyarenekmen/thesis)
**Ağ analizi kodu:** [github.com/helinyarenekmen/plenarynetwork](https://github.com/helinyarenekmen/plenarynetwork)

---

## Teknik Detaylar

- Tamamen istemci taraflı (backend yok) — tüm veri `index.html` içine gömülüdür
- [Plotly.js](https://plotly.com/javascript/) ile interaktif grafikler
- GitHub Pages üzerinden sunulmaktadır

---

*Son güncelleme: Mart 2026 — Veri: 2011-06-28 → 2026-03-12*
