# 📊 ProGantt Studio — v18.3

**ProGantt Studio**, kurulum gerektirmeyen, tek bir HTML dosyasından çalışan profesyonel bir proje zaman çizelgesi (Gantt) uygulamasıdır. Tarayıcınızda açın, projelerinizi planlayın — başka hiçbir şeye ihtiyacınız yok.

---

## 🚀 Nasıl Başlarım?

1. `ProGantt_18.3.html` dosyasını bilgisayarınıza indirin.
2. Dosyaya **çift tıklayın** — Chrome, Edge veya Firefox ile açılır.
3. Hepsi bu kadar! Uygulama anında çalışmaya başlar.

> 📌 **Hesap veya kayıt gerekmez.** Giriş yapmanıza, üye olmanıza ya da herhangi bir kişisel bilgi girmenize gerek yoktur. Verileriniz tamamen sizin bilgisayarınızda, tarayıcınızın belleğinde saklanır.

> ⚠️ **İlk çalıştırma için internet bağlantısı gereklidir.** Uygulama bazı görsel bileşenleri (ikonlar, kütüphaneler) internetten yükler. Çevrimdışı kullanım için "HTML olarak kaydet" özelliğini kullanın (aşağıda anlatılıyor).

> ⚠️ **Çalışmalarınız önbelleklenir kaydetmeniz için kaydet tuşunu kullanın** Uygulama verileri tarayıcı belleğine (localStorage) kaydeder. Tarayıcı geçmişini veya çerezleri temizlediyseniz veriler silinir. Düzenli olarak **JSON dışa aktarma** ile yedek alın.


---

## 🗂️ Ekranı Tanıyalım

Uygulama üç ana bölümden oluşur:

```
┌─────────────────────────────────────────────────────────────┐
│  Araç Çubuğu (üst)                                          │
├──────────────────────┬──────────────────────────────────────┤
│                      │                                      │
│  Görev Listesi       │  Zaman Çizelgesi (Gantt Grafiği)     │
│  (sol panel)         │  (sağ panel)                         │
│                      │                                      │
├──────────────────────┴──────────────────────────────────────┤
│  Proje Sekmeleri (alt)                                       │
└─────────────────────────────────────────────────────────────┘
```

| Bölüm | Ne işe yarar? |
|---|---|
| **Araç Çubuğu** | Görev ekleme, geri al/ileri al, kaydet/yükle, dışa aktar |
| **Görev Listesi** | Görevlerin adı, tarihi, süresi, ilerlemesi burada görünür |
| **Zaman Çizelgesi** | Görevlerin grafiksel olarak zaman üzerindeki görünümü |
| **Proje Sekmeleri** | 8 farklı proje arasında geçiş yapılır |

---

## 📁 Projeler ve Sekmeler

Uygulama aynı anda **8 ayrı projeyi** yönetebilir. Ekranın altındaki renkli sekmelere tıklayarak projeler arasında geçiş yapabilirsiniz.

### Proje Adını veya Rengini Değiştirme

- Sekme üzerindeki **kalem ikonuna** tıklayın.
- Proje adını düzenleyin veya rengi değiştirin.

### Sekme Sıralamasını Değiştirme

- Bir sekmeyi sürükleyip başka bir sekmenin yanına bırakın — sıra otomatik değişir.

---

## ✅ Görev Ekleme

1. Araç çubuğundaki **`+ Görev Ekle`** düğmesine tıklayın.
2. Açılan forma şu bilgileri girin:
   - **Görev Adı** — Ne yapılacak?
   - **Başlangıç Tarihi** — Ne zaman başlıyor?
   - **Süre (gün)** — Kaç gün sürecek?
   - **İlerleme (%)** — Şu an yüzde kaçı tamamlandı?
   - **Kategori** — Görevin türünü seçin (aşağıya bakın)
3. **Kaydet** butonuna tıklayın.

### Görev Kategorileri

