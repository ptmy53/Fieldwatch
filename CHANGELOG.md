# Yenilikler

En yenisi önce. Bu, Fieldwatch'tur (`app.fieldwatch`). Aşağıdaki her derleme, Ayarlar'da sürüm olarak görünen sürümdür.

Fieldwatch, Spectre 1.2.14 saha derlemesini yeni bir ad, uygulama kimliği ve MIT Lisansı altında sürdürür. Bir telefondaki Spectre'ın yerini almaz.

## 1.2.2 — 23 Kasım 2026

- Android 13 ve üzeri sürümlerde bildirim izni istenir; reddetmek artık uygulamayı engellemez. Tarama bildirimi yine gösterilir, böylece ekran kapalıyken tarama çalışmaya devam edebilir. Uyarı bildirimleri, siz izin verene kadar kapalı kalır.
- Katalog 118, bir ürün adı veya o şirketin kendi Bluetooth kimliği için satırlar ekler: Air Lift, BlueParrott, Danlaw, Directed, Dreo, GN Hearing, Grundfos, HughesNet, iFIT, Kia, Kuna, Lighthouse, Lippert, Optimum, Otodata, PrepWizard, Procon, Pura, Redtiger, ResMed, Rinnai, Sennheiser, SonicWall, Soundstream, Toast, Turtle Beach, Ubee, Victron ve Vivint. Bunların hiçbiri bip sesi çıkarmaz. Eddystone mağaza işaretçileri eşleşmeden kalır.
- Katalog 118, zaten mevcut olan satırlara dört kurulum ve seri adı ekler. Tuya, SmartLife- veya SmartLife_ ile başlayıp dört karakterle devam eden bir kurulum Wi-Fi adıyla eşleşir. Bu ad yalnızca eşleştirme sırasında görünür. UniFi, UDM Setup ile başlayan bir kurulum Wi-Fi adıyla, yani bir Dream Machine ile eşleşir. Midea, net_ac_ ile başlayan bir kurulum Wi-Fi adıyla eşleşir. net kelimesi tek başına Midea değildir. Motive, bu ad yayınlanırken AABL ile başlayan bir Bluetooth adıyla, yani bir Vehicle Gateway serisiyle eşleşir. Bunların hiçbiri bip sesi çıkarmaz.
- Başka bir uygulama, MainActivity'ye gönderilen `app.fieldwatch.OPEN` ile Fieldwatch ekranını açabilir. AutomationService'e gönderilen `app.fieldwatch.CLOSE`, ekranı arka plana gönderir ve taramayı çalışır durumda bırakır. Fieldwatch'u Son Kullanılanlar'dan kaydırarak kapatmak taramayı yine durdurur.
- Oturum dışa aktarma ve Günlük dışa aktarma, en son kullandığınız biçimde açılır. İlk sefer yine Günlük dosyası — CSV'dir. GeoJSON ve ATAK veri paketi Oturum dışa aktarma'da kalır.
- Başka bir uygulama taramayı başlatıp durdurabilir, bir oturumu başlatıp durdurabilir ve taramanın çalışıp çalışmadığını sorabilir. Ayrıca en yeni kaydedilmiş oturumu veya radyo günlüğünü yazabilir. Sonuç, `Android/data/app.fieldwatch/files/automation` altındaki `status.txt` dosyasıdır. Oturum dışa aktarma o kaydedilmiş oturumu yazar. Açık bir oturum ve son 15 dakika dışarıda kalır.
- Ayarlar listesindeki Tarama altındaki satır, tarama yoğunluğunu ve Pil korumasının Açık veya Kapalı olduğunu gösterir.
- Ayarlar → Drone izleme, canlı listedeki bir Remote ID acil durum bildirdiğinde uyarabilir. Anahtar siz açana kadar kapalıdır. Bip sesi, sesli okuma ve sessiz bildirim, o sayfadaki diğer uyarılarla aynı anahtarlardır. Bluetooth ve Wi-Fi üzerindeki aynı UAS ID tek bir uyarıdır. GPS kilidi veya yer imi gerektirmez. Size ait olarak işaretlenmiş bir drone yine uyarı verir. Satır; Remote ID, hava aracı adı veya UAS ID, acil durum bildirdi şeklindedir.
- Canlı yol ile haritayı göster, bir Remote ID izini hareket yönünde beyaz köşeli çift ayraçlar olarak çizer. Açık halka ilk noktadır. Son konum sınıf simgesi olarak kalır. Bildirilmiş bir acil durum o bölümü işaretler.
- Bir oturum yolu, bir Remote ID izini hava aracı kaydıyla aynı köşeli çift ayraçlar, açık halka ve okla çizer. Oturum ve rapor irtifa, hız ve rotayı gösterir. Bildirilmiş bir acil durum zamanı not eder ve o bölümü işaretler.
- Bir Remote ID acil durumu ziyaretle birlikte saklanır. Kart ne zaman bildirildiğini not eder. Yolun o bölümü işaretlenir ve başladığı yerde bir elmas gösterilir.
- Bir Remote ID yolu hareket yönünde köşeli çift ayraçlarla çizilir. Açık halka duyulan ilk noktadır. Ok son noktadır. Ziyaret, hava aracının gönderdiği irtifa, hız ve rotayı gösterir.
- Bir Remote ID ziyareti ne kadar sürdüğünü gösterir. Kayıt, hava aracının gönderdiği yolu ve o ziyaret için tek bir pilot pinini saklar. Aynı alandaki ziyaretler haritayı paylaşır, her biri kendi rengindedir. Diğerlerinden uzak bir ziyaretin kendi haritası olur. Pilot pini 2 km içindeyken çizilir. Gizlilik modu haritayı korur.
- Raporlar, son 14 gündeki Remote ID hava araçlarını listeler. Bir satır bir hava aracıdır. Bir geçiş bir ziyarettir ve sonraki geçiş 20 dakika sessizlikten sonra başlar. Radyo sayfası kaç gün duyulduğunu ve bu geçişten önce ne zaman duyulduğunu gösterir. Bu satır aynı kaydı açar.
- Katalog 117 üç radyoyu adlandırır. iTAG, Bluetooth adı tam olarak iTAG olanla eşleşir. Daha uzun bir ad eşleşmez. VIOFO, VIOFO ile başlayan bir Wi-Fi adıyla eşleşir. Bir oyuncak kamera drone'u, WIFI_UFO veya FLY-UFO- ile başlayan bir Wi-Fi adıyla eşleşir. Drone bip sesi çıkarır. iTAG ve VIOFO çıkarmaz.
- Bilinen kamera sesi tek bir uyarıyı paylaşabilir. Konuşan kameranın 200 m içindeki kameralar sessiz kalır. Anahtar siz açana kadar kapalıdır. Harita yine her kamerayı gösterir.
- Tek türden bir grup çoğulu söyler, örneğin İleride bilinen Flock kameraları. Birden fazla türden bir grup her türü adlandırır, örneğin İleride Flock ve kırmızı ışık kameraları. Tek bir kamera hâlâ size bakıp bakmadığını söyler.
- Porkchop, tam olarak PORKCHOP adıyla ve M5PORKCHOP ile başlayan bir adla eşleşir. Yalnızca bu harfleri içeren daha uzun bir ad eşleşmez. 50:52:4B satıcı işareti yine eşleşir.
- Bir radyoda Sessize al, o radyo için bip sesini, sesli okumayı, bildirimi ve titreşimi durdurur. Aynı imza adıyla listede kalır. Size ait olarak işaretlenmez.
- Katalog 116, yakın zamandaki bir oturumdan dört radyoyu adlandırır. LEDnetWF, LEDnetWF ile başlayan bir Bluetooth adıyla eşleşir. EZ Lynk, EZLYNK ile başlayan bir Wi-Fi adıyla eşleşir. Trackunit, Trackunit'in şirket kimliğiyle eşleşir. OontZ, OontZ ile başlayan bir Bluetooth adıyla eşleşir. Bunların hiçbiri bip sesi çıkarmaz.
- Ekran kapalıyken başlayan bir tarama açık kalır. Konum, Fieldwatch bir sonraki ekranda olduğunda eklenir.
- Adlandırılmış bir radyo sessizleştiğinde uyarabilir. Anahtar siz açana kadar kapalıdır. 2 dakika boyunca duyulduktan sonra tek bir bip, bir titreşim ve bir sesli mesaj verir. Sessize al sessiz kalır. Benim de bunu kullanabilir. Taramayı durdurmak bunu tetiklemez.
- Bu sürüm için paketlenmiş dil dosyaları yazılır.

## 1.2.1 — 20 Kasım 2026

- İzleme listesindeki sesli okuma, bip sesinden sonra yeniden konuşur. Uzun bir izleme listesi bip sesi çıkarıp cümleyi atlayabiliyordu; çünkü bip sesi, cümle kaydedilmeden önce bitiyordu. Cümle artık saklanır. Duran bir konuşma motoru yeniden başlatılır. Zaten açık olan ses açık kalır.
- Bu sürüm için paketlenmiş dil dosyaları yazılır.

## 1.2.0 — 19 Kasım 2026

- Ayarlar → Drone izleme bölümünde Drone çevre algılama bulunur. Anahtarın altındaki satır, aşağıda seçilen menzil içinde Remote ID kullanan bir drone algıladığını söyler. Anahtarın altındaki mesafeler 100 m, 250 m, 500 m ve 1 km'dir; başlangıç 250 m'dir. 50 m veya daha iyi bir GPS kilidi gerekir. Bip sesi, sesli okuma ve sessiz bildirim, sürü uyarısıyla aynı anahtarlardır. Canlı satır, en son taze konum içindeyken o mesafe içinde olduğunu söyler. Yayın mesafenin bir buçuk katını geçtikten sonra veya o drone gittikten sonra yeniden uyarır. Remote ID yer imi, bu uyarının ilk ipucunu alabilmesi için 10 saniyeye kadar bekler. Uyarı açık olan adlandırılmış bir radyo yine kendi başına uyarır.
- Ayarlar listesindeki o bölüm artık İmza izleme listesi uyarıları olarak adlandırılır.
- Ayarlar listesi Görünüm, İmza izleme listesi uyarıları, Konum ve Haritalar ile TAK'ta aynı Açık ve Kapalı ifadelerini kullanır. Hücresel bağlantı izleme uyarı cümlesini söyler. İmza izleme listesi uyarıları altındaki not, izlenen bir radyo için sessiz bildirimi adlandırır.
- Ayarlar → İzleyici izleme, bir uyarı ilk açıldığında bip sesi çıkarır ve konuşur. İkisi de siz birini kapatana kadar açıktır. Sistem bildirimi siz açana kadar kapalıdır. Bu bildirim sessizdir ve açılır pencere açıkken gösterilebilir. Bunlar kapalıysa açılır pencere yine açılır. Bir uyarının size nasıl ulaşacağı; GPS girişimi, Güvenilir ağlar, Hücresel bağlantı izleme, Drone izleme ve İzleyici izleme üzerinde aynı bloktur.
- Drone sürüsü algılama, Remote ID aşağıdaki zaman penceresinde yeni drone'lar algıladığında uyarır. Ayarlar → Drone izleme, sürü uyarısı ve mesafe uyarısı için kendi başına bip sesi çıkarır ve konuşur. İkisi de siz birini kapatana kadar açıktır ve ikisi de izleme listesini izlemez. Sistem bildirimi siz açana kadar kapalıdır. Bu bildirim sessizdir. Bunlar kapalıysa uyarı yine açılır. Tek bir Uyarı size nasıl ulaşsın bloğu ikisini de kapsar.
- Düşük pil koruma modu siz seçene kadar kapalıdır. Düşük pil taramayı Pil tasarrufuna düşürür, ardından durdurabilir. Pil tasarrufu açıkken Wi-Fi ve Bluetooth simgeleri sarıya döner. Kaydedilmiş yoğunluk korunur. Şarja takmak yavaşlatmayı geri alır. Bir durdurma, Fieldwatch açılana kadar durmuş kalır.
- Sizinle ayrılmış etiket uyarıyı açıklar. Paragraf, bir izleme etiketinin sahibinden uzakta olduğunu, ardından bu telefonun onu kaç dakika ve kaç yerde duyduğunu söyler.
- İki yerde duyuldu uyarıyı açıklar. Paragraf, bir izleme etiketinin bu telefonun bulunduğu yerlerde duyulduğunu söyler.
- Katalog 113 iki yönlü telsizleri adlandırır. Bir BLE KISS TNC, KISS hizmetiyle eşleşir. Icom IC-705, Bluetooth adı ICOM BT(IC-705) ve Wi-Fi adı IC-705 ile eşleşir. Icom ID-5200, ICOM BT(ID-5200) ile eşleşir. Icom UT-137, ICOM BT-003 ile eşleşir. Bir Blu-PTT düğmesi, yayınladığı hizmetle eşleşir. TIDRADIO TD-H9, TD-H9 ile başlayan bir adla eşleşir. Bir AINA PTT Smart Button, ASB artı altı karakterle eşleşir. Wireless CPS açık olan bir el telsizi, tam olarak walkie-talkie adıyla eşleşir. Bu ad marka veya modeli söylemez. Bunların hiçbiri bip sesi çıkarmaz.
- Katalog 112, bu telefonun görmeye devam ettiği radyoları adlandırır. Samsung TV'ler ve soundbar'lar kurulum adıyla eşleşir. Google Cast, FEA0 hizmetiyle eşleşir. Levoit, MELK, Midea, Zebra, JLab, ScentAir, Escort, Gard Pro, Vizio, Owlet, Tandem t:slim, SleepTracker, WHOOP, soundcore, Hume, Platco, NEEWER, 70mai, BlackVue, Galaxy Watch ve Galaxy Buds'ın her birinin bir satırı vardır. CHB, HarpBT ve GT201 bir ad önekiyle eşleşir. Bu üçünün arkasındaki ürün tanımlanmadı. Epson ayrıca bir ET- Series adıyla eşleşir. Bluetooth üzerindeki bir Samsung fırını cihaz satırıyla eşleşir. Osmo, osmo_ ile başlayan bir Wi-Fi adıyla eşleşir. UniFi, U6- veya UXG model adıyla eşleşir. Bunların hiçbiri bip sesi çıkarmaz.
- Katalog 114, yakın zamandaki oturumlardan radyoları adlandırır. Acuity aydınlatma, hizmeti veya şirket kimliğiyle eşleşir. Cardo, Cardo adıyla veya FREECOM ile başlayan bir adla eşleşir. Cobra, 2A668FA4 hizmetiyle eşleşir. Bir ELK LED şerit, ELK-BLEDO ile başlayan bir adla eşleşir. Bir GLI açık tabelası, GLI1050 ile başlayan bir adla eşleşir. GM phone-as-key, FE48 hizmetiyle veya GM_PEPS ile başlayan bir adla eşleşir. Gree, GR-AC_ ile başlayan bir adla eşleşir. Bir HIKMICRO termal optik, HIKMICRO_ ile başlayan bir Wi-Fi adıyla eşleşir. IOSiX, IOSiX ELD ile başlayan bir Wi-Fi adıyla eşleşir. iRobot, iRobot'un şirket kimliğiyle eşleşir. JLG ClearSky, JLG'nin şirket kimliğiyle veya ClearSky Smart Fleet adıyla eşleşir. Bir LG cihazı kurulum adıyla eşleşir. Mazda, Mazda ile başlayıp _SPL ile biten bir adla eşleşir. Mentra Live gözlükler, Mentra_Live ile başlayan bir adla veya XyBLE_ artı daha fazla karakterle eşleşir. Phillips Connect, şirket kimliğiyle eşleşir. Pulsar termal ve gece görüş optikleri, Stream Vision Wi-Fi adlarıyla eşleşir. RNode, RNode artı dört onaltılık karakter adıyla eşleşir. Rove, ROVE ile başlayan bir adla eşleşir. Steiner ve Burris termal optikleri, Steiner ve Burris_BTH adlarıyla eşleşir. Bir Steiner M830 LRF dürbünü, LRF X, Steiner LRF X, LRF1535 veya Steiner LRF1535 ile eşleşir. TBS Crossfire, TBS_XF_AP_ ile başlayan bir Wi-Fi adıyla eşleşir. TOZO, TOZO ile başlayan bir adla eşleşir. Mentra Live gözlükler, Steiner M830 LRF dürbün ve TBS Crossfire bip sesi çıkarır. Diğer yeni satırlar çıkarmaz. Brilliant Frame artık Brilliant Labs glasses (Frame / Halo) oldu. Even G1 artık Even Realities G1 / G2 oldu. Apple AirTags artık Find My (AirTag or other Apple) oldu.
- GitHub'dan stok kataloğunu güncelle, `dist/fieldwatch-signatures.rsi` dosyasını okur. 1.1.12–1.1.44 arası telefonlar hâlâ `dist/fieldwatch-signatures-v2.json` okur. 1.1.11 hâlâ `dist/fieldwatch-signatures.json` okur.
- Bu sürüm için paketlenmiş dil dosyaları yazılır.

