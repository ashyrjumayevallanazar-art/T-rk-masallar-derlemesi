# Masal Sandığı: Anadolu'dan Hikâyeler

**İstanbul Medipol Üniversitesi · Görsel İletişim Tasarımı · Programlamaya Giriş**

Anadolu masallarını çocuklara uygun bir arayüzde sunan, **8 masallık bir web sitesi**. İlk vize sürümünde bütün kod `index.html` içinde bulunuyordu. **“External CSS ve JS ile Projenizi Yapılandırma” ödevi** kapsamında CSS ve JavaScript kodlarını ayrı dosyalara taşıdık. Sitenin tasarımı ve özellikleri korundu.

## Proje dosyaları

```text
T-rk-masallar-derlemesi/
├── index.html       # Sayfanın HTML iskeleti
├── style.css        # Harici CSS: tasarım, kartlar, mobil uyum
├── script.js        # Harici JavaScript: masallar ve etkileşimler
├── README.md        # Projeyi tanıtan bu dosya
├── main.tex         # Önceki vize raporunun LaTeX kaynak dosyası
└── 86230057_Allanazar_Ashyrjumayev_ProgramlamayaGiriş_Güz_Vize.pdf  # Önceki vize raporunun PDF'i
```

**Bu ödevin temel üçlü dosyası:** `index.html`, `style.css` ve `script.js`. Bu üçü aynı klasörde tutulmalıdır. Masalların kapakları SVG veri adresleri biçiminde kod içine gömülüdür; web sitesi için ayrıca resim klasörü gerekli değildir.

## Nasıl çalıştırılır?

1. GitHub sayfasındaki **Code → Download ZIP** seçeneğinden depoyu indirin.
2. ZIP dosyasını bir klasöre çıkarın.
3. `index.html`, `style.css` ve `script.js` dosyalarının **aynı klasörde** olduğundan emin olun.
4. `index.html` dosyasını Chrome, Edge, Firefox veya Safari gibi bir tarayıcıda açın.

Web sitesinin masallarını okumak için internet bağlantısı gerekmez; ancak üç dosyanın da birlikte indirilmiş olması gerekir. Kaynak bağlantılarına gitmek için internet kullanılır. GitHub'ın kod önizleme sayfası web sitesini çalıştırmaz; indirilmiş HTML dosyasını tarayıcıda açın.

## Harici CSS ve JavaScript bağlantıları

`index.html` dosyasının `<head>` bölümünde CSS şöyle bağlanır:

```html
<link rel="stylesheet" href="style.css">
```

HTML'in sonunda JavaScript şu şekilde bağlanır:

```html
<script src="script.js" defer></script>
```

- **HTML:** Başlık, menü, masal arşivi, kaynakça ve okuma penceresinin yapısını oluşturur.
- **CSS:** Kâğıt tonları, Georgia başlıkları, kart düzeni, düğmeler ve `@media` ile ekran boyutuna uyarlamayı yönetir.
- **JavaScript:** Masal verilerini işler; filtreleme, arama, favoriler, okundu durumu ve okuma penceresini çalıştırır.
- `defer` sayesinde betik, HTML ayrıştırıldıktan sonra çalıştırılır.

## Web sitesinin özellikleri

- **Sekiz masal:** Dört Öğüt, Değirmenci ile Tilki, Fatmacık ile Yusufçuk, Keloğlan ve Altın Bülbül, Tuz Kadar Sevgi, Üç Turunçlar, Nardaniye Hanım ve Keloğlan Masalı (Bir Nohut).
- **Arama:** Masal adında, açıklamasında, türünde ve hikâye metninde arama.
- **Filtreleme:** Tümü, türler, Favorilerim ve Okuduklarım.
- **Okuma penceresi:** Masal kapağı ve tam metni, önceki/sonraki masal, yazı boyutu değiştirme.
- **Favoriler ve okundu kaydı:** Tarayıcının `localStorage` alanını kullanır. Bazı dosya önizleyicilerinde veya özel gizlilik ayarlarında kayıt kalıcı olmayabilir.
- **Rastgele masal:** Tek tuşla sekiz hikâyeden birini açar.
- **Duyarlı tasarım:** Geniş ekranda çok sütunlu, dar ekranda iki veya tek sütunlu kart yerleşimi.
- **JavaScript kapalıyken okuma:** HTML'deki `<details>` ve `<summary>` öğelerinde sekiz masalın metnine ulaşılabilir.
- **Kapak çizimleri:** Sekiz ayrı SVG illüstrasyonu; hazır stok görsel kullanılmadı.

## Kodun genel mantığı

`script.js` içinde `stories` dizisi masal bilgilerini tutar. `visibleStories()` arama ve kategori koşullarına göre listeyi süzer. `renderCards()` süzülmüş masalları kart hâlinde ekrana yerleştirir. `openStory()` ve `showStory()` seçilen hikâyeyi okuma penceresinde gösterir. `setFlag()` ve `persist()` favori/okundu bilgilerini günceller ve kaydetmeye çalışır.

Harici dosyalara ayırma sırasında bu temel işlevler yeniden yazılmadı; daha önce tek HTML içinde bulunan stil ve betikler, bağlantıları değiştirilerek ayrı dosyalara taşındı.

## Rapor ve önceki vize çalışması

Depoda önceki vize çalışmasına ait PDF ve `main.tex` de tutulmaktadır. **Bu yeni ödev**, önceki PDF'yi değiştirmekten çok web sitesini üç dosyaya ayırmaya yöneliktir. PDF'de eski *içsel CSS/JS* düzeni anlatıldığı için yeni dosya yapısını görmek isteyenler bu README'yi ve `index.html` içindeki harici dosya bağlantılarını esas almalıdır.

**Not:** `main.tex` içinde önceki rapora ait bazı ekran görüntülerine `assets/` yollarıyla başvurulur. Bu görüntüler olmadan kaynak dosyayı doğrudan yeniden derlemek mümkün olmayabilir; PDF raporunun kendisi depoda yer almaktadır.

## Kullanılan teknolojiler

HTML5, CSS3, JavaScript (ES6+), SVG veri adresleri ve tarayıcı `localStorage`. Harici çatı (framework), hazır CSS kütüphanesi veya çevrimiçi API kullanılmıyor.

## Kaynak ve yapay zekâ açıklaması

Masallar geleneksel anlatılardan yararlanılarak çocuklara uygun biçimde **yeniden anlatılmıştır**; kaynak sayfalardaki tam metinlerin birebir kopyası değildir. Kaynak bağlantıları web sitesinin **Kaynaklar** bölümünde ve vize raporunda bulunur.

ChatGPT; HTML/CSS/JavaScript oluşturma ve düzenleme, kodları harici dosyalara ayırma, etkileşimleri kontrol etme, masal anlatılarını genişletme, SVG kapak taslakları ve rapor/README düzenleme aşamalarında kullanılmıştır. Projenin sunumunda kodların çalışma mantığını açıklamak ve son kullanıcı kontrolü proje sahibinin sorumluluğundadır.

## Bağlantılar

- **GitHub:** https://github.com/ashyrjumayevallanazar-art/T-rk-masallar-derlemesi
- **YouTube sunumu:** Henüz eklenmedi; video hazırlandıktan sonra bağlantı eklenecek.

---

**Hazırlayan:** Allanazar Ashyrjumayev · **Öğrenci no:** 86230057

**Yeni ödev teslimi:** GitHub deposu bağlantısını ilgili assignment alanına ayrıca eklemek gerekiyor.