| Kategori | Renk | Kullanım Alanı |
|---|---|---|
| Software | 🔵 Mavi | Yazılım geliştirme |
| Hardware | 🟠 Turuncu | Donanım işleri |
| Design | 🟣 Mor | Tasarım ve mimari |
| Experiments | 🩷 Pembe | Deneysel çalışmalar |
| Prototyping | 🟡 Sarı | Prototip üretimi |
| Test & Verification | 🟢 Yeşil | Test ve doğrulama |
| Quality Assurance | 🩵 Teal | Kalite güvencesi |
| Field Test | 🟤 Amber | Saha testleri |
| Deployment | ⚫ Gri | Yayına alma |

---

## 🔽 Alt Görev (Subtask) Ekleme

Büyük görevleri daha küçük parçalara bölebilirsiniz:

1. Görev listesinde bir görevin yanındaki **`›` okuna** tıklayarak görevin altını açın.
2. Araç çubuğundan **`+ Alt Görev`** seçin.
3. Alt görev, otomatik olarak üst görevin altında görünür.

> 💡 Üst görevin **süresi ve ilerlemesi**, alt görevlere göre otomatik hesaplanır.

---

## ✏️ Görev Düzenleme

### Adı veya Bilgileri Değiştirme
- Görev listesinde ilgili alana (ad, tarih, süre, ilerleme) **doğrudan tıklayın** ve yazın.

### Gantt Grafiğinde Sürükleyerek Ayarlama
- **Görev çubuğunu** sol veya sağa sürükleyin → başlangıç tarihi değişir.
- **Çubuğun sağ kenarını** sürükleyin → süre uzar veya kısalır.
- **İlerleme barını** sürükleyin → tamamlanma yüzdesi güncellenir.

---

## 🔗 Görevler Arası Bağımlılık Tanımlama

"B görevi, A bitmeden başlayamaz" gibi ilişkiler kurabilirsiniz:

1. Araç çubuğundan **bağlantı aracını** (zincir ikonu) seçin.
2. Gantt grafiğinde bir görevin sağ kenarındaki **yuvarlak noktaya** tıklayın (fare yaklaştırınca görünür).
3. Ardından bağımlı olacak görevin sol kenarındaki noktaya tıklayın.
4. Ok çizgisi otomatik oluşur.

> 💡 Bir bağımlılık bağlantısına **silgi aracıyla** tıklayarak silebilirsiniz.

---

## 🛠️ Araçlar

Araç çubuğunun sol kısmında üç araç bulunur:

| İkon | Ad | Ne Yapar? |
|---|---|---|
| 🖱️ | **İmleç** | Görevleri taşı, yeniden boyutlandır, seç |
| 🔗 | **Bağlantı** | Görevler arası bağımlılık çiz |
| 🧹 | **Silgi** | Bağımlılık oklarını sil |

---

## 🔍 Görünümü Ayarlama

### Zaman Çizelgesini Kaydırma
- Gantt grafiği üzerinde **sağ tıklayıp sürükleyin** → grafik kayar.
- Yatay kaydırma çubuğunu kullanın.

### Yakınlaştırma / Uzaklaştırma
- Araç çubuğundaki **kaydırma çubuğunu** (slider) hareket ettirin → haftaların genişliği değişir.

### Panel Boyutunu Ayarlama
- Sol panel (görev listesi) ile sağ panel (Gantt) arasındaki **dikey çizgiyi** sürükleyin → panellerin genişliğini ayarlayın.

### Bugünün Çizgisi
- Grafik üzerinde **kırmızı dikey çizgi** bugünün tarihini gösterir.

---

## 🗑️ Görev Silme

**Yöntem 1 — Silgi aracı ile:**
Silgi aracını seçin, ardından görevin Gantt çubuğuna tıklayın.

**Yöntem 2 — Klavye ile:**
Görev listesinde bir göreve tıklayarak seçin, ardından `Delete` tuşuna basın.