## 1.1.44 — 13 Kasım 2026

- Exposure Notification, FD6F hizmetindeki bir Bluetooth reklamını adlandırır. Radyo sayfası tanımlayıcının orada olduğunu ve meta verinin şifreli olduğunu söyler. Bu baytları göstermez. Bip sesi çıkarmaz. Katalog 111 imzayı ekler.
- BTHome, FCD2 hizmetini kullanan bir Bluetooth sensörünü adlandırır. Radyo sayfası, cihazın yayınladığı ölçümleri; sıcaklık, nem, pil, kapı ve hareket dahil gösterir. Açık bir kapı veya pencere canlı satırda gösterilir. Şifreli paketler yalnızca şifreli olduklarını söyler. Katalog 110 imzayı ekler. Bip sesi çıkarmaz.
- Remote ID kimlik doğrulaması, plakanın gönderdiği türü, sayfayı ve zamanı gösterir. İmza baytları sayfada kalmaz. İmzayı doğrulamaz. Aynı oturumdaki bir konum mesajı bu bloğu korur. Bip sesi çıkarmaz.
- Amazon Sidewalk, AMA hizmetini ve Amazon'un şirket kimliğini gönderen bir Bluetooth cihazını adlandırır. Kayıt modu canlı satırda gösterilir. Radyo sayfası işaretçi türünü ve pil bandını gösterir. Gizli kimliği göstermez. Bu hizmeti olmayan bir Echo, Amazon olarak kalır. Katalog 109 imzayı ekler. Bip sesi çıkarmaz.
- Matter kurulumu, Matter devreye almayı sunan bir Bluetooth cihazını adlandırır. Radyo sayfası, cihazın gönderdiği satıcı kimliğini, ürün kimliğini ve ayırt ediciyi gösterir. Canlı satır Matter kurulumu der. Yakınlık mesafe ölçümü adlandırılır ve gizli kimliği göstermez. Katalog 108 imzayı ekler. Bip sesi çıkarmaz.
- HomeKit, aksesuarın yayınladığı kategoriyi ve eşleştirilmiş satırını adlandırır. Eşleştirilmemiş bir aksesuar o kategoriyi canlı satırda gösterir. Eşleştirilmiş göstermez. Katalog 107 imzayı ekler. Bip sesi çıkarmaz.
- Fransız Direct Remote ID, o Wi-Fi işaretçisi mevcut olduğunda hava aracı konumunu, irtifasını, hızını, rotasını ve kalkış pinini doldurabilir. Kalkış üzerindeki yükseklik radyo sayfasında gösterilir ve hava aracı pini değildir. Bu plakadaki bir CTA-2063 seri numarası üreticiyi adlandırabilir. Üç harfli kod adlandıramaz. Aynı oturumdaki daha sonraki bir Fransız plakası saklanan plakayı değiştirir. Android 11 veya üzeri. Katalog 106, hâlâ Fransız plakasının bir konumu doldurmadığını söylüyorsa Remote ID notunu günceller.
- Karşılaştır ve Özet, büyük bir oturumda yüzdeyi ilerletmeye devam eder. Metin dosyasını yazmak bu çubuğun çoğunu oluşturur; parçalar halinde yazıldığı için dosya bitene kadar tırmanır. Sayısı olmayan bir adım da yüzdeyi yavaşça ilerletir, böylece bekleme takılı görünmez.
- Bir Wi-Fi erişim noktası ağın ne tür olduğunu, interneti olup olmadığını, bir mekanı ve bir hotspot kimliğini söyleyebilir. Ayrıntı, işaretçi bunu içerdiğinde gösterir. Android 11 veya üzeri. Bu değerleri erişim noktası belirler. Doğrulanmazlar.
- Karşılaştır (metin) ve Özet (metin) bir metin dosyasını paylaşır. Büyük bir rapor artık tüm metni paylaşım aktarımına koymaz.
- Bir paylaşım açılamazsa Fieldwatch nedenini söyler. Buna telefonun depolama alanının dolması, belleğin tükenmesi veya paylaşımın açılmayacak kadar büyük olması dahildir.
- Google Find Hub, yük uzunluğundan seçilen 20 baytlık veya 32 baytlık geçici bir kimlik gösterir. Karma bayrak baytı reklamda olduğunda satır bunun mevcut olduğunu söyler. Bu bayt şifrelidir, bu yüzden değer gösterilmez. Katalog 105 bunu satırı zaten kaydetmiş bir telefona kopyalar.
- Google Find Hub çerçevesi 0x40, ayrılmamış olarak etiketlenir. Bu çerçeve istenmeyen izleme korumasının kapalı olduğu anlamına gelir. Etiketin sahibine yakın olduğunu söylemez. 0x41 çerçevesi ayrılmış olarak kalır. Katalog 104 bu ifadeyi satırı zaten kaydetmiş bir telefona kopyalar.
- Ayarlar → İzleyici izleme, ikisi de siz birini açana kadar kapalı olan iki uyarıya sahiptir. Sizinle ayrılmış etiket; bir etiket sahibinden uzakta olduğunu söylediğinde, bu telefon onu 20 dakikayı aşan boşluk olmadan 30 dakika duyduğunda ve bu telefonun GPS'i en az 100 m arayla üç nokta aldığında uyarır. İki yerde duyuldu; kararlı bir adrese sahip bir bulucu iki durağa ulaştığında uyarır. Yerler listesi her iki durumda da kalır. Radyoyu aç o radyoyu açar. Kapat, aynı koşul sürerken bu uyarıyı kapalı tutar. Bip sesi yoktur. Fieldwatch ekranda değilken sessiz bir bildirim aynı satırları gösterir.
- Pebblebee, Pebblebee ve moto tag adlarının yanı sıra Bluetooth hizmeti FA25 ile de eşleşir. Adını göndermeyen bir etiket yine eşleşir. Bu hizmet, etiketin sahibinden uzakta olup olmadığını söylemez. Find Hub ve DULT kendi satırlarında kalır. Satır bip sesi çıkarmaz.
- 25 baytlık bir Find My reklamı, genel anahtar yayınladığını söyler. 2 baytlık bir reklam, kısa biçim olduğunu, genellikle sahibine yakın bir etiketi ifade ettiğini ve bunun kesin olmadığını söyler. Pil seviyesi yalnızca son-sahip biti ayarlandığında gösterilir. AirTag imzası değişmez.
- Bu sürüm için paketlenmiş dil dosyaları yazılır.
- Bir dil dosyası en fazla 352 KiB olabilir. İngilizce şablon bu sınıra sığar.

## 1.1.43 — 9 Kasım 2026

- Quest olan bir Bluetooth adı; Quest ile başlayıp boşluk veya tireyle devam eden bir ad; ya da Meta Quest ile başlayan bir ad Meta Quest'tir. Quest 3S o satırdır. Ray-Ban / Meta glasses olarak etiketlenmez ve bip sesi çıkarmaz. Bu ad olmadan bir Meta şirket kimliği veya FEB8 hizmeti hâlâ gözlük satırıyla eşleşir.
- Bluetooth kanalı ve frekansı boş bırakılır. Android reklam kanalını bildirmez, bu yüzden radyo sayfası ve günlük artık 2402 MHz'i ölçülmüş gibi göstermez. Wi-Fi kanalı ve frekansı kalır. Zaten 2402 diyen eski bir günlük satırı olduğu gibi kalır.
- İmza adayları tam bir özel hizmet UUID'sini korur. Artık bunu farklı bir Bluetooth hizmetiyle eşleşebilecek dört onaltılık basamağa indirmez. Standart bir 16-bit hizmet hâlâ kısa biçimiyle ve tam Bluetooth UUID'siyle eşleşir.
- 0 olan bir Wi-Fi sinyali okuma yokmuş gibi değerlendirilir. Artık en güçlü radyo olarak sıralanmaz veya yüksek sinyal gibi boyanmaz. Gerçek bir okuma hâlâ öyle davranır.
- Günlük, telefonun zaten sakladığı Bluetooth reklamını 512 bayta kadar tutar. Ham alan o reklamdır. Üretici verisi kendi alanıdır. Zaten kaydedilmiş bir günlük satırı olduğu gibi kalır.
- Adlandırılmış radyolar, Ayarlar listesinde Uyarılar'dan sonra kendi satırıdır. İmza ve ağ, Uyarılar'da kalır.
- Radyo ayrıntısı GitHub katalog isteği gösterebilir. Bu, eşleşmeyen bir Bluetooth radyoda; telefonun interneti olduğunu iddia eden bir ağı olduğunda, ad fabrika modeline benzediğinde ve bu ad bu oturumda iki adreste duyulduğunda görünür. Dokunmak tarayıcıda bir GitHub issue taslağı açar. O dokunuştan önce hiçbir şey gönderilmez. Taslak; adres son ekini, bu telefonun konumunu ve ham reklamı dışarıda bırakır.
- İmzalar → A–Z Sınıfı, imzası olmayanlar dahil her sınıfı listeler. O sınıfta bir imza olana kadar sayı 0'dır. Vücuda takılan, Giyilebilirler altındadır.
- Microsoft Nearby Sharing, cihaz türünü ve paylaşımın Yalnızca cihazlarım mı yoksa Yakındaki herkes mi olarak ayarlandığını adlandırır. Yakındaki herkes olduğunda satır, o reklamdan gelen bilgisayar adını içerir. Bu arka plan işaretçisi artık Swift Pair olarak adlandırılmaz.
- Katalog 101, Novatel Wireless satırını kaldırır. 28:80:A2 adresi Inseego'da kalır ve kamu güvenliği olarak bip sesi çıkarmaz. Hatch, C8:FA:9C adresini bırakır. Hatch adları ve şirket kimliği kalır. Bu uygulamayı açmak, GitHub'dan stok kataloğunu güncelle zaten katalog 101'i kaydetmiş ve bunları yerinde bırakmış olsa bile, bu satırı ve bu adresi yerleşik imzalardan kaldırır. Eklediğiniz bir kural kalır. Yerleşik olmayan özel bir Novatel kopyası kalır.
- Filtreler İki yönlü telsizler ve Askeri ekler. İki yönlü telsizler; radyo eşleşmeyi beklerken Bluetooth adı ICOM BT(ID-52) olan Icom ID-52'yi ve Icom VS-3, Yaesu SSM-BT10, Yaesu SSM-BT20, Kenwood KHS-55BT, Kenwood KHS-56BT ve VGC BHM-88 kablosuz mikrofonlarını içerir. Bu mikrofonlarda Bluetooth, mikrofonun çalışma şeklidir. Her satır, Low Energy reklamında yayınlanan adla eşleşir. Yalnızca Classic bağlantıda görünen bir ad sessiz kalır. Askeri'de henüz imza yok. Katalog 102 ayrıca Benshi tabanlı radyoları tam Bluetooth adı UV-PRO, UV-50PRO, GA-5WB, VR-N75, VR-N76, VR-N7500, VR-N7600 veya DB50-B olanlarla; BLE bas-konuş düğmelerini de PTT-Z, PTT-AZ veya PTT-Z01 adlı olanlarla eşleştirir. Hiçbiri bip sesi çıkarmaz.
- Bu uygulamanın bilmediği bir sınıf, kural veya radyo kullanan bir imza dosyası, önce Fieldwatch'u güncellemenizi ister. Bu mesajdaki Şimdi güncelle bir uygulama güncellemesi denetler. Telefondaki katalog olduğu gibi kalır. Aynı mesaj GitHub'dan stok kataloğunu güncelle, İmzaları içe aktar ve Ayarları içe aktar için kullanılır.
- Wi-Fi satıcı etiketleri WPA, WMM, WPS, Wi-Fi Direct, Miracast, Hotspot 2.0, MBO-OCE, EasyMesh ve OWE geçişini adlandırır. Bir WMM etiketi artık Microsoft olarak okunmaz. Diğer satıcı etiketleri hâlâ OUI'ye sahip şirketi gösterir.
- Katalog 100, ExpressLRS kurulum Wi-Fi'sini, Xiaomi Mi Home hizmeti FE95'i ve bir EZVIZ kurulum ağını ekler. Her biri tek bir modeli değil aileyi adlandırır. ExpressLRS, diğer drone satırları gibi bip sesi çıkarır. Diğer ikisi çıkarmaz.
- Katalog 99: DJI ayrıca daha eski DroneID Wi-Fi işaretçisi, satıcı IE 26:37:12 ile de eşleşir. Bu, hava aracını etiketler. Bir konumu doldurmaz. ASTM Remote ID, Remote ID satırında kalır. Android 11 veya üzeri bu işaretçi alanını görebilir.

## 1.1.42 — 5 Kasım 2026

- Uzun bir sürüşte canlı oturum haritası güncel kalır. Çizgi, duraklar ve kamera işaretleri olduğu yerde kalır.
- Raporlar → Yol üzerinde, o görünüme ait kamera resmi haritayla birlikte kayar. Aynı rengin iki diliminin üst üste geldiği yerde tonlama bir kez boyanır.
- Bir radyonun ayrıntı sayfasındaki Av, yeni bir av başlatır. Av'dan ayrılmak yürüyüşü temizler.
- Sinyal kaybolduğunda büyük sayı - - olarak, altındaki satır -- dBm · Sinyal Kayboldu olarak okunur.
- Filtreler rastgeleleştirilmiş Bluetooth'u gizleyebilir. Wi-Fi kalır. Oturum yine bu radyoları tutar.
- Bu sürüm için paketlenmiş dil dosyaları yazılır. Sinyal Kayboldu ve Rastgeleleştirilmiş Bluetooth'u gizle, 1.1.41'den beri eklenen satırlardır.

