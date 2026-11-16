# Masal Sandığı – Anadolu'dan Hikâyeler

Merhaba, ben Allanazar Ashyrjumayev. Bu projeyi Programlamaya Giriş dersinde hazırladım. Türk masallarını bir araya getirip sade, kolay okunabilen bir web sayfası oluşturmak istedim. Sitede sekiz masal bulunuyor. Her masalın ayrı kapak resmi var ve kullanıcılar istedikleri masalı seçip okuyabiliyor.

## Yeni ödevde ne yaptım?

Vize projemde HTML, CSS ve JavaScript kodlarının hepsi `index.html` dosyasının içindeydi. Hocamızın yeni yönergesinde bunları **üç farklı dosyaya ayırmamız** istendi.

Bunun için sayfanın HTML kısmını `index.html` içinde bıraktım. Renkleri, yazı tiplerini ve sayfanın görünümünü düzenleyen kodları `style.css` dosyasına; arama, masal açma ve diğer düğmelerin çalışmasını sağlayan kodları da `script.js` dosyasına taşıdım. Böylece kodları daha düzenli bir şekilde incelemek mümkün oldu.

## Projenin üç ana dosyası

- **index.html:** Sayfanın başlıkları, menüsü, masal kartlarının bulunduğu alan ve okuma penceresinin HTML yapısı.
- **style.css:** Sayfanın renkleri, yazı tipleri, kartların görünümü ve telefona uygun yerleşim.
- **script.js:** Masalların bilgileri, arama kutusu, filtreler, favoriler, okundu işareti ve okuma penceresinin çalışması.

Ayrıca şu an okuduğun **README.md** dosyası projenin açıklaması için var. Depoda önceki vize çalışmama ait **PDF raporu** ve **main.tex** dosyası da bulunuyor. Bunlar üç ana kod dosyasından ayrı.

HTML dosyasında CSS ve JavaScript bağlantılarını şu şekilde kullandım:

```html
<link rel="stylesheet" href="style.css">
<script src="script.js" defer></script>
```

İlk satır CSS dosyasını, ikinci satır JavaScript dosyasını sayfaya bağlıyor.

## Projeyi nasıl açabilirsiniz?

1. GitHub sayfasında **Code > Download ZIP** seçeneğine tıklayıp projeyi indirin.
2. ZIP dosyasını bilgisayarınızda bir klasöre çıkarın.
3. `index.html`, `style.css` ve `script.js` dosyalarının aynı klasörde olduğundan emin olun.
4. `index.html` dosyasına çift tıklayıp bir internet tarayıcısında açın.

Masal metinleri ve kapak resimleri dosyalarda kayıtlı olduğu için internet olmadan da okunabiliyor. Kaynak bağlantılarını açmak için ise internet gerekiyor.

## Sitede neler var?

Sitede sekiz Türk masalı bulunuyor: Dört Öğüt, Değirmenci ile Tilki, Fatmacık ile Yusufçuk, Keloğlan ve Altın Bülbül, Tuz Kadar Sevgi, Üç Turunçlar, Nardaniye Hanım ve Keloğlan Masalı (Bir Nohut).

Masalları arama kutusundan bulmak, türüne göre seçmek, favorilere eklemek ve okundu olarak işaretlemek mümkün. Ayrıca rastgele masal seçme düğmesi ve okuma sırasında yazıyı büyütüp küçültme seçenekleri var.

## Kodun çalışma mantığı

`script.js` dosyasında masallar `stories` adlı bir dizide tutuluyor. `visibleStories()` arama ve filtreye uygun masalları buluyor. `renderCards()` bunları sayfada kart olarak gösteriyor. Kullanıcı bir masala bastığında `openStory()` ve `showStory()` hikâyeyi açıyor.

Favoriler ve okundu işaretleri tarayıcının `localStorage` alanına kaydedilmeye çalışılıyor. Böylece üyelik oluşturmadan bu işaretler saklanabiliyor. `style.css` içindeki `@media` kuralları da sayfanın telefon ve bilgisayar ekranlarında farklı şekilde yerleşmesini sağlıyor.

Bu ödevde amacım sitenin özelliklerini değiştirmek değil, aynı projeyi hocamızın istediği gibi **harici CSS ve JavaScript dosyalarıyla** çalışır duruma getirmekti.

## Masalların kaynakları

Masalların kaynak bağlantılarını web sitesinin **Kaynaklar** bölümüne ve önceki vize raporuna ekledim. Sitedeki metinler geleneksel masalların çocuklar için sadeleştirilmiş uyarlamalarıdır.

## Bağlantı

**GitHub deposu:** https://github.com/ashyrjumayevallanazar-art/T-rk-masallar-derlemesi

**Hazırlayan:** Allanazar Ashyrjumayev  
**Öğrenci no:** 86230057  
**Ders:** Programlamaya Giriş