**Birden fazla görev silmek için:**
`Ctrl` (Mac'te `⌘`) tuşunu basılı tutarak birden fazla göreve tıklayın, ardından `Delete` tuşuna basın.

---

## ↩️ Geri Al / İleri Al

| İşlem | Windows/Linux | Mac |
|---|---|---|
| Geri Al (Undo) | `Ctrl + Z` | `⌘ + Z` |
| İleri Al (Redo) | `Ctrl + Y` veya `Ctrl + Shift + Z` | `⌘ + Shift + Z` |

Veya araç çubuğundaki **ok ikonlarını** kullanın.

---

## 📋 Kopyala / Yapıştır

| İşlem | Windows/Linux | Mac |
|---|---|---|
| Kopyala | `Ctrl + C` | `⌘ + C` |
| Yapıştır | `Ctrl + V` | `⌘ + V` |

Kopyalanan görev, orijinalinin hemen altına **(Kopya)** adıyla eklenir.

---

## 💾 Kaydetme ve Yükleme

### Otomatik Kayıt
Uygulama yaptığınız değişiklikleri **tarayıcıya otomatik kaydeder**. Sayfayı kapatıp tekrar açsanız bile verileriniz korunur.

> ⚠️ Bu kayıt **tarayıcıya özgüdür**. Farklı bir tarayıcı veya cihazdan açarsanız veriler görünmez.

### Veri Yedekleme (JSON Dışa Aktar)
Verilerinizi başka bir cihazda kullanmak veya yedeklemek için:

1. Araç çubuğundaki **`Dışa Aktar`** düğmesine tıklayın.
2. `.json` uzantılı bir dosya indirilir.

### Veri Geri Yükleme (JSON İçe Aktar)
1. Araç çubuğundaki **`İçe Aktar`** düğmesine tıklayın.
2. Daha önce kaydettiğiniz `.json` dosyasını seçin.

---

## 📤 Dışa Aktarma Seçenekleri

### Excel'e Aktar (`.xlsx`)
Projenizi görsel Gantt çubuklarıyla birlikte Excel tablosuna aktarır:
- Araç çubuğundaki **Excel ikonu**na tıklayın.
- `ProGantt_Visual_Export_TARIH_SAAT.xlsx` dosyası indirilir.

### HTML Olarak Kaydet (Çevrimdışı Kullanım)
Uygulamayı verilerinizle birlikte tek bir HTML dosyasına gömer:
- Araç çubuğundaki **`HTML Kaydet`** düğmesine tıklayın.
- İndirilen `ProGantt_Local.html` dosyasını internetsiz de açabilirsiniz.

---

## ⌨️ Klavye Kısayolları Özeti

| Kısayol | İşlev |
|---|---|
| `Ctrl + Z` | Geri al |
| `Ctrl + Y` / `Ctrl + Shift + Z` | İleri al |
| `Ctrl + C` | Seçili görevi kopyala |
| `Ctrl + V` | Yapıştır |
| `Delete` | Seçili görevi sil |

---

## ❓ Sık Karşılaşılan Sorular

**S: Verilerimi kaydettim ama tekrar açınca kayboldu.**
C: Uygulama verileri tarayıcı belleğine (localStorage) kaydeder. Tarayıcı geçmişini veya çerezleri temizlediyseniz veriler silinir. Düzenli olarak **JSON dışa aktarma** ile yedek alın.

**S: Grafik yavaş açılıyor.**
C: Uygulama açılışta internet üzerinden bazı kütüphaneler yükler. İlk yükleme birkaç saniye sürebilir. Çevrimdışı kullanmak için "HTML Kaydet" özelliğini kullanın.

**S: Bir görevi başka bir projeye taşıyabilir miyim?**
C: Şu an için taşıma özelliği yoktur. Görevi kopyalayıp hedef projede yapıştırabilirsiniz.

**S: 8'den fazla proje ekleyebilir miyim?**
C: Hayır, uygulama aynı anda maksimum 8 proje slotunu destekler.

---

## 🔧 Teknik Bilgiler

- **Gereksinim:** Modern bir tarayıcı (Chrome, Edge, Firefox — güncel sürüm)
- **Kurulum:** Yok — tek HTML dosyası
- **Veri depolama:** Tarayıcı localStorage + JSON/HTML dışa aktarma
- **Teknolojiler:** React 18, Tailwind CSS, SheetJS (Excel aktarımı)

---

## 📄 Lisans

Bu uygulama kişisel ve kurumsal kullanım için serbestçe kullanılabilir.

---

*ProGantt Studio v18.3 — Tek dosya, sınırsız planlama.*