## 1.1.41 — 4 Kasım 2026

- GPS, hücre, güvenilir ağ ve taşma için uyarı iletişim kutuları tek bir düzen kullanır. Neden bir paragraftır. Okumalar Ayrıntılar altında yer alır; etiket ve değer aynı satırdadır.
- Güncelleme teklifi Sürüm Notları başlığına sahiptir. Uzun notlar kaydırılır.
- Bu telefondaki bir uygulama GPS konumunu üretiyorsa uyarı Olası GPS girişimidir. Bu telefondaki bir uygulamanın GPS konumunu ürettiğini ve bu telefonun uydular yerine bunu kullandığını söyler.
- Bir hücre uyarısı başlıkta ne olduğunu korur. Paragraf, Fieldwatch'un nedeni söyleyemediğini belirtir.
- Bu sürüm için paketlenmiş dil dosyaları yazılır. Sürüm Notları, 1.1.40'tan beri eklenen satırdır.

## 1.1.40 — 3 Kasım 2026

- Bu telefon başlangıçta çevrimiçiyse Fieldwatch, GitHub'a daha yeni bir sürüm olup olmadığını sorar. Daha yeni bir sürüm notları Şimdi güncelle ve Daha sonra ile gösterir. Daha sonra, daha yeni bir sürüm yayınlanana kadar o sürümü atlar. Ayarlar yeniden denetleyebilir. Şimdi güncelle uygulamayı indirir ve Android yine kurulumu onaylamanızı ister. GitHub yanıt vermezse bu telefondaki uygulama olduğu gibi kalır.
- Ekrandaki notlar daha kısadır. Denetimin ne yaptığını söyler. Tarama durumu artık taramayı pasif olarak adlandırmaz. Anahtarların altındaki Ayarlar notları tek satırdır. Daha uzun açıklama kullanım kılavuzunda kalır.

## 1.1.39 — 2 Kasım 2026

- Uygulamayla gelen bir dil dosyası, bu sürüm için yazıldığını söyler. İçe aktarılan bir dosya, yazıldığı sürümden sonra eklenen anahtarları bildirir. Daha eski bir dosyadan gelen çevrilmiş satır yine gösterilir.

## 1.1.38 — 2 Kasım 2026

- Samsung SmartTags, SmartTag adıyla veya FD5A hizmetiyle eşleşir. Yalnızca Samsung'un şirket kimliğini gönderen bir telefon, TV, Buds veya saat o satırın dışında kalır. Stok katalog 98'dir. Bu sürümü açmak, o şirket kimliğini yerleşik satırdan kaldırır. Eklediğiniz bir kural kalır. GitHub'dan stok kataloğunu güncelle aynı dosyayı getirir.
- Raporlar, son 7 gün içinde iki veya daha fazla yerde duyulan, oturumu olmayan ve şu anda duyulmayan radyoları listeler. Harita bu telefonun nerede olduğunu gösterir. Her radyonun haritada ve adının yanında kendi rengi vardır. Gizlilik modu haritayı ve koordinatları gizler.
- Bu raporda her durak numaralandırılır. Saat, sokak ve koordinat kendi satırlarındadır. Numaralar düzdür. Ad, canlı listenin Ad + tür biçimidir. Canlı'dan ayrılmış olan dahil bir radyoyu açmak için dokunun.
- Hücresel bağlantı izleme, Hücre bağlantısını izle açık olana kadar kapalıdır. Bir yerdeki ilk durağan ziyaret yalnızca öğrenir. Öğrenme süresi 3 günle başlar. Seçenekler Yok, 1 gün, 3 gün, 7 gün ve 14 gündür. Daha sonraki bir ziyaret yeni bir hücrede veya 2G ya da 3G'ye düşüşte uyarabilir. İletişim kutusu ülke, operatör, kanal ve bant listeleyebilir. Bir uyarı oturumla örtüştüğünde Özet bir bölüm alır. Uyarı, izleme listesinden ayrıdır. Tanılama, izleme kapalıyken bile kampı listeler.
- Uyarılar altındaki İmza ve ağ, duyuruda imzanın yerini alan kelimeleri kaydeder. Bu kelimeler, o ağ adına sahip o imzanın her radyosuna uygulanır. Ağ adı söylenmez. Tek bir radyodaki ad hâlâ önce gelir. Yalnızca sınıfı söylemek kelimeleri kayıtlı tutar ve sınıfı söyler. Liste Ayarları dışa aktar ile gider.
- Güvenilir ağlar, öğrenmenin ne kadar süresi kaldığını gösterir. Öğrenme süresi 1 saat ekler. Süreyi değiştirmek zaten kaydedilmiş erişim noktalarını unutmaz.
- Canlı yol ile haritayı göster ve Raporlar → Yol bir kamera düğmesine sahiptir. Resimdeki işaretleri gizler veya yeniden gösterir. Seçim kaydedilir. Av'ın düğmesi yoktur. Yol altındaki liste, oturum raporu ve yazdırılan yol hâlâ katman anahtarlarını izler.
- Yeni ayarlar ve uyarı metni, uygulamayla gelen 26 dilin tamamındadır.

## 1.1.37 — 29 Ekim 2026

- Canlı yol ile haritayı göster ve Av, yön değiştikçe döner. Ekranda zaten olan harita onunla döner, böylece kenarlar dolu kalır. Yerinde durmak veya telefonu yerinde çevirmek haritayı olduğu yerde bırakır.
- Canlı yol ile haritayı göster veya Av üzerinde çift dokunma, yakın görünüm ile tüm yol arasında hemen geçiş yapar.
- Canlı listeye geri dönmek önce listeyi çizer. Harita ardından gelir.

## 1.1.36 — 29 Ekim 2026

- Her güvenilir ağ uyarısı o ağı ve tetikleyen nedeni adlandırır. Başlık Olası kötü ikiz "{name}": {reason} biçimindedir. Neden bunlardan biri veya birkaçı olabilir: açık güvenlik, daha zayıf güvenlik, bilinmeyen cihaz veya alışılmış yerlerden uzakta. Altındaki satır o erişim noktasının adresidir. "00:13:37 Orient Power Home Network'e aittir." fazladan bir satırdır ve yalnızca o adres 00:13:37 ile başladığında görünür. Başka bir adres için uyarı bunu içermez. Bu satır ağ adının veya nedenin yerini almaz ve bu adres bloğu kendi başına uyarmaz.
- Güvenilir ağ uyarı eylemleri kendi satırlarında yer alır.

## 1.1.35 — 29 Ekim 2026

- Dil paketleri ekrandaki metnin daha fazlasını kapsar: canlı oturum satırı, radar, cihaz açıklamaları, filtreler, raporlar ve insan tarafından okunabilir Özet ile Karşılaştır ifadeleri, PDF dahil. İngilizce şablon her satır için bir karakter sınırı listeler. İmza adları ve katalog notları İngilizce kalır. CSV, JSON, GPX, KML ve diğer makine dışa aktarımları olduğu gibi kalır.
- Bir dil paketi içe aktarmak bir metin raporu kaydedebilir. Kullanılacak anahtarları, eksik anahtarları ve uzunluk ile sınırla birlikte çok uzun her satırı adlandırır.
- GNSS girişimi, Konum ve Haritalar ve TAK / CoT, açma/kapama anahtarını altındaki seçeneklerden ayrı gruplar. Her denetimin ne yaptığına dair kısa bir satırı vardır. Uyarı seviyesi, Uyarı başlangıcı ifadesinin yerini alır. Sinyal tutulduğunda uyar, Sahtecilik denetimleri ifadesinin yerini alır. GPS alıcısını uyanık tut, Birlikte solan uyduları say ve Kazanç geriye doğru okur, eski alıcı anahtarlarının yerini alır. Bilinen kameralar, Katmanlar ifadesinin yerini alır. Köşe okuması, Konum ifadesinin yerini alır. Haritada konumu göster, o grubun başlığıdır.
- Güvenilir ağlar üzerinde açma/kapama anahtarı tek başına durur. Uyarı denetimleri, her biri neyi yakaladığına dair kısa bir satırla Uyarılar grubundadır. Öğrenme ve bir uyarının size nasıl ulaşacağı ayrıdır.
- TAK / CoT üzerinde GNSS başlığı GNSS uyarılarıdır. O sayfadaki Güvenilir ağlar başlığı kalkmıştır. Not Ağ uyarıları altındadır.
- TAK / CoT üzerinde Taşmalar başlığı BLE Taşma uyarılarıdır. Bir Wi-Fi işaretçi taşması hâlâ aynı satırı kullanır. TAK denetimlerinin altındaki notlar daha kısadır ve Güvenilir ağlar'ın bir notu vardır.
- TAK / CoT üzerinde, Güvenilir ağlar altında o anahtar Ağ uyarılarıdır. Altındaki tutma süresi Bir uyarı noktasının ne kadar kaldığıdır.
- Güvenilir ağlar TAK pini ve o pinin ne kadar kaldığı Ayarlar → TAK / CoT altındadır. Güvenilir ağları izle açık olana kadar ikisi de soluk kalır.
- Kılavuz, Güvenilir ağlar'ın bir ağı kendiniz kontrol etmenin yerine geçmediğini söyler. Sessiz bir izleme, ağın güvenli olduğuna dair bir bulgu değildir.
- Canlı üzerindeki Görüntüle anahtarı Canlı yol ile haritayı göster'dir.
- Bu telefona giden TAK / CoT artık soketini sabitlemeye çalışmaz. Tanılama, aynı telefondaki beslemenin ATAK'a ulaşıp ulaşmadığını söyler. Soket Wi-Fi veya Ethernet üzerinde açıldığında ATAK'a ulaşır. Yalnızca hücresel bağlantıda Wi-Fi gerekir. Wi-Fi veya Ethernet olmadan açılan bir soket, ikisinden biri bağlandığında yine değiştirilir.
- Gizlilik modu, radyo sayfasında, Metin olarak paylaş'ta ve tek radyo AI Dışa Aktarımı'nda ham reklam baytlarını maskeler. Satır etiketini ve bayt sayısını korur; hex masked olarak gösterilir. Günlükler ve oturum dışa aktarma eksiksiz kalır.
- Bir Samsung SmartTag reklamı artık sahibinden ayrılmış mı yoksa sahibinin yanında mı olduğunu söyler ve ayrılmış bir etiket adres değişiklikleri boyunca takip edilir.
- Canlı yol ile haritayı göster, Av ve Raporlar → Yol, telefonun bağlantısı olmadığında kaydedilmiş harita resimlerini çizer. Kaydedilmiş resmi olmayan bir yer düz bir çizgi olarak kalır. Yeni resimler hâlâ yalnızca çevrimiçiyken indirilir.
- Oturum raporu, katman anahtarı kapalıyken kamera listesini dışarıda bırakır. Sayı ve yazdırılan yoldaki işaretler kapalı kalır. Dosya telefonda kalır. Açık olan bir anahtar, telefonda olmayan bir listeyi yine adlandırır.
- Güvenilir ağlar, o radyonun sayfasında işaretlediğiniz bir Wi-Fi adını izler. O adın daha sonraki bir görülmesinde daha zayıfsa, bilinmeyen bir üreticiden geliyorsa veya bu telefonun genellikle duyduğu yerlerden uzaktaysa uyarabilir. Liste, öğrenme penceresi ve bir TAK pini Ayarlar altındadır. Pin başlangıçta kapalıdır. Telefon ağa bağlanmaz veya parolasını istemez.
- Canlı yol ile haritayı göster ve Raporlar → Yol, bilinen bir kameraya dokunduğunuzda bir kart açar. Kart türü, liste bir tane varsa şirketi ve kayıtlıysa yönü adlandırır. Bir sayı o türden birkaç tane olduğunu belirtir. Kapatmak için işarete yeniden dokunun. Kartta koordinat yoktur.
- Fieldwatch'u açmak artık yol kaydedilmiş bir kamera listesini okurken kapanmaz. Başarısız bir kamera indirmesi ayarlar satırında kalır ve nedenini söyler. Kaydedilmiş bir kopya kalır ve yol yine açılır.
- Bir dil paketi, imzalar, ayarlar, güvenilir ağlar veya stok kataloğu içe aktarmak neden başarısız olduğunu söyler. Okunamayan, boş, çok büyük veya kaydedilemeyen bir dosya telefonda zaten olanı bırakır.
- Canlı üzerindeki bir izleme listesi uyarısı, Canlı yol ile haritayı göster altındaki listede açılır. Sınıfa göre, güç listesi, Zaman çizelgesi ve Hibrit, o satırı haritanın altındaki alanda tutar.
- Haritadaki bilinen bir kameraya dokunmak, bir algılamayla aynı kartı kullanır. Çizgi o karta ulaşır. Aynı noktadaki kameralar birlikte listelenir.

## 1.1.34 — 27 Ekim 2026

- Bu telefona giden TAK / CoT, loopback soketini bağlamadan önce lo'ya sabitler. Wi-Fi veya Ethernet olmadan açılan bir soket, hücresel zaten açıkken bile ikisinden biri bağlandığında değiştirilir. O LAN üzerinde açılan bir soket, LAN düştükten sonra göndermeye devam eder. Tanılama; TAK'ın açık olup olmadığını, hedef türünü ve portunu, loopback soketinin lo'ya bağlı olup olmadığını, açıldığında neyin bağlı olduğunu ve son gönderimin başarılı olup olmadığını listeler. Ana bilgisayar adresi o sayfada kalmaz.

## 1.1.33 — 27 Ekim 2026

- Bu telefona giden TAK / CoT, Fieldwatch bağlı Wi-Fi olmadan başladığında hâlâ ATAK'a ulaşır. Ağ yokken açılan bir soket, ağ olduğunda değiştirilir. Zaten çalışan bir soket, Wi-Fi düştükten sonra göndermeye devam eder.

## 1.1.32 — 26 Ekim 2026

- Canlı yol ile haritayı göster, uyarı noktalarını ve bilinen kameraları sürüş çizgisinin üzerine çizer.
- Av, GPS kilitlenmeden önce yürüyüşü çizer. O resimdeki satır Henüz GPS yok. Bu yürüyüş haritada değil şeklindedir. Sokaklar ve köşedeki yer kapalı kalır. İki taze sabitleme, hâlâ yaklaşık ilk 20 m içindeyken o yürüyüşü yerleştirir. Daha uzun bir yürüyüş haritada kalmaz.
- Raporlar → Yol, kameraları ve algılamaları sürüş çizgisinin üzerine çizer. Yakınlaştırmak, bu noktalar aynı yer olmadığı sürece numaralı bir grubu ayrı noktalara böler.
- Gerçek bir durak yeşil kalır. GPS titremesi artık o bölümü tekrar maviye çevirmez.
- Canlı yol ile haritayı göster, görünüm yakınlaştırıldığında sürüş çizgisini haritada tutar.
- Raporlar → Yol üzerinde yakınlaştırmak sürüş çizgisini haritanın içinde tutar.
- Raporlar → Yol sıkıştırılabilir ve sürüklenebilir. Çift dokunma tüm yolu yeniden sığdırır.
- Bilinen bir kamera, hâlâ yaklaşık 500 m ilerideyken konuşur. Yol raporu hâlâ yaklaşık 150 m içindeki kameraları sayar.
- Sürüş çizgisi biraz daha koyu mavidir. Yeşil bir durak, o mavi çizgiyle aynı genişliktedir.
- Sesli Uyarılar, kırmızı ışık anahtarını Kırmızı ışık kameraları için uyar olarak adlandırır.
- Av, açılır açılmaz en son GPS sabitlemesini gösterir. Daire o sabitlemenin boyutundadır. Isı izi, iki taze sabitleme uyuştuktan sonra başlar ve bundan önce atılan adımlar dışarıda bırakılır. İlk 20 m'de, uyuşmayan tek bir sıkı sabitleme noktayı o sabitlemeye taşır. Adım sensörü eksik olan veya hiç adım bildirmeyen bir telefon, adımları yürüyüş hareketinden sayar. Bir pusula sıçraması, telefonun kendisi dönmüyorsa yürüyüşü taşımaz.
- Oturum raporu, bilinen kameraları Raporlar → Yol ile aynı şekilde listeler. Başlık Yoldaki bilinen kameralardır. Her tür; ad, sonra yola bakan kaç tane ve yönü olmayan yolda kaç tane olduğu şeklindedir. Eksik bir liste yine adlandırılır.
- Bir oturum yolundaki kameralar daha büyük, açık halkalı çizilir; böylece mavi yol üzerinde görünür kalırlar. Canlı yol ile haritayı göster ve Av daha küçük işaretleri korur.
- Raporlar → Yol, bu liste telefonda olmadığında veya katman anahtarı kapalı olduğunda Yoldaki bilinen kameralar bölümünü dışarıda bırakır. Telefonda olan bir liste yine satırlarını gösterir. Özet hâlâ kaydedilmiş bir listeyi sayar.
- Raporlar → Yol, bilinen kameraları haritayla aynı renklerde, her tür için bir satır olarak listeler. Başlığın altındaki satır mesafedir. Özet tam cümleleri korur.
- Raporlar → Yol, yoldaki bilinen kameraları uyarı veren radyoların altında listeler. Satırlar oturum raporuyla eşleşir.
- Kameralar yol çizgisinin üzerinde durur. Bu; Raporlar → Yol, yazdırılan yol ve Canlı yol ile haritayı göster için geçerlidir.
- Bir Özet PDF'indeki ve Karşılaştır'daki yazdırılan yol, telefondaki yolun aynısı mavidir. Gerçek bir durak hâlâ yeşildir. İkinci oturum arduvaz rengindedir. Raporlar → Yol ve o yazdırılan yol, oturum raporunun saydığı kameraları gösterir. Saklanan bir yön, yola doğru bakıyorsa sayılır. Saklanan yön yoksa yolda sayılır. Silah sesi dedektörleri ve uzağa bakan bir yön dışarıda bırakılır. Canlı yol ile haritayı göster ve Av hâlâ açık olan katmanı çizer.
- Oturum raporu, yol boyunca kameraları sayar. Saklanan bir yön, yola doğru bakıyorsa sayılır. Saklanan yön yoksa yolda sayılır. Flock, diğer plaka okuyucular, hız kameraları, kırmızı ışıklar ve diğer kameralar listelenir. Silah sesi dedektörleri dışarıda bırakılır. Sayım bu telefonda kayıtlı listeleri kullanır.
- Raporlar → Yol, bitmiş bir oturumda köşe satırını dışarıda bırakır. Bu satır ızgara ya da Gizlilik modu açıkken maskelenmiş halidir. Açık bir oturum hâlâ bu telefonun nerede olduğunu gösterir.
- Canlı yol ile haritayı göster, sürüşü daha kalın mavi bir çizgi olarak çizer. Gerçek bir durak hâlâ yeşildir.
- Canlı yol ile haritayı göster veya Av üzerinde uzaklaştırmak, her nokta için bir harita resmi gösterir. Daha yakın bir resim artık daha geniş olanın üzerinde kalmaz.
- Canlı yol ile haritayı göster veya Av üzerinde kaydırmak, ekranda zaten olan resimleri tutar ve her resim geldikçe yeni zemini doldurur. O kaydırma yönündeki sonraki ekran, bir sonraki sürükleme için kaydedilir.
- Canlı yol ile haritayı göster ve Av, seyahat yönü boyunca ve rota dönerken biraz yana doğru haritanın sonraki ekranını kaydeder. Bu resimler siz oraya gelene kadar ekranda kalmaz.
- Canlı yol ile haritayı göster üzerinde çift dokunma, henüz hareket etmemiş bir oturumla aynı ölçeği açar. Kısa kenar yaklaşık 220 m'ye ulaşır.
- Av, başlangıcı yalnızca bu sabitleme yaklaşık 12 m içindeyken bir GPS sabitlemesine yerleştirir. Adımları saymayı ister ve buna izin verildikten sonra bu telefonun adım sensörünü kullanır. Av'ı açmak adım sayılmaz.
- Av, adım sensörü adım bildirmeyen bir telefonda bu telefonu izlemeye devam eder. Bu telefon adımları ivmeölçerden sayar.
- Pembe pin av haritasından kaldırıldı.
- Av haritası renkleri bir yerden diğerine yeniden derecelenir. Yüksek bir geçiş, çok daha zayıf bir geçişten hâlâ ağır basar.
- Neredeyse kaybolmuş bir av sinyali mavi kalır. Renk yaklaştıkça tonlar arasında kademeli olarak kırmızıya doğru ilerler ve yaklaşık −50 dBm'de kırmızı görünür. Üzerinde durduğunuz yer, orada duyulan en yüksek okumayı tutar.
- Av, radyo menzil dışına çıktıktan sonra bu telefonu izlemeye devam eder. O yürüyüş bölümüne renk eklenmez, çünkü boyanacak okuma yoktur.
- Av, adımları ve telefon yönünü izler. GPS, o yürüyüşü haritaya yerleştirir ve yalnızca iyi bir sabitleme uyuştuğunda hafifçe düzeltir. Noktanın üzerindeki daire, yürüyüş uzadıkça büyür. Telefonu düz tutun. Eğik telefon adımları duraklatır. Üzerinde durduğunuz yer, orada duyulan en yüksek okumayı tutar. Yaklaşık bir buçuk adım ilerideki sonraki yer, zayıf olan dahil orada duyulan gücü alır. Renk bir yerden diğerine eşit derecelenir.
- Canlı yol ile haritayı göster veya Av üzerinde sürüklemek ya da sıkıştırmak, zaten seçilmiş yönü korur. Seyahat yönü yukarıda kalır. Artık kuzey yukarıya geçmez.
- Canlı yol ile haritayı göster ve Av, seyahatle döndüğünde haritanın köşelerini doldurur.
- Konum ve Haritalar, kaydedilmiş harita resimlerini telefonda 512 MB'a kadar tutar ve temizleyebilir. Kaydedilmiş haritaları temizle, plaka okuyucuları veya diğer sensörleri kaldırmaz.
- Konum ve Haritalar, USGS Imagery Topo ve FAA VFR Sectional ekler. USGS haritaları ve FAA VFR Sectional Amerika Birleşik Devletleri'ni kapsar ve anahtar istemez. FAA VFR Sectional navigasyon için olmadığını söyler. Bu harita için çok uzak bir görünüm yakınlaştırmanızı ister. Harita altında Kaplamalar, seçtiğiniz haritanın üzerine USGS Shaded Relief ve USGS Hydrography koyabilir. İkisi de Amerika Birleşik Devletleri'ni kapsar. Yalnızca harita için kapalı bırakın. Kaplama açıkken harita kredisi ve her kaplama kredisi sağda ayrı satırlardır, böylece soldaki ızgara okunabilir kalır. Kaplamalar kapalıyken harita kredisi tek kısa satır olarak kalır.
- Konum ve Haritalar iki Katman ekler. Plaka okuyucu kameralar, Amerika Birleşik Devletleri plaka okuyucu listesini indirir (yaklaşık 37 MB). Diğer sensörler, hız kamerası, kırmızı ışık, silah sesi dedektörü ve diğer kamera listesini indirir; yaklaşık 1 MB. Harita resimleri aynı kalır. Her iki liste de uygulamayla birlikte gelmez. Her birinin kendi Güncellemesi vardır. İşaretler Canlı yol ile haritayı göster, Av ve Raporlar → Yol üzerinde görünür. Flock plaka okuyucular mavidir. Diğer plaka okuyucular kehribardır. Hız kameraları turkuaz, kırmızı ışıklar kırmızı, silah sesi dedektörleri mor noktalar ve diğer kameralar daha küçük gri işaretlerdir. Bir türden kalabalık o rengi korur. Her türün kendi sesli uyarısı vardır; siz açana kadar kapalıdır. Birini açmak o bildirimi söyler. Bir anahtar işaretleri gizlemez. Plaka okuyucu uyarısı, dosyada varsa şirketi adlandırır.
- Bu liste indirmeyi bitirdikten sonra satır, telefon dosyayı okurken İşleniyor der. Bilinen yönü olan bir sensör görüş konisidir. Harita uzakken küçük kalır, yakınlaştırdığınızda büyür. Yön yoksa ve her silah sesi dedektörü bir noktadır. Yalnızca Flock kameraları olan kaydedilmiş bir kopya, indirilen liste değişmemiş olsa bile Güncelle'den önce sorar.
- Konum ve Haritalar üzerinde, Harita'nın üzerindeki paragraf, Konum'un zaten sahip olduğu kutudan önceki aynı boşluğa sahiptir.
- Bitchat bir Mesh imzasıdır. BLE hizmet reklamıyla eşleşir. Bip sesi çıkarmaz. Ayarlar → GitHub'dan stok kataloğunu güncelle onu ekler. Katalog 97.

## 1.1.31 — 23 Ekim 2026

- Üst çubuktaki Wi-Fi, Bluetooth ve imza sayıları, sayılar değiştikçe satır kaymasın diye her biri 888 için yer tutar.
- Av artık Çok Yakın, Zayıf veya Gitti göstermez. Sayıyı, kıvılcım çizgisini ve bulutu izleyin. Bip ve Titreşim, paket olmadığında veya radyo ayrıldığında hâlâ sessiz kalır.
- Ayarlar → Konum ve Haritalar, Canlı yol ile haritayı göster, Raporlar → Yol ve yol şekli altında Esri, MapTiler, Stadia ve Thunderforest dünya haritalarını kullanabilir. Bu haritalar Anahtar olarak işaretlidir. Kendi hesabınızdan aldığınız anahtarı yapıştırın. Bu telefonda kalır ve Ayarları dışa aktar onu dışarıda bırakır. OpenStreetMap ve USGS haritaları anahtar istemez. Hatalı bir anahtar veya yüklenmeyen bir harita bir açılır pencere gösterir.
- Canlı yol ile haritayı göster üzerinde çift dokunma, tüm yol ile bu telefonun çevresindeki yakın görünüm arasında geçiş yapar. Yakın görünüm bu telefonu merkezde tutar ve kısa kenar yaklaşık 100 m'nin biraz ötesine ulaşır. Kuzey yukarı ve seyahat yönü bu yakınlaştırmayı korur.
- Sürüş çizgisi birkaç metrede bir nokta tutar, böylece bir köşede sokağı izler. Bir dönüş, zaten sürülen yolu olduğu yerde bırakır. Yeşil hâlâ gerçek bir duraktır.
- Canlı yol ile haritayı göster ve Av, N işaretinin olduğu yerde bir pusula düğmesine sahiptir. Kuzey yukarı ve seyahat yönü arasında geçiş yapmak için dokunun. Resim dört birleşimi de gösterir. Uzaklaştırılmış görünüm bükülü bir yoldur; kuzey yukarıdayken üzerinde N vardır. Seyahat yönü, yakın görünümle aynı pusula harflerini daha küçük bükülü bir yolun üzerine koyar. Yakınlaştırılmış görünüm bu harflerdir ya da kuzey yukarıdayken bir okun üzerinde N vardır. Yerinde durmak son yönü korur. Yerinde dönüş haritayı döndürmez. Raporlar → Yol ve kaydedilmiş yol şekli kuzey yukarı kalır.
- Canlı yol ile haritayı göster, bir dönüş boyunca yolu izler. Düz bir bölüm hâlâ GPS yalpalamasını çizginin dışında bırakır. Yeşil gerçek bir duraktır: bu telefon yaklaşık 40 saniye boyunca yaklaşık 25 m içinde kaldı. Sürüşün geri kalanı düz çizgidir.
- Av, harita için sayfanın üst kısmını bırakır. Sayıyı, kıvılcım çizgisini ve bulutu izleyin. Ölçek Zayıf ile başlar. Sayının yanındaki kelimeler dil paketini izler.
- Av, bu telefonun o radyoyu duyduğu yerlerin bir ısı bulutunu çizer. Renk zayıf olduğu yerde maviden, camgöbeği, yeşil, sarı ve turuncudan geçerek güçlü olduğu yerde kırmızıya gider. Bölgeyi yürüyün veya sürün. En parlak yama en yüksek sesle duyulduğu yerdir. En yüksek ses işareti o yamanın içindedir. Bu bir mesafe değildir ve diğer radyonun üzerinde bir pin değildir.
- Av yakın açılır ve bulut daha ince çizilir. Adımlar, GPS sabitlemeleri arasındaki kısa hareketleri doldurur. Yakın zamandaki sıkı bir GPS sabitlemesi yürüyüşü yeniden merkezler.
- Av bulutu yürüyüşü izler. Duyumlar bağlanır ve renk birinden diğerine yumuşakça değişir. Yürüyüşün yakın bölümleri çizgiler arasında dolar. Uzak bir boşluk açık kalır. Kenar o rengi dışarı doğru soldurur.
- Av, yürüyüş uzadıkça size yakın kalır. Sayfadan ayrılmak bulutu Sıfırla'ya kadar veya farklı bir radyo avlayana kadar tutar. Yerinde dönüş noktayı hareket ettirmez. Sol alttaki okuma noktaya uyar. GPS hareket ederken adımlar o yönü izler. GPS takılıyken telefonun üstü kullanılır. Üzerinde durduğunuz yer, orada duyulan en yüksek okumayı tutar. Yaklaşık bir buçuk adım ilerideki sonraki yer, zayıf olan dahil orada duyulan gücü alır. Renk bir yerden diğerine eşit derecelenir.
- Ayarlar → Haritalar, Canlı yol ile haritayı göster, Raporlar → Yol ve yol şekli altındaki haritayı seçer. OpenStreetMap başlangıçtır. USGS Imagery ve USGS Topo Amerika Birleşik Devletleri'ni kapsar. Haritanın köşesindeki küçük satır kaynağı adlandırır.
- Radyo sayfası GPS'in yanında ızgarayı gösterir. Sıradan bir radyo için bu, bu telefonun bulunduğu yerdir. Bir Remote ID hava aracı, hava aracı konumunu ve kalkış, pilot veya sabit noktayı, her biri bir ızgarayla birlikte, artı bu telefondan mesafe ve yönü gösterir. Bir oturum raporu, bu telefonun o konum duyulduğunda nerede olduğunu kullanır ve zamanı adlandırır. Daha eski bir oturum ızgarayı gösterir, mesafe ve yönü dışarıda bırakır. Gizlilik modu ızgarayı maskeler, mesafe ve yönü dışarıda bırakır.
- Ayarlar → Haritalar, bu telefonun şu anda nerede olduğunu haritanın sol alt köşesinde GPS veya ızgara olarak gösterebilir. Kapalı o köşeyi boş bırakır. Gizlilik modu onu maskeler. Bu telefon hareket edene kadar köşe yerinde kalır.

## 1.1.30 — 22 Ekim 2026

- Yerler artık Android 10 ve 11'de uygulamayı kapatmıyor.

## 1.1.29 — 22 Ekim 2026

- Radar üzerinde Görüntüle; Başlık satırı, Alt başlık satırı, Canlı yol ile haritayı göster, RSSI çubukları, Frekans ve İlk / son görülmeyi soldurur. Zaman çizelgesi RSSI çubuklarını soldurur. Kaydedilmiş seçim kalır ve onu kullanan bir görünümde geri gelir. Görünüm, Sırala, Kısa tut ve İmza adları kullanılabilir kalır.
- Konum kapalıyken Fieldwatch, Wi-Fi veya Bluetooth taraması istemez. Konumu açmak bir an bekler, sonra onları yeniden başlatır.
- Fieldwatch bir çökmeden kapanırsa, bir sonraki açılış başka bir şey başlamadan önce ne olduğunu gösterir. Kopyala onu gönderir. Devam uygulamayı açar. Normal bir kapanış onu göstermez.

## 1.1.28 — 22 Ekim 2026

- Canlı yol ile haritayı göster, Görüntüle üzerindedir; ilk anahtardır, RSSI çubuklarının üzerindedir. Kapalı başlar. Açtığınızda bu telefonun kuzey yukarı haritası Canlı'nın üstüne yerleşir, liste hâlâ altındadır. Harita ile liste arasındaki çubuğu sürükleyin. Görünüm Radar iken anahtar soluk kalır ve kapanmaz.
- Çizgi, harita açıldığında bulunduğunuz yerde başlar ve hareket eder etmez çizilir. Sürüş son çizgiden yaklaşık 12 metre ayrıldığında bir kıvrım korunur. Yana doğru GPS yalpalaması çizginin dışında kalır. Oturum yokken çizgi, anahtarı açtığınız zaman ile 15 dakika öncesinin daha geç olanıdır. Açık bir oturum, yürüyerek veya araçla oturumun başından çizer. Noktalar izleme listesi uyarılarıdır. Sıkıştırmak veya sürüklemek görünümü tutar. Yeniden ortala veya çift dokunma sizi yeniden izler.
- Raporlar → Yol aynı çizgiyi kullanır.
- Fieldwatch açıkken Konumu açmak Wi-Fi ve Bluetooth'u bir an duraklatır, sonra yeniden başlatır. Hatalı bir tarama sonucu uygulamayı kapatmak yerine atlanır.
- Özet ve Karşılaştır yol şekilleri sokak döşemelerini dolu çizer. Sorumluluk reddi ve yol başlığı gövde metnini kullanır.

## 1.1.27 — 16 Ekim 2026

- Yerler, bu telefonun son 7 gün içinde iki veya daha fazla yerde duyduğu kararlı bir izleyiciyi ve sessiz bir aradan sonraki dönüşü hatırlar. Satırlar o radyonun sayfasında ve oturum raporundadır; bu telefonun bulunduğu yerle birlikte. Başka bir günden gelen bir durak tarihi içerir. Çevrimiçi yer adları sokağı ekler. Filtreler Canlı'yı şu anda duyabildiklerinizle sınırlayabilir. Adresini değiştiren bir radyo atlanır. Sıradan Wi-Fi ve Bluetooth dışarıda kalır. Bip sesi yoktur ve TAK işaretçisi yoktur. Her radyo en son 8 durağı tutar. Dokuzuncu doğrulanmış durak en eskisini düşürür.
- Kullanıcı kılavuzu Yerler'i açıklar: bir durağın ne olduğu, hangi radyoların uygun olduğu ve sınırlar.
- İmza adayları, günlüğü okuyup kataloğu eşleştirirken bir ilerleme iletişim kutusu gösterir. Çubuk dosyayı izler.
- Oturum dışa aktarma GeoJSON yazabilir. Bu, oturum GPX ve KML ile aynı haritadır: bu telefonun yolu ve bu telefonun her radyoyu duyduğu nokta.
- Ayarlar konu listesi olarak açılır. O sayfa için bir satıra dokunun. Satır geçerli seçimi gösterir. Geri listeye döner. Adlandırılmış radyolar, İzleme listesinden sonra kendi satırıdır. Satır kaç tane kaydedildiğini gösterir.

- Bir Filtreler satırı, Ayarlar ile aynı soluk metinde neyin seçildiğini adlandırır. Bu satır yeşil değildir.
- Oturum listesi biraz daha sıkı aralıklıdır.
- İmzalar sayfası Uyarı için yer imi ekle der. Filtreler üzerinde bir aileyi gizleme satırı kaldırılmıştır.
- Oturumlar satırı, Radyolar adlandırılmış bir zaman dilimi boyunca duyuldu der. Oturum başlat altında Aşağıdaki eylemler için Oturum seç der.
- Sizinle hareket ediyor, Sizinle kalan yüksek sesli Bluetooth radyoları der.
- Ön ayarlar, bir ön ayarı yüklemek için dokunun, silmek için uzun basın veya geçerli filtre ayarlarını yeni bir ön ayara kaydedin der.
- Seçili imza sınıfları, Yalnızca göster veya Bunları gizle seçin, sonra sınıfları seçin ve bir ön ayarın bu seçimleri içerdiğini söyler.
- Seçili imzalar, Yalnızca göster veya Bunları gizle seçin, sonra imzaları seçin ve bir ön ayarın bu seçimleri içerdiğini söyler.
- İmzayı düzenle, Notlar altındaki son cümleyi ve Ekstra dikkat altındaki son cümleyi kaldırır.
- İmzayı düzenle, sınıfın Filtreler'in Yalnızca göster veya Bunları gizle için kullandığı şey olduğunu söyler.
- İmzayı düzenle ve Alanları çöz; Min eşler, renk, kurallar, varsayılanları geri yükle, bir çözüm haritasını kaldırma ve boş önizleme için daha kısa, doğru satırlar kullanır.
- Ayarlar → Tanılama, taramanın çalışıp çalışmadığını ve Wi-Fi, Bluetooth, Konum ve GPS durumunu gösterdiğini söyler. Tanılama sayfası artık kopyayı bir issue'ya yapıştırmanızı söylemez.
- Ayarlar alt bilgisi artık Yalnızca Wi-Fi ve Bluetooth demez.
- Canlı tur, sağ üstteki kaydırıcıları gösterir. Aç göster, Canlı'nın nasıl göründüğünü gösterir. Atla turu kapatır. Bu sürüme yükseltme, o kartı ilk Canlı ekranında bir kez gösterir. Ayarlar → Canlı turu göster onu geri getirir.
- Dil listesi, her dilin İngilizce adını alfabetik sırayla kullanır. Varsa telefonun yerel ayarını kullan ilk sırada kalır.
- Kullanıcı kılavuzu Dil'i açıklar: paketlenmiş taslaklar AI ile çevrildi, yanlış bir satır GitHub issue'sunda olmalı ve yeni bir dil yazarın kendi deposundaki bir dosyadır. Yazar kılavuzu o bölümden bağlantılanır.
- Kapalı bir anahtar, yine açılabiliyormuş gibi görünmesi için açık bir topuz tutar. Kullanılamayan bir anahtar soluk kalır.
- Raporlar Oturumlar'ı açık tutar. Yol, Özet, Oturum dışa aktarma, Karşılaştır, Günlük Dışa Aktarma ve İmza adayları her biri kendi sayfasını açar. Her satırın altındaki satır kısa bir açıklamadır. İmza adayları aramayı açıklar ve Adayları bul onu başlatır. Yol, Özet, Oturum dışa aktarma ve Karşılaştır, kullandıkları oturumu adlandıran bir satırın altında, o satırlarla aynı yeşilde bir çubukla yer alır. Günlük ve İmza adayları o grubun altında tam genişlikte kalır.
- Tut veya gizle; İmza eşleşmelerini yalnızca tut, Yalnızca izlenenleri tut ve Yalnızca adlandırılanları tut olmak üzere üç tut anahtarını adlandırır. Radyolarımı gizle, Benim'i Gizle'dir.
- Filtreler, üstte Ön ayarlar ve Radyolar'ı açık tutar. Sizinle hareket ediyor, Birden fazla yerde görüldü ve Yeni algılamalar o listedeki anahtarlardır. Tut veya gizle, Seçili imza sınıfları, Seçili imzalar ve Sinyal, ad, MAC, satıcı kendi sayfasını açar. Satır o bölümde neyin seçildiğini adlandırır.
- Seçili imzalar tek bir listedir. Yalnızca göster ve Bunları gizle, Seçili imza sınıflarının çalıştığı şekilde üstünde yer alır. Bir çipi kapatmak seçimleri korur.
- Oturum dışa aktarma bir ATAK veri paketi yazabilir. ATAK zip'i içe aktarır. İçinde bu telefonun yolu, her radyo için bir nokta, bir konum yayınlandıysa bir hava aracı pini ve kısa izi, o konum yayınlandıysa bir operatör pini ve yolda bir pin olarak GNSS vuruşu vardır. Elips ve taşmalar canlı akışta kalır.
- Her telefon kendi TAK işaretçisini alır. Ad, siz bir ad yazmadığınız sürece Fieldwatch artı 4 karakterlik bir etikettir. Aynı ağdaki iki telefon artık o işaretçiyi paylaşmaz. UAS ID'si olan bir Remote ID hava aracı hâlâ tek bir paylaşılan işaretçidir. Bu yön bulma değildir.
- Ayarlar → GNSS girişimi, bir vuruş çevresinde telefonun ham GPS ölçümlerini kaydedebilir. Anahtar siz açana kadar kapalıdır. Son kaydı paylaş o sayfadadır. Gizlilik modu kaydetmez.

## 1.1.26 — 12 Ekim 2026

- Bir Remote ID operatör konumu o noktanın ne olduğunu söyler. Kalkış, fırlatma noktasıdır. Pilot, canlı bir GPS operatörüdür. Sabit, hava aracının bildirdiği bir noktadır. Daha eski bir oturum Operatör der. Pin Turuncu kalır. Bilinen bir operatör irtifası gösterilir. Bilinmeyen boş kalır. Kart, hava aracı yüksekliğinin kalkışın üzerinde mi yoksa yerin üzerinde mi olduğunu söyleyebilir. AB kategorisi ve sınıfı yalnızca plaka sınıflandırmanın AB olduğunu söylediğinde gösterilir.
- Ayarlar, daha uzun GNSS işaretini elips olarak adlandırır. Kısa bir vuruş hâlâ pindir. Daha uzun bir vuruş, başlangıçtan son yere kadar, uzunluğunun yarısı genişliğinde tek bir elipstir.
- Kullanıcı kılavuzu, GNSS girişimi altında bir vuruşun nasıl kararlaştırıldığını açıklar.

## 1.1.25 — 11 Ekim 2026

- Bir GNSS vuruşu, bu telefonun bulunduğu yerde ATAK haritasına bir işaret koyabilir. Kısa bir vuruş pindir. Vuruş sürerken telefon hareket etmeye devam ederse işaret, başladığı yerden son duyulduğu yere kadar, uzunluğunun yarısı genişliğinde bir oval olur. Kelimeler ayrıca bu telefonun Fieldwatch işaretçisi üzerinde kalır. İşaret nedenin nerede olduğunu söylemez.
- Bu işaretin ne kadar kaldığı bir ayardır: 1 saat, 6 saat, 24 saat veya silinene kadar. Varsayılan 1 saattir. Silinene kadar, TAK üzerindeki GNSS kapatılana kadar kalır.
- TAK üzerindeki bir radyo noktası, radyo ayrıldıktan sonra adını korur. Bir noktanın ne kadar kaldığı 1 saat, 6 saat, 24 saat veya silinene kadar. Varsayılan 1 saattir. Bu telefonun Fieldwatch işaretçisi hâlâ yaklaşık her 2 dakikada bir yenilenir. Beslemeyi kapatmak veya Gizlilik modunu açmak bu radyo noktalarını haritadan kaldırır. Ovale dönüşen kısa bir GNSS pini arkasında bir Fieldwatch noktası bırakmaz.

## 1.1.24 — 10 Ekim 2026

- Üst çubuktaki simgeler Wi-Fi, Bluetooth ve imzaların sağlıklı olup olmadığını gösterir. Yeşil, Wi-Fi taramaları arasındaki bekleme ve planlı bir Bluetooth dinlenmesi dahil o bölümün çalıştığı anlamına gelir. 0 imza sayısı yeşil kalır. Gri, taramanın durdurulduğu anlamına gelir. Soluk gri, o radyonun kapalı olduğu anlamına gelir. Kırmızı, o tarama çalışırken Konum'un kapalı olduğu veya Android'in onu reddettiği anlamına gelir. Simgelerden sonraki kelimeler ikincil metin renginde kalır. Gece modu renkleri kırmızı ekrana katlar.
- GNSS girişim denetimi açıkken o çubukta numarasız bir GPS işareti durur. Denetim hazır ve sessizken yeşil. Hâlâ yerleşirken veya öğrenirken, telefon GPS'i duraklatırken, bu telefon Zayıf derecelendirildiğinde veya tarama durdurulduğunda gri. Bir vuruş sürerken kırmızı. Bir duraklama gri kalır.
- Daha hızlı Wi-Fi AP taramaları, Geliştirici seçenekleriyle eşleşir. Anahtar yalnızca Wi-Fi tarama kısıtlaması kapalıyken açıktır. O sayfayı açmak için dokunun. Normal bekleme yerine yaklaşık her 8 saniyede bir. Fieldwatch bu anahtarı sizin için değiştiremez.
- Pencere telefonun tam yüksekliğini kullanır, böylece üst çubuk, liste ve sekmeler onları boş bırakan telefonlarda yine çizilir.

## 1.1.23 — 9 Ekim 2026

- GPS duraklaması girişim değildir. Uydular ve kazanç birlikte kaybolursa veya telefon alıcının durduğunu bildirirse, Canlı GNSS telefon tarafından duraklatıldı der. Açılır pencere, kırmızı çizgi veya TAK satırı yoktur. Denetim, GPS döndükten sonra bir düşüşü izlemeye başlamadan önce birkaç saniye bekler. Gerçek bir düşüş hâlâ uydular izlenirken bir kazanç değişimidir.

## 1.1.22 — 9 Ekim 2026

- Katalog 94. Flipper Zero ayrıca resmi aygıt yazılımı hizmetleri 3080–3083 ile eşleşir, böylece yeniden adlandırılmış resmi bir birim yine eşleşir. Tile ayrıca etkinleştirme öncesi hizmet olan FEEC ile eşleşir. Polar yeni bir Giyilebilir satırıdır: şirket 0x006B, hizmet FEEE veya Polar ile başlayan bir Bluetooth adı. GoPro kalp atış hızı hizmetini de gönderen bir Polar kayışı Polar'da kalır.
- Bir GPS uyarısı, yalnızca Ayarlar → GNSS girişimi → Sistem bildirimi açıkken telefon bildirimi gönderir. Bu anahtar siz açana kadar kapalıdır ve izleme listesi anahtarından ayrıdır. Açılır pencere, kırmızı çizgi, bip sesi ve sesli okuma değişmez.
- Kalibrasyondan sonra Ayarlar Kalibrasyon tamamlandı der ve bu telefonu İyi, Orta veya Zayıf olarak adlandırır. İyi, denetimin gökyüzünü net gören bir yerde, diğer elektroniklerden uzakta çalışması gerektiğini söyler.
- GPS açılır penceresi neyin fark edildiğini ve nedenini sade sözlerle söyler. Alıcı numaraları bundan sonra Ayrıntılar altında gelir. Kırmızı çizgi, oturum ve yol notu daha kısa teknik satırı korur.
- Bir saat uyumsuzluğu, konum uyumsuzluğu veya seyahatten daha hızlı bir sıçrama tek başına uyarmaz. Bunlar bir kazanç düşüşüyle veya birbirleriyle birlikte sayılır. 100 m veya daha kaba bir ağ sabitlemesi sayılmaz. Merkezlerin açıkça ayrı olması ve uyumsuzluğun sürmesi gerekir.
- Bu telefon bir yürüyüşten daha hızlı hareket ederken ve patlama yaklaşık -80 dBm veya daha zayıfken bir eşleştirme veya ad taşması sessiz kalır. Yüksek bir patlama herhangi bir hızda yine uyarır. Durmak veya yürümek herhangi bir ses yüksekliğinde yine uyarır. Bir Wi-Fi işaretçi taşması değişmez.
- TAK / CoT, bir taşma algılandığında taşma bitene kadar bu telefonun işaretçisine bir taşma notu ekleyebilir. Siz Açık seçene kadar kapalıdır. Ayrı bir pin değildir ve Canlı üzerindeki kırmızı çizgiyi değiştirmez. Eşleştirme reklamı yapan radyolarla dolu bir mağaza buna neden olabilir. Not bunun tek bir radyo olduğunu söylemez.
- GNSS denetimi başladıktan sonraki ilk dakikayı yok sayar. Bu okumalar temel çizgi değildir. Ardından yaklaşık bir dakika öğrenir ve bundan sonra bir uyarı gelebilir. Bu telefon için kaydedilmiş kalibrasyon hâlâ geçerlidir.
- Bir GNSS algılaması, Raporlar → Yol üzerinde bu telefonun bulunduğu yerde kırmızı bir elmas olarak görünür. Haritanın altındaki not ile Özet ve Karşılaştır bölümü zaman, seviye ve neyin değiştiğini içerir. Elmas girişimin geldiği yer değildir. GPS sabitlemesi olmayan bir oturum vuruşu yine listeler, elmas olmadan.
- GNSS girişim denetimi, bu telefon kalibre edilene kadar, sonra siz açana kadar kapalı kalır. Bu telefonu kalibre et, dışarıda, yerinde dururken, bir yönlendiriciden uzakta yaklaşık bir dakika sürer. Sonuç siz yeniden kalibre edene kadar bu telefonda kalır ve Ayarları dışa aktar dışarıda bırakılır. İyi, Orta veya Zayıf, denetimin bu GPS üzerinde ne kadar yararlı olacağını söyler. Daha zayıf bir alıcı yine bir yolu etiketleyebilir. Zayıf, açılır pencereyi kapalı bırakır. Fieldwatch tararken bir vuruş bir açılır pencere, sonra Canlı üzerinde kırmızı bir çizgi açar. Özet ve Karşılaştır bunu kaydeder. Sahtecilik denetimleri, ses, hassasiyet ve uyarı veren güven ayrı anahtarlardır. Bu denetim için ses açıktır. Telefonun yanındaki bir Wi-Fi yönlendirici veya başka elektronik bir vuruşa neden olabilir. Fieldwatch kaynağı veya mesafeyi söyleyemez. Tanılama alıcı gerçeklerini ve kalibrasyon derecesini listeler; GPS koordinatlarını içermez. TAK / CoT bu satırı bu telefonun işaretçisine ekleyebilir: Kapalı, Uyarı verirken, Kırmızı çizgi veya Herhangi bir vuruş. Ayrı bir pin değildir.
- Konum kapalıyken Canlı bir başlık gösterir. Aç, o ekran varsa telefonun Konum ekranını açar. Konum kapalıyken Android Wi-Fi veya Bluetooth sonuçları döndürmez.
- Tanılama, o radyo zaten açıkken Wi-Fi tarama ve Bluetooth taramayı adlandırmayı bırakır. Reddedilen bir Wi-Fi taraması veya park edilmiş bir Bluetooth taraması radyonun açık olduğunu söyler.
- Katalog 93. Flock Safety Cameras, B4:1E:52 ve Flock- ile başlayan bir adı tutar. Yalnızca Flock, FLCK, Condor, Falcon veya Sparrow içeren bir ad artık eşleşmez. FS Ext Battery adı ve FS Ext ile başlayan bir adı tutar. Silicon Labs önekleri ve FS_* kaldırıldı. Penguin, XUNTONG üretici kimliğini ve Penguin- ile başlayan bir adı tutar. LiteOn kamera radyosu B8:35:32'yi bırakır. 08:3A:88 kalır. Bu önek Universal Global Scientific Industrial'a aittir, Lite-On'a değil.
- Eşleştirme taşması, Windows arka plan işaretçisini (01 ile başlayan şirket 0x0006) dışarıda bırakır. Swift Pair hâlâ sayılır: işaretçi kimliği 03, bir eşleştirme alt senaryosu ve ayrılmış bayt. Find My dışarıda kalır; sonraki baytları yakınlık eşleştirmesine benzeyen bir Find My reklamı dahil.
- Ayarlar → Tanılama, Ne kontrol edilmeli ile başlar. Kapalı olan ve açık olması gereken bir anahtarı adlandırır. Bu boş bir Canlı listesini açıklamazsa, Kopyala yine sayfayı yapıştırır.
- Sesli uyarılar Android 11 ve üzeri sürümlerde bir konuşma motoruna ulaşabilir. Android 10 zaten ulaşabiliyordu. Telefonun hâlâ indirilen sesi olan herkese açık bir motora, Ses açık olmasına ve medya sesinin açık olmasına ihtiyacı vardır.

## 1.1.21 — 6 Ekim 2026

- Gizlilik modu, oturum raporu yol anahtarında bir Remote ID'yi maskeler: MAC sonu, UAS kimliği ve hava aracı ile pilot koordinatları. İrtifa, rota ve hız kalır. Harita ve noktalı iz yine çizilir. Aynı UAS kimliği Özet, Karşılaştır ve AI Dışa Aktarımı'nın geri kalanında maskelenir. Günlük, oturum dışa aktarma ve GPX/KML/WiGLE dosyaları değişmez.
- WiGLE CSV, ilk boşluk olmayan karakteri =, +, - veya @ olan bir adı, o ad düz bir sayı değilse, oturum CSV ve günlük CSV ile aynı şekilde önekler. RSSI, koordinatlar ve normal bir ağ adı olduğu gibi kalır.
- Ayarlar → Tanılama, Canlı turu göster altında telefonu, Android sürümünü, kataloğu ve Wi-Fi, Bluetooth ile Konum'un tarayıp taramadığını listeler. Ayrıca Daha hızlı Wi-Fi AP taramaları, Arka plan kullanımına izin ver ve Kısıtlanmamış pil değerlerini listeler. Kopyala bu satırları bir issue'ya yapıştırır. Ağ adı ve GPS koordinatı içermez. Boş bir Canlı listesi, bir tarama engellendiğinde orayı gösterir.

## 1.1.20 — 5 Ekim 2026

- Oturum CSV ve günlük CSV, ilk karakteri =, +, - veya @ olan bir hücreyi önekler; böylece bir elektronik tablo ad veya notu metin olarak tutar. Negatif bir koordinat dahil düz bir sayı olduğu gibi kalır. WiGLE CSV değişmez.
- Ayarları içe aktar, TAK / CoT beslemesini açacak veya hedefini değiştirecek bir dosyayı uygulamadan önce sorar. Beslemeyi ve hedefi olduğu gibi bırakan bir dosya yine fazladan adım olmadan içe aktarılır. İptal telefonu olduğu gibi bırakır.
- Katalog 92: LiteOn kamera radyosu 48:27:EA (Samsung) ve 82:6B:F2 (yerel bir adres, fabrika bloğu değil) düşürür. F8:A2:D6 kalır. Ray-Ban / Meta glasses ayrıca Meta RB Display ile başlayan bir Bluetooth adıyla eşleşir. Axon notları vücuda takılan veya sabit ALPR der. Bu genel adres öneki vücut kameraları ve sabit okuyucular tarafından paylaşılır. Remote ID, ID türü seri olduğunda 1748C ile başlayan bir seriden Autel'i, 1668B ile başlayan bir seriden Skydio'yu adlandırır. Daha kısa bir önek o adı almaz.

## 1.1.19 — 4 Ekim 2026

- Katalog 91: DJI Power, Power2000 ile başlayan bir Bluetooth adıyla eşleşir. Bu bir güç istasyonudur, Ev IoT'dur ve yer imli değildir. Osmo kameralar Osmo satırında kalır. Bir DJI Power vuruşu DJI drone satırını düşürür. Diğer DJI radyoları DJI'da kalır. Model kimliği 4500, Power 2000 olarak okunur. Satırı seçen addır.
- Atrius sepet etiketi, o iBeacon UUID'sinin adıdır. Reklam mağazayı adlandırmaz, bu yüzden satır artık Target demez.
- Bir ad taşması rastgeleleştirilmiş Bluetooth adreslerini sayar. Kararlı adı olan bir fabrika adresi o sayının dışında kalır. Eşleştirme açılır pencereleri hâlâ her adresi sayar. Daha küçük bir eşleştirme açılır penceresi kümesi sessiz kalır.
- Eşleştirme taşması iletişim kutusu, patlamanın mağazadaki gibi zaten eşleştirme reklamı yapan birçok radyo olabileceğini ya da her pakette adresini değiştiren tek bir radyo olabileceğini söyler. Bir ad taşması mağazadaki etiketler veya adını ve adresini değiştiren tek bir radyo olabilir. Devam onları Canlı'da bırakır. Bunları gizle onları Canlı'dan alır. Oturum ve günlük yine onları tutar. Reklam aracı adlandırmaz.
- Bir oturum sırasında Devam veya Bunları gizle oturum bitene kadar tutulur. İlk patlama yine sorar. Daha sonraki patlamalar kırmızı çizgiyi korur ve iletişim kutusunu açmaz. Bunları gizle ayrıca o oturumdaki daha sonraki patlamaları Canlı'dan alır. Oturumu bitirmek yeniden sorar. Açık oturum yokken seçim yaklaşık 15 dakika tutulur ve kaymaz. O süredeki daha sonraki bir patlama kırmızı çizgiyi korur. 15 dakika sonra sonraki patlama yeniden sorar. Bu tutma sürerken bir oturum başlatmak yanıtı oturum bitene kadar korur. Eşleştirme ve ad taşmaları yanıtı paylaşır. Bir Wi-Fi işaretçi taşması kendi başına bir kez sorar.

## 1.1.18 — 3 Ekim 2026

- Canlı, birçok yeni Bluetooth adresi birkaç saniye içinde yaklaşık aynı ses yüksekliğinde bir eşleştirme açılır penceresi reklamı yaptığında veya birçok yeni ad yayınladığında uyarır. Tek bir iletişim kutusu, sonra o patlama sessizleşene kadar tek bir satır. Reklam aracı adlandırmaz.
- Bir oturum sırasında eşleştirme veya ad taşması, Özet ve Karşılaştır üzerinde sessiz bir Taşma satırıdır: zaman, tür, kaç yeni adres ve karşılaştırmada hangi oturum. Bu adresler radyo sayılarından ve listelerinden dışarıda bırakılır. Satır kaç tanesinin ayrıldığını söyler. Oturum dosyası ve günlük yine onları tutar. Adresler saklanmadan önce kaydedilmiş bir oturum yine onları diğer radyolarla sayar. Not, canlı uyarı göründüğünde kaydedilir.
- Canlı taşma satırındaki Bu patlamayı gizle, o patlamanın yeni adreslerini kendi kendilerine ayrılacakları zamana kadar Canlı görüntüsünden alır. Oturum dosyası ve günlük yine onları tutar. Özet ve Karşılaştır onları radyo sayılarından ve listelerinden dışarıda bırakır. Bu adresler için uyarılar sessiz kalır. Sonraki patlama anahtar kapalıyken başlar.
- Canlı, tek bir taramada birçok yeni Wi-Fi adı göründüğünde, yaklaşık aynı ses yüksekliğindeyken ve sonraki taramada gittiklerinde uyarır. Bir oturumun ilk taraması sessiz kalır. Tekrarlanan bir ad, mesh, genişletici veya misafir ağı sayılmaz. Tek bir iletişim kutusu, sonra tek bir satır, sonra aynı Taşma notu. Bu adresler radyo sayılarından ve listelerinden dışarıda bırakılır. Oturum dosyası ve günlük yine onları tutar. Reklam aracı adlandırmaz.
- Eşleştirme taşması bir Swift Pair işaretçisini (işaretçi kimliği, bir eşleştirme alt senaryosu ve ayrılmış bayt) sayar, böylece Bu patlamayı gizle o yeni Microsoft Device adreslerini kapsar. Nearby Sharing hâlâ kendi reklamından sayılır.
- Eşleştirme taşması bir Samsung Easy Setup kulaklık veya saat reklamını sayar, böylece Bu patlamayı gizle o yeni adresleri kapsar. Yine Samsung SmartTags olarak görünürler. FD5A veya FD59 hizmetini reklam eden bir etiket değişmez.
- Eşleştirme taşması bir LoveSpouse reklamını (şirket 0x00FF ve sabit öneki) sayar, böylece Bu patlamayı gizle o yeni adresleri kapsar. Eşleşmeden kalırlar. Daha kısa bir 0x00FF blobu dışarıda kalır.
- Katalog 89: Even G1 ayrıca Even Realities şirket kimliğiyle eşleşir. RayNeo yalnızca ad RayNeo ile başladığında ve reklam TCL şirket kimliğini kullandığında eşleşir. LiteOn kamera radyosu E0:0A:F6 ve 14:B5:CD ekler, hâlâ Ekstra dikkat yoktur.
- Katalog 90: Remote ID ayrıca Fransız Direct Remote ID satıcı IE'sini etiketler. Konum ve pilot hâlâ ASTM plakasından gelir. Tello, TELLO veya RMTT ile başlayan bir adla eşleşir. Potensic, Holy Stone, Hubsan, Yuneec, SwellPro ve Crazyflie, markayla başlayan bir adla eşleşir. Parrot ayrıca Skycontroller ile eşleşir. Bu drone satırları yer imlidir ve Ekstra dikkatleri yoktur.
- Remote ID, ID türü seri olduğunda ASTM plakasındaki seriden Freefly, BRINC ve Teal'i adlandırır. Satır Remote ID olarak kalır. Bir oturum kimliği ve Fransız plakası bu adı almaz.
- Benim, zaten adlandırabildiğiniz bir radyoyu işaretler. Canlı liste bir Benim çipi gösterir. Benim açıkken o radyo bip sesi çıkarmaz, konuşmaz, yanıp sönmez, titreşmez veya bir kart yükseltmez; yer imli bir imza eşleşse bile. O imzanın diğer radyoları yine uyarır. Özet ve Karşılaştır onu Benim olarak işaretlenenler altında listeler ve birlikte seyahat çağrılarını dışarıda bırakır. Benim'i açmak, gözlemci notlarının yaptığı gibi boş bir özel adı doldurur.
- Filtreler → Kim kalır → Radyolarımı gizle, Benim olarak işaretlenen radyoları canlı listeden alır. Oturum, günlük ve Özet yine onları içerir. Sizinle hareket ediyor'u açmak bu anahtarı açık bırakır. Canlı bunun için bir hatırlatma satırı göstermez.
- Bir Bluetooth şirket adı şirket satırında kalır. MAC öneki listede değilken artık IEEE satıcısı olarak saklanmaz. Yerel biti ayarlı bir adres fabrika adresi olarak adlandırılmaz.
- Ayarlar → Adlandırılmış radyolar, ad satırına Wi-Fi veya BLE işaretini koyar. Özel ad ve MAC her biri tek satırda kalır. Benim ve Uyarı adın altında yer alır.
- Özet ve Karşılaştır sayılarla başlar. PDF sınıf, kanal ve karşılaştırma çubuklarını çizer. Bir radyo; Ekstra dikkat olduğunda, özel adı olduğunda, Benim olarak işaretlendiğinde veya yer imli olduğunda listelenir. Karşılaştır ayrıca değişen bir çözülmüş değeri listeler. Raporlar → Oturum raporu → Tüm radyoları göster tam listeleri geri getirir. Metin aynı sayılara ve aynı satırlara sahiptir. Oturum dışa aktarma değişmez.

## 1.1.17 — 1 Ekim 2026

- Gizlilik modu artık Raporlar → Yol üzerindeki haritayı veya Özet ve Karşılaştır mektup yol şekillerini gizlemez. Bu döşemeler Çevrimiçi yer adları ve haritaları izler. Gizlilik modu hâlâ MAC sonlarını ve koordinatları maskeler, sokak adlarını dışarıda bırakır ve TAK / CoT beslemesini duraklatır.
- Raporlar → Yol, GPS yolu tek bir sabitleme veya kısa bir oturum olduğunda kısa kenarda yaklaşık 400 m zemin tutar. Daha uzun bir yürüyüş yine çizimi doldurur.

## 1.1.16 — 30 Eylül 2026

- Raporlar → Yol, MAC uyarılarını ve imza uyarılarını, her birini en güçlü duyumda bir kez, sınıf simgesi olarak çizer. Bir sayı bir yerde birkaç tane olduğunu belirtir. Siyah nokta başlangıçtır. Mavi nokta sizsiniz, son noktadasınız. Liste MAC'in yanına Wi-Fi veya BLE simgesini koyar. Haritanın altındaki sembol anahtarı kaldırılmıştır ve uyarı satırları birbirine daha yakındır. Çözülmüş enlem ve boylamı olan bir uyarı, son reklamı yapılan sabitlemede sınıf simgesi olarak çizilir. O karttaki reklamı yapılan iz beyaz noktalı bir çizgidir. Bu simge diğer uyarılarla aynı noktayı paylaşıyorsa sayı onları birlikte listeler. Pilot, haritada kelime etiketi olmayan bir kişi simgesidir. Tek bir sınıf simgesinin sayı kutusu yoktur; o tek radyo için dokunun. Bir sayı hâlâ yalnızca o noktadaki radyoları listeler. 2 km'den uzak bir sabitleme o hava aracının haritasında kalır. Diğer uyarılar en güçlü duyumda kalır. Özet ve Karşılaştır PDF şekilleri o izi siyah noktalı çizgi olarak, son konumda sınıf simgesiyle ve pilot için kişi simgesiyle çizer. Bir karşılaştırmada ikinci oturumun izi mavi noktalı çizgidir. Bu PDF şekilleri aynı MAC uyarılarını ve imza uyarılarını, radyo bir tane gönderdiyse son reklamı yapılan konumda çizer. Yol anahtarı o şeklin altında reklamı yapılan bir hava aracını drone sınıf simgesiyle, artı canlı durumu, UAS kimliği, son konumu, hareketi ve pilot konumuyla listeler. Bir algılamayı kapatan bir başlangıç veya bitiş işareti hâlâ o algılamayı açar.
- Bir çözüm alanı, değerini canlı satırda göstermeyi ve hangi adlandırılmış değerlerin daha güçlü çipi kullandığını isteyebilir. Katalog 85 bunu DULT modu için açar: Ayrılmış öne çıkar; Sahibinin yanında sessiz kalır. Ayrılmış cümlesi o değerdeki katalog metnidir. Eski uygulamalar yeni anahtarları atlar ve paketi yine içe aktarır.
- Özet ve Karşılaştır o canlı etiketi ve katalog cümlesini alıntılar. Ayrılmış bir etiket, dönen adres satırı yerine yaklaşık bir gün cümlesini korur. Karşılaştır, çözülmüş değerin oturumlar arasında değişip değişmediğini söyler. Katalog 86 sahibinin yanında cümlesini ekler. Adlandırılmış bir oturum etiketi saklar, çünkü oturum reklam baytlarını tutmaz.
- Katalog 87: Google Find Hub modu aynı canlı satırı kullanır. Ayrılmış daha güçlü çiptir ve yaklaşık bir gün cümlesini korur. Yakında sessiz kalır; birlikte seyahatin çoğu zaman sizin kendi etiketiniz veya kendi anahtarlarıyla katılan biri olduğu cümlesiyle.
- Katalog 88: Remote ID konum durumu aynı canlı satırı kullanır. Bildirilmedi, Yerde, Havada, Acil durum ve RID hatası hepsi gösterilir. Acil durum daha güçlü çiptir.
- Bir oturum, raporda UAS kimliğiyle birleştirilen kısa bir reklamı yapılan konum izini tutar. Telefon yolunun 2 km içindeki bir iz o haritayı paylaşır. Daha uzaktaki bir hava aracı kendi haritasını alır. Raporlar → Yol, bu izi açık veya kaydedilmiş bir oturumda beyaz noktalı çizgi olarak çizer. Mektup boyutu şekil onu siyah noktalarda çizer. Son 15 dakika geçerli reklamı yapılan konumu işaretler ve iz tutmaz. Bu değişiklikten önce kaydedilen oturumlar tek bir son konumu korur.

## 1.1.15 — 28 Eylül 2026

- Katalog 82: Flock Safety Cameras Ekstra dikkat yalnızca IEEE B4:1E:52 ve Flock / FLCK / Flock-* / Condor / Falcon / Sparrow adlarıdır. LiteOn / modül önekleri LiteOn kamera radyosuna taşınır (Kameralar sınıfı, Ekstra dikkat yok, yer imli değil). UGSI E0:4F:43 bırakılır, böylece bir Ring- SSID'si Flock direği değil Ring olur.
- Oturum dışa aktarma CSV / JSON satırları eşleşen imzaları ve Ekstra dikkat aile adlarını (noktalı virgülle ayrılmış) içerir. Ekstra dikkat true/false kalır. GPX / KML / WiGLE değişmez.
- Adlandırılmış oturum sınırı 6000 benzersiz radyo (eskiden 3000). Adsız BLE hâlâ önce düşer. Düşük bellek kapısı değişmez.
- Özet metin/PDF varsayılan olarak eşleşmeyen dönen BLE'yi envanterlerden gizler. Sayılar, Ekstra dikkat, adlandırılmış imzalar, yer imleri, yük pinleri ve Oturum dışa aktarma yine onları içerir. Raporlar anahtarı: Eşleşmeyen dönen BLE'yi göster.
- Katalog 83: XUNTONG 0x09C8 üretici verisinde Penguin çözümü — yükte MAC ve TN ile başlayan ASCII seri. Kimlik hâlâ şirket kimliği / Penguin* adlarıdır.
- Katalog 84: BLE hizmet verisi FCB2 üzerinde DULT izleyici (IETF Detecting Unwanted Location Trackers). Ağ Kimliği ve sahibinin yanında / ayrılmış çözümü. Ekstra dikkat yok. Chipolo / Pebblebee adları çift etiketlenebilir. Yalnızca FCB2 UUID listesi eşleşmez.
- Wi-Fi Remote ID ASTM mesaj paketleri (satıcı IE FA:0B:BC tür 13), stok Remote ID Alanları çöz haritasının, ayrıntının ve TAK Yük konumunun BLE ile aynı alanları kullanması için BLE FFFA (`0x0D` + sayaç + her 25 baytlık mesaj) olarak çerçevelenir. GitHub kataloğu v2 kalır.
- GitHub'dan stok kataloğunu güncelle: bilinmeyen çözüm kaynakları imzayı tutar ve yalnızca o alan haritasını düşürür. İçe aktarmadan sonra, herhangi bir harita atlandıysa ikinci bir iletişim kutusu daha yeni bir APK ister.

## 1.1.14 — 27 Eylül 2026

- Özet / Karşılaştır PDF yol şekli: Çevrimiçi yer adları ve haritalar açıkken ve Gizlilik kapalıyken OpenStreetMap döşemeleri (Raporlar → Yol ile aynı kapı). Tam genişlikte mektup çerçevesi, kalın yeşil kalır, numaralı Ekstra dikkat (kırmızı) ve yer imli (mavi) vuruşlar. Çevrimdışı veya Gizlilik: yalnızca kuzey yukarı iz.
- Remote ID Konum: yön, OpenDroneID doğu/batı bayrağını kullanır (yön 0–179, o bit ayarlandığında +180); ×2 ölçeği yerine. Yatay hız (`hspeed`), SpeedMult bitiyle çözülür (×0.25 veya ×0.75 + 63.75). Katalog 79. ATAK iz rotası/hızı bu değerleri izler.
- Katalog 80: BLE üreticisi 0x09C8 (XUNTONG), Raven / ShotSpotter'dan Penguin'e taşınır. Bu kimlik Flock harici pilidir, akustik sensör değil. Raven adları, UUID'ler 3100–3500 ve OUI D4:11:D6'yı tutar.
- Katalog 81: Axon `BWCDEVICE`, reklamı yapılan adla değil, BLE hizmet verisinde ASCII (ve bayt ters çevrilmiş) olarak eşleşir. Boş UUID hizmet verisi kuralları o hex'i herhangi bir hizmet yükünde içerir.

## 1.1.13 — 26 Eylül 2026

- TAK / CoT: reklamı yapılan Remote ID hava aracı pinleri, Konum mesajında varsa ATAK iz rotasını ve hızını içerir. Wi-Fi Remote ID (satıcı IE FA:0B:BC tür 0x0D), Konum / Temel ID / Sistem'i BLE FFFA ile aynı şekilde çözer; böylece Yük konumu yalnızca Wi-Fi olan bir drone'u sabitleyebilir. Satıcı IE yükü artık 24 baytta kesilmez.

## 1.1.12 — 26 Eylül 2026

- Google Find Hub etiketleri (FEAA çerçeveleri 40/41). Katalog 78. Eddystone UID/URL/TLM eşleşmeden kalır. Ayrılmış mod bir MAC'i yaklaşık bir gün tutabilir. GitHub güncellemesi `dist/fieldwatch-signatures-v2.json` kullanır; 1.1.11 hâlâ v1 paketini okur (katalog 77).
- Katalog 77 (1.1.11 için zaten GitHub'da): Flock/FS Ext, Espressif ve Silicon Labs OUI'lerini bırakır; Axon TASER/Axon UUID'leri; Meta FEB7/FEB8, Snap FE45, Vuzix; Remote ID Wi-Fi FA:0B:BC ve BLE v0–v2 konum ekleri.

## 1.1.11 — 26 Eylül 2026

- Ayrıntı / paylaşım: RSSI 127, Bluetooth "mevcut değil" demektir, iletim gücü değil. Mevcut, min/maks, kıvılcım çizgisi, Av ve paylaşım metninden çıkarılır.

## 1.1.10 — 26 Eylül 2026

- Yol: Ekstra dikkat ve yer imli radyolar, en güçlü RSSI'de numaralı noktalar olarak. Gözlemci notları yalnızca o radyo yer imliyse Yol üzerinde. Tüm rota boyunca mevcut kaldırıldı. GPS izleri, yalnızca son 40 yerine oturum boyunca yayılmış örnekleri tutar. Yol, GPS sıçramalarını bırakır (gidip dönme sıçramaları veya yaklaşık 150 km/s'den hızlı atlamalar).
- Stok katalog: BLE TPMS. Pazar sonrası sibop kapağı sensörleri (TPMS* / FBB0 / üretici verisi 80–83) basınç, sıcaklık, pil ve alarmı çözer. SYTPMS / BR (ad BR veya UUID 27A5) gösterge basıncı, sıcaklık, pil ve hareketi çözer. Tesla tsTPMS, sensör uyanıkken basınç / sıcaklık / pili çözer. Yeni satırlar: TireCheck, Bluetooth TPMS hizmeti. FOBO ayrıca 00EE hizmetiyle eşleşir. Yalnızca Nokia 0x0001 eşleşmesi değil. Katalog 76.

## 1.1.9 — 25 Eylül 2026

- Yol: çizgi üzerinde kalın yeşil olarak kalır, zaman işaretleri, başlık durak / tüm rota sayıları, Tüm rota boyunca mevcut üzerinde RSSI min–maks. Her Ekstra dikkat / Adlandırılmış radyo en güçlü RSSI'de bir kez çizilir. Tüm rota, ilk/son duyulmayı oturum penceresine göre kullanır (40 örnekli GPS izine göre değil).
- Ayarlar → Çevrimiçi yer adları ve haritalar (varsayılan açık) ayrıca Yol altına OSM döşemeleri yükler. Döşemeler çizim kutusunu doldurur sonra kırpılır, rota çevresinde fazladan harita bulunur. Çevrimdışı, döşeme yok veya Gizlilik modu: yalnızca kuzey yukarı iz, hata yok. Kullanıcı kılavuzu güncellendi.

## 1.1.8 — 25 Eylül 2026

- Raporlar → Oturum dışa aktarma: Oturum raporunun altında kendi kartı, Günlük dışa aktarma ile aynı Biçim ve radyolar çipleri (CSV, JSON satırları, GPX, KML, WiGLE). Dönen günlük değil, seçili oturumdaki (veya son 15 dakikadaki) her benzersiz radyo için bir satır. GPX / KML, bu telefonun yolunu bir iz artı duyum noktaları olarak içerir. Gizlilik modu dosyayı maskelemez. Günlük kartının başlığı Günlük dışa aktarma'dır. Kullanıcı kılavuzu §5.6.2 / §11.6 oturum ile günlüğü açıklar.
- Yol açıklaması: Çizgi = bu telefon kendi satırında; Mavi = Adlandırılmış camgöbeği renginde (Adlandırılmış noktalarla aynı).

## 1.1.7 — 25 Eylül 2026

- Adlandırılmış radyolar: özel adla aynı TÜR+MAC üzerinde Gözlemci notları (en fazla 280 karakter). Ayrıntıda adın altında camgöbeği blok; kaydedilmiş bir özel ad büyük başlıktır, reklamı yapılan ad daha küçüktür. Ayrıntıda veya Ayarlar → Adlandırılmış radyolar üzerinden düzenle. Ad olmadan not kaydetmek yine Adlandırılmış radyo satırı oluşturur (önerilen etiket, Uyarı kapalı). Canlı liste, Ekstra dikkat "!" işaretinin yanında camgöbeği not çipi gösterir. Özet, Nerede olduğunuzdan sonra Gözlemci notlarını listeler; Karşılaştır Pencerelerden sonra. Yol ve AI Dışa Aktarımı duyulan radyoları ve notu listeler. Ekstra dikkat altın renginde kalır. BLE gizlilik adresleri kalemi hâlâ gizler. Ayarlar yedeği notu içerir.
- Özet / Karşılaştır PDF: kalış/geçiş satırları, Kanal doluluğu / En yüksek AP'ler ve diğer "Etiket:" başlıkları kalındır; madde işaretleri ve Yol anahtarı numaraları yapılandırılmıştır.
- Raporlar, Özet, Karşılaştır, Yol, AI Dışa Aktarımı ve GPX/KML'de Adlandırılmış radyolardan gelen özel adı kullanır (reklamı yapılan SSID/LE adı değil). WiGLE CSV hâlâ reklamı yapılan SSID'yi yazar.
- Raporlar → Yol: bu oturumun (veya son 15 dakikanın) kuzey yukarı çizimi. Operatör GPS izi, ölçek çubuğu, Ekstra dikkat / Adlandırılmış noktalar. Yığılmış sayılar tek bir küçük pencere için dokunulur. Harita döşemesi yok. Radyo sabitlemeleri değil, duyum noktaları. Özet PDF ve Karşılaştır PDF, mektup boyutunda operatör yolu şekli içerir (karşılaştırma iki yürüyüşü üst üste bindirir).
- Raporlar → Günlük: Biçim (Günlük dosyası — CSV, Günlük dosyası — JSON satırları, GPX — GPS Exchange, KML — Google Earth, WiGLE CSV — wigle.net) ve radyolar (Her ikisi / Yalnızca Wi-Fi / Yalnızca BLE). Dönen dosya JSON satırlarıdır. CSV / haritalar Paylaş/Kaydet projeksiyonlarıdır. Duyum noktası pinleri bu telefondur. Fieldwatch yükleme yapmaz. Ayarlar CSV/JSON çipleri kaldırıldı.
- Kullanıcı kılavuzu Yol, Karşılaştır, Günlük dışa aktarma, Gözlemci notları, özel adlar ve Canlı not çipi için yeniden yazıldı. Ekran görüntüleri Gizlilik modunda yeniden alındı.

## 1.1.6 — 24 Eylül 2026

- Çözüm alanı sayıları ve radar yakınlaştırması `Locale.US` kullanır; böylece Fransız/Alman telefonlar nokta tutar (`26.48 °C`, `×1.5`). Ayrıştırıcı birim testleri ve push/PR üzerinde GitHub Actions (`testDebugUnitTest` + debug APK).
- Raporlar → Oturumları karşılaştır: bu oturum (açık, seçili veya son 15 dakika) ile ikinci bir kaydedilmiş oturum. Karşılaştır (metin) ve Karşılaştır (PDF) — Özet ile aynı mektup düzeni. Karşılaştır AI Dışa Aktarımı bir ektir (örtüşme, yalnızca bu oturumdaki Ekstra dikkat / Adlandırılmış radyolar), listelerin yeniden yazımı değil. Varlık: yalnızca bu oturumda, yalnızca ikincisinde, ikisinde de. Tür + MAC. Ekstra dikkat ve Adlandırılmış radyolar işaretli. Paylaşım metninde Gizlilik modu.
- Oturum raporu AI Dışa Aktarımı aynı ek biçimindedir: yerleşik Özet olduğu gibi, ardından 5/15 dakikalık oranlar, RSSI bantları, izleme stres testi için Ekstra dikkat ve bulucu etiketi kimlikleri — ikinci bir Wi-Fi/BLE listesi değil.

## 1.1.5 — 24 Eylül 2026

- Ayrıntı "Bu nasıl görünür", genel bir SSID tahmini yerine eşleşen bir katalog ailesini kullanır. Bir `DIRECT-rR-Raven-*` AP'si, Wi-Fi Direct üzerindeki bir telefon veya TV değil, Raven / ShotSpotter sensörüdür.
- Stok **Unknown Signature** yakalayıcısı (`ESP_*`, `ANDROID-`, `DIRECT-`, `UNIT-`) kaldırıldı. Bu adlar bir ürün ailesi değildi ve gerçek satırları (Raven, Roku, Epson) çift etiketliyordu. Genel `DIRECT-` SSID'leri eşleşmeden kalır; tahmin hâlâ Wi-Fi Direct diyebilir.
- Ayrıntıdaki özel ad, yerel olarak yönetilen BSSID'ler (araç / mesh / misafir AP'leri) dahil Wi-Fi için her zaman kullanılabilir. BLE gizlilik adresleri kalemi hâlâ gizler. Kimlik kopyası artık bir Wi-Fi yerel-bit BSSID'sini dönen gizlilik MAC'i olarak adlandırmaz.
- Stok Ekstra dikkat: Digital Ally vücut/araç içi (IEEE 00:23:BD); Limitless, Bee, Omi ve Friend giyilebilir kaydediciler (benzersiz BLE hizmetleri / adları); Brilliant Frame ve Even G1 gözlükler; Reveal Media ve Wolfcom vücut kameraları; Panasonic i-PRO / Arbitrator; Hayden AI, Miovision, Tattile ve LVT LiveView (yalnızca ad — hücresel birimler sessiz kalır).
- Stok filtre çipleri: Tüm trafik, Yalnızca Wi-Fi, Yalnızca BLE, Güçlü sinyal, Sizinle hareket ediyor, Yalnızca izlenenler. İzleyiciler / İzleyicileri gizle / Telefonları gizle stok setinden çıktı (sınıf çipleri + Geçerli olanı kaydet... hâlâ bu oturumları oluşturur). Bir stok adı veya filtreyi yineleyen mevcut özel çipler yükseltmede katlanır.
- Kullanıcı kılavuzu Bölüm 14 Teknik özellikler / Nasıl çalışır (Şek. 20).

## 1.1.4 — 21 Eylül 2026

- Biraz daha küçük anahtarlar. Çerçeveli alanlar ve açılır listeler aynı sıkı iç dolguyu paylaşır (Görüntüle, imza düzenleyici, Çöz, Filtreler, Ayarlar TAK, oturum/ad iletişim kutuları). Kural Tür/Değer ve Üretici verisi alanları artık üst üste binmez.
- Görüntüle'yi açmak Canlı'yı soldurur ve arkasındaki radyolara dokunmayı engeller. Kapatmak için soluk alana dokunun.

## 1.1.3 — 21 Eylül 2026

- Canlı Ayar (Görüntüle), radar/listeyi aşağı itmek yerine üzerine yerleşir. Panel başlangıçta daraltılmış kalır. Dikeyde sekme çubuğunun üzerindeki yüksekliği kullanır; yatayda kaydırılır, aşağıda daha fazla seçenek varsa bir solma ve aşağı ok gösterir.
- Daha sıkı FIELDWATCH başlığı, Filtreler/İmzalar alt başlık çubuğu ve alt sekme çubuğu.
- Gece modu Görünüm altındadır. Koyu tema artık bir anahtar değildir — ekran her zaman koyudur. Koyu tema kapalıyken yapılan bir yükseltme veya ayar içe aktarma zorla açılır.

## 1.1.2 — 21 Eylül 2026

- Stok imza: BlueTOAD Spectra (Iteris Vantage Velocity / Spectra CV yol kenarı Bluetooth seyahat süresi okuyucu). Gözetim sınıfı. BlueTOAD / Vantage Velocity / Spectra CV adında veya Iteris OUI `00:14:7B` üzerinde etiketler. Ekstra dikkat yok ve stok yer imi değil — sessiz kabinler ve 5.9 GHz C-V2X görünmez.
- Stok imzalar: BlipTrack (seyahat süresi, bip yok); Hanwha Wisenet, Uniview, Rhombus (kameralar, Ekstra dikkat); MeshCore, goTenna, SenseCAP, RAK WisGate (mesh, bip yok); GhostESP ve Bruce (pentest Ekstra dikkat, yalnızca GhostNet / BruceNet). Mevcut telefonlar artık Geri Yükle olmadan yeni Ekstra dikkat yer imlerini alır (GhostESP, Bruce, Hanwha, Uniview, Rhombus).
- Kilitler sınıfı artık Erişim kontrolü olarak etiketlenir. ASSA ABLOY, SALTO, dormakaba ve Paxton, Gözetim'den (kapı okuyucular, kamera değil) oraya taşınır. Saklanan sınıf değeri hâlâ LOCK'tur.
- Ayarlar alt bilgisi Katalog N gösterir. GitHub'dan stok kataloğunu güncelle, depo JSON'undan stok satırlarını (Ekstra dikkat dahil) değiştirir; yer imleri ve Ayarlar kalır. İnternet gerekir. Çevrimdışı: İmzaları içe aktar.

## 1.1.1 — 20 Eylül 2026

- Raporlar → Oturumlar: oturumun ne olduğuna ve Oturum raporunun açık oturumu, seçili kaydedilmiş oturumu veya son 15 dakikayı kullandığına dair kısa bir not.

## 1.1.0 — 19 Eylül 2026

- Adlandırılmış oturumlar. İsteğe bağlı: Raporlar → Oturum başlat. Özet ve AI Dışa Aktarımı, RAM'deki son 15 dakika yerine o pencereyi kullanır. Hiç başlatmazsanız Canlı liste, Filtreler, Av ve TAK değişmez.

## 1.0.8 — 19 Eylül 2026

- TAK açıklamaları, bir işaretçiyi incelediğinizde kısa bir karttır: çağrı işareti, radyo türü, MAC, RSSI, burada duyuldu / reklamı yapıldı / pilot, imzalar, Ekstra dikkat. Harita etiketi hâlâ 32 karakterlik çağrı işaretidir.

## 1.0.7 — 19 Eylül 2026

- TAK burada duyuldu pinleri, operatörü izlemek yerine en yüksek duyumu (en yakın yaklaşım) tutar. Daha zayıf bir duyum, ATAK işaretçiyi düşürmesin diye aynı enlem/boylamı yaklaşık her 10 saniyede bir yine yeniler. Reklamı yapılan Remote ID / pilot pinleri hâlâ yükü izler. Yön bulma değildir.

## 1.0.6 — 19 Eylül 2026

- Radar taraması ekran yenilemesinden bağımsız çalışır; böylece Geliştirici seçeneklerinde Animatör süre ölçeği kapalıyken bile döner. İz, ışından uzaklaşarak solar; temaslar tarama onları boyadığında parlar.
- Yeni kurulumlar / Geri Yükle: Canlı görüntü Sınıfa göre olur. RSSI çubukları, İmza adları, Frekans ve İlk / son görülme açıktır. Mevcut telefonlar zaten seçtikleri görünümü korur.

## 1.0.5 — 18 Eylül 2026

- Yan yükleme APK'sı Android debug sertifikasıyla değil, Off Grid Pete LLC sürüm sertifikasıyla imzalanır. Sertifika SHA-256 `instruction.txt` içindedir. 1.0.4 veya daha eski sürümü zaten kurulu olan telefonlar önce kaldırmalıdır; Android farklı imzalayan üzerinden güncellemez.

## 1.0.4 — 18 Eylül 2026

- Kullanılmayan `RECEIVE_BOOT_COMPLETED` kaldırıldı. Fieldwatch hiç açılışta başlamıyordu; tarayıcılar alıcısı olmayan bir izni işaretliyordu.

## 1.0.3 — 17 Eylül 2026

- TAK / CoT: Remote ID, hareket eden tek bir hava aracı işaretçisini tutar (dönen BLE MAC'i değil, yapışkan UAS ID). Çözülmüş pilot enlem/boylamı, hava aracına bağlı ikinci bir pindir.
- Burada duyuldu çağrı işaretleri (here) ile biter; Ekstra dikkat Bordo, reklamı yapılan drone'lar Sarı, pilot Turuncu kullanır. Ayrılan radyolar yaklaşık 120 saniye beklemek yerine ATAK'tan düşürülür.
- Ayarlar Besleme durumu, akıştaki pinleri ve bu tikteki gönderimleri, artı hedef, hata ve zamanı gösterir. Hedef çipleri: Bu telefon (`127.0.0.1:10011`), LAN multicast (`239.2.3.1:6969`), Özel. Yalnızca UDP — bir TAK sunucusunun TCP 8087'si bu besleme değildir.
- Yeni kurulumlar / Geri Yükle: İzlenen imzada ses açık; Ne söylenecek Sınıf + imzadır. Koyu tema, Ekranı açık tut, Yeni izlenen algılamaya atla ve Bip zaten açıktı.
- Stok yer imleri Ekstra dikkat içerir (Ekstra dikkat metni olan her Gözetim satırı dahil) artı yerleşik her Drone sınıfı satırı (DJI, Remote ID, Skydio, Autel, Parrot, HOVERAir). Mevcut telefonlar, Varsayılanları geri yükle yapmadığınız sürece mevcut Ayarlarını ve izleme listesini korur.

## 1.0.2 — 16 Eylül 2026

- Ayarlar yedeği: Ayarları dışa aktar / Ayarları kaydet / Ayarları içe aktar. Adlandırılmış radyolar, filtre ön ayarları ve Ayarlar anahtarları; katalog, günlükler veya GPS değil. Tamamlandı ve hata bir Tamam iletişim kutusu gösterir.
- İmzaları içe aktar aynı Tamam / hata iletişim kutularını kullanır.
- Alt sekmeler hemen keser (700 ms solma yok).

## 1.0.1 — 15 Eylül 2026

- Sizinle hareket ediyor yalnızca BLE'dir. Wi-Fi erişim noktaları dışarıda kalır (yanından geçtiğiniz yüksek sesli bir AP yolunuzu boyar). Filtreler, bu anahtar açıkken Yalnızca BLE gösterir.

## 1.0.0 — 15 Eylül 2026

- Yeni uygulama: Fieldwatch (`app.fieldwatch`). Spectre'ın yanına yan yüklenir; veriler taşınmaz.
- Fieldwatch kaynak kodu için MIT Lisansı. Apache-2.0 kütüphaneleri ve IEEE / Bluetooth SIG arama tabloları: NOTICE dosyasına bakın.
- Operatörün gördüğü ad Fieldwatch'tur (başlatıcı, bildirim, Özet, TAK, ilk çalıştırma).
- İmza dışa aktarma `fieldwatch-signatures` kullanır. Spectre paketleri (`spectre-signatures`) hâlâ içe aktarılır.
- Spectre 1.2.14'ü içerir: Android 12–14 ilk BLE reklamında artık çökmez; Android 15 hâlâ yığından Public / Random gösterir. Yan yükleme APK'sı debug derlemesi değildir. BLE taraması başlangıçta Wi-Fi'den yaklaşık yarım saniye sonra başlar.
