# Fieldwatch

[![RSI-1 imzaları desteklenir](https://raw.githubusercontent.com/OffGridPete/radio-signature-interchange/main/badges/RSI.svg)](https://github.com/OffGridPete/radio-signature-interchange)

Fieldwatch'u, telefonumun algılayabildiği Wi-Fi erişim noktalarını ve Bluetooth LE cihazlarını görmek için kişisel bir araç olarak geliştirdim; böylece çevremde nelerin çalıştığını daha iyi anlayabildim. Tamamen pasiftir ve yalnızca dinler. Dongle yok, hesap yok, arka uç sunucu yok. Sahada çevrimdışı çalışır.

Hedeflerim şunlardı: modern ve kullanımı kolay bir arayüz; esnek, özelleştirilebilir görünümler; yalnızca önemli olanı görmemi sağlayan bir filtreleme motoru; mümkün olduğunca çok radyo kaynağını tanıyabilmem ve anında yenilerini ekleyebilmem için genişletilebilir bir imza kütüphanesi; ve gözlemlenenlerin raporlarını üretebilme.

Bir süredir kullanıp üzerinde geliştiriyorum ve yeterince faydalı olduğu için paylaşmak istedim.

Bu bir hobi projesi — boş zamanlarımda eğlencesine yaptığım bir şey. Fieldwatch arka ucu yok. Reklam yok. Her şey telefonda kalır. Kaynak ve yan yükleme dosyaları bu depodadır (`dist/` içinde APK, talimat kartı ve kılavuz).

Bir hata, saçma bir şey fark ederseniz ya da bir özellik fikriniz varsa — uygulamada ya da belgelerde — lütfen [bu depoda bir issue açın](https://github.com/ptmy53/Fieldwatch/issues). Daha iyisini böyle yapıyoruz. Umarım sizin için de benim kadar faydalı olur. Nasıl gittiğini duymak isterim.

**Sadece kurmak mı istiyorsunuz?** [Fieldwatch.apk](https://github.com/ptmy53/Fieldwatch/raw/main/dist/Fieldwatch.apk) dosyasını indirin. Talimat kartı ve kılavuz: [instruction.txt](https://github.com/ptmy53/Fieldwatch/raw/main/dist/instruction.txt), [Fieldwatch_User_Manual.pdf](https://github.com/ptmy53/Fieldwatch/raw/main/dist/Fieldwatch_User_Manual.pdf). [Yenilikler](CHANGELOG.md), her derleme için değişiklik günlüğüdür. APK adını `Fieldwatch.apk` olarak bırakın. GitHub dosyanın önizleme için çok büyük olduğunu söyleyebilir — bu onların görüntüleyicisidir; İndir'i kullanın.

Fieldwatch'ta çok fazla özellik var. Kapsamlı bir kullanıcı kılavuzu yazdım; uygulamadan en iyi şekilde yararlanmak için [indirmenizi](https://github.com/ptmy53/Fieldwatch/raw/main/dist/Fieldwatch_User_Manual.pdf) öneririm.

**Güncel kalın.** Fieldwatch Play Store'da değil. Kurulduktan sonra, telefon çevrimiçiyken uygulamayı açmak GitHub'da daha yeni bir derleme olup olmadığını kontrol eder. Varsa Fieldwatch sürüm notlarını gösterir. Şimdi güncelle onu indirir. Android yine de kurulumu onaylamanızı ister. Sonra, o derlemeyi daha yenisi yayınlanana kadar bir kenara koyar. Kendiniz bakmak isterseniz Ayarlar'da Güncelleme denetle vardır. [Obtainium](https://github.com/ImranR98/Obtainium) hâlâ https://github.com/ptmy53/Fieldwatch adresini izleyebilir.

**Resmi derlemeler.** Tek resmi Fieldwatch derlemeleri bu depodaki sürümlerdir. Diğer derlemeler ve çeviriler Off Grid Pete LLC tarafından yapılmaz veya incelenmez.

## Telefonda

<table>
  <tr>
    <td align="center" valign="top" width="33%">
      <img src="docs/readme/signatures.png" width="200" alt="Sınıfa göre gruplandırılmış imza kütüphanesi">
      <br><strong>İmzalar</strong>
      <br>250'den fazla imza, sınıflara ayrılmış. Uyarı almak için birini işaretleyin ya da kendinizinkini ekleyin.
    </td>
    <td align="center" valign="top" width="33%">
      <img src="docs/readme/floods.png" width="200" alt="Eşleştirme taşkını uyarısı">
      <br><strong>Bluetooth taşkınları</strong>
      <br>Aynı ses yüksekliğinde yeni eşleştirme adreslerinden oluşan bir patlama. Duyuru aracı adlandırmaz.
    </td>
    <td align="center" valign="top" width="33%">
      <img src="docs/readme/gnss-warning.png" width="200" alt="Olası GPS paraziti uyarısı">
      <br><strong>GPS</strong>
      <br>Bu telefonun GPS'i parazit anlamına gelebilecek şekilde değiştiğinde uyarı. Bunun nereden geldiğini söylemez.
    </td>
  </tr>
  <tr>
    <td align="center" valign="top">
      <img src="docs/readme/trusted.png" width="200" alt="Güvenilir ağlar uyarı anahtarları">
      <br><strong>Güvenilir ağlar</strong>
      <br>İşaretlediğiniz bir Wi-Fi adı daha zayıf, yeni bir üreticiden ya da alışılmış yerlerinden uzakta geri dönerse uyarabilir.
    </td>
    <td align="center" valign="top">
      <img src="docs/readme/cameras.png" width="200" alt="Bilinen kamera listeleri">
      <br><strong>Bilinen kameralar</strong>
      <br>Plaka okuyucular ve diğer sensörlerin kayıtlı listeleri. Bu işaretler, telefonun duyduğu radyolarla birlikte haritada durur.
    </td>
    <td align="center" valign="top">
      <img src="docs/readme/map.png" width="200" alt="Haritada radyolarla canlı yol">
      <br><strong>Canlı harita</strong>
      <br>Telefonun duydukları, yürüdüğünüz yol üzerinde.
    </td>
  </tr>
  <tr>
    <td align="center" valign="top">
      <img src="docs/readme/hunt.png" width="200" alt="Ses yüksekliği ve ısı bulutuyla Hunt ekranı">
      <br><strong>Hunt</strong>
      <br>Bir Bluetooth radyoyu ses yüksekliğine göre yürüyerek bulun. Daha sıcak renk, bu telefonun onu daha güçlü duyduğu yerdir.
    </td>
    <td align="center" valign="top">
      <img src="docs/readme/filters.png" width="200" alt="Filtre ön ayarları">
      <br><strong>Filtreler</strong>
      <br>Listeyi Wi-Fi veya Bluetooth'a, güçlü sinyale, sizinle hareket edene ya da yeni olana daraltın.
    </td>
    <td align="center" valign="top">
      <img src="docs/readme/reports.png" width="200" alt="Bir oturum için raporlar">
      <br><strong>Raporlar</strong>
      <br>Bir oturum; brifing, yol, dışa aktarım ve başka bir oturumla karşılaştırma tutar.
    </td>
  </tr>
  <tr>
    <td align="center" valign="top">
      <img src="docs/readme/cell-warning.png" width="200" alt="Bu telefonun bu konumda daha önce kullanmadığı bir hücreye bağlandığı uyarısı">
      <br><strong>Hücre bağlantısı</strong>
      <br>Bu telefon bu konumda daha önce kullanmadığı bir hücreye bağlandığında uyarı. Bir neden söylemez. Görseldeki sayılar örnektir.
    </td>
    <td align="center" valign="top">
      <img src="docs/readme/drone-swarm.png" width="200" alt="Drone sürüsü algılandı uyarısı">
      <br><strong>Drone sürüsü algılama</strong>
      <br>Remote ID, belirlediğiniz zaman penceresinde yeni dronlar algıladığında uyarır. Drone çevre algılama, Remote ID kullanan bir drone seçtiğiniz mesafenin içindeyken uyarır: 100 m, 250 m, 500 m veya 1 km.
    </td>
    <td align="center" valign="top">
      <img src="docs/readme/tracker.png" width="200" alt="Sizinle ayrılmış etiket uyarısı">
      <br><strong>Takipçi izleme</strong>
      <br>Bir etiket sahibinden uzakta olduğunu söylediğinde, telefonunuz onu 30 dakika boyunca 20 dakikadan uzun boşluk olmadan duyduğunda ve en az 100 m arayla üç yerde duyduğunda uyarır.
    </td>
  </tr>
</table>

Tek telefon. Wi-Fi, Bluetooth LE, bu telefonun GPS'i ve bu telefonun hücre bağlantısı. Harita ve oturum cihazda kalır.

## Teknik makaleler

Bunlar Fieldwatch'un daha uzun yazılarıdır: her birinin ne ölçtüğü ve bir uyarının ne anlama gelmesine izin verildiği. İmza dosyasının kendi deposu vardır. Kullanıcı kılavuzu nasıl yapılır rehberi olarak kalır. Her makale kendi başına okunabilir.

- [Radio signature interchange](https://github.com/OffGridPete/radio-signature-interchange). Fieldwatch, uygulamaların bilinen radyo kütüphanelerini paylaşabilmesi için bu öneriyi kullanır.
- [Wi-Fi ve Bluetooth'u bilinen radyolar için taramak](docs/papers/Fieldwatch_Scanning_and_Signatures.pdf). Radyolarla dolu bir yer ve hâlâ okunabilir kalması gereken bir liste.
- [Taşkın izleme](docs/papers/Fieldwatch_Flood_Monitoring.pdf). Radyo listesi, bir kişinin okuyabileceği liste olmaktan çıktığında.
- [Elinizdeki telefonda GNSS izleme](docs/papers/Fieldwatch_GNSS_Monitoring.pdf). Konum kötüleştiğinde ve bir telefonun bunun hakkında ne söylemesine izin verildiği.
- [Güvenilir ağlar](docs/papers/Fieldwatch_Trusted_Networks.pdf). Wi-Fi listesindeki tanıdık bir ad ve kimse bağlanmadan önce bir taramanın ne söyleyebileceği.
- [Hücre bağlantısı izleme](docs/papers/Fieldwatch_Cell_Connection_Monitoring.pdf). Telefondaki çubuklar ve arkalarındaki hücrenin kaydı yok.

## Güvenlik ve sorumluluk reddi

Bu bir hobi projesidir, MIT Lisansı altında olduğu gibi sunulur. Yapmadan önce bilmeniz gereken birkaç şey:

- Kullanım riski size aittir. Fieldwatch'u kullanmak sizin sorumluluğunuzdadır. Yasaların izin verdiği azami ölçüde Off Grid Pete LLC, kullanımından doğan dolaylı, arızi, özel, sonuçsal veya cezai zararlardan sorumlu değildir.
- Takipçilerin, kameraların, etiketlerin, erişim noktalarının veya başka herhangi bir cihazın bulunacağı, adlandırılacağı veya bildirileceği garantisi yoktur. Kapalı, yalnızca hücresel, uykuda, rastgeleleştirilmiş, sessiz olan ya da bu cihazın işletim sisteminin açığa çıkardığı alanın dışındaki radyolar görünmez. Her telefonun kendi radyoları, bellenimi, tarama kotaları ve OEM pil politikaları vardır. Yazılım bu sınırları aşamaz.
- Desen eşleşmeleri, GPS birlikte hareket ("Sizinle hareket ediyor" / "olası takip"), Debrief dili ve AI Export çıktısı hipotezdir — kimlik, hukuki bulgu veya eksiksiz bir RF yakalaması değildir. Bu uygulamayı ve bu belgeyi nasıl kullandığınızdan ve yerel yasaya uymanızdan yalnızca siz sorumlusunuz. Yazılımı veya bu kılavuzu kullanarak bu şartları ve MIT Lisansı'nı kabul etmiş olursunuz.
- Etiketleme açıksa konum verisi, duyulma anındaki bu telefondur — diğer radyo değil. Fieldwatch sunucusu yoktur. Damgalar siz paylaşana kadar cihazda kalır. Günlükler, Gizlilik modu ekranı ve oturum raporlarını maskeleyse bile tam koordinatları tutar. Debrief, Günlüğü paylaş, AI Export (oturum veya tek radyo) ve radyo detayı Metin olarak paylaş bu yolu telefondan çıkarabilir. Çevrimiçi yer adları, Fieldwatch bulutu değil, sistem coğrafi kodlayıcısını (çoğunlukla OEM / Google ağı) kullanır. Bu dosyaları nasıl sakladığınız, paylaştığınız veya yayımladığınız sizin sorumluluğunuzdadır.

## Telefona kurun

Telefonda kurulum dosyaları deponun kökünde değil [`dist/`](https://github.com/ptmy53/Fieldwatch/tree/main/dist) içindedir:

- [Fieldwatch.apk](https://github.com/ptmy53/Fieldwatch/raw/main/dist/Fieldwatch.apk)
- [instruction.txt](https://github.com/ptmy53/Fieldwatch/raw/main/dist/instruction.txt)
- [Fieldwatch_User_Manual.pdf](https://github.com/ptmy53/Fieldwatch/raw/main/dist/Fieldwatch_User_Manual.pdf)

APK adını değiştirmeyin. `Fieldwatch.apk` dosyasını Dosyalar'dan (veya Dosyalarım) açın. Android isterse o uygulamadan kuruluma izin verin.

| Dosya | Ne olduğu |
|---|---|
| `dist/Fieldwatch.apk` | Yan yükleme APK'sı |
| `dist/fieldwatch-signatures.json` | 1.1.11 GitHub güncellemesi için stok katalog (katalog 77) |
| `dist/fieldwatch-signatures-v2.json` | 1.1.12 - 1.1.44 GitHub güncellemesi için stok katalog |
| `dist/fieldwatch-signatures.rsi` | 1.2.0 GitHub güncellemesi için stok katalog |
| `dist/fieldwatch-sensors.geojson.gz` | Diğer sensörler listesi. OpenStreetMap katkıda bulunanlar, ODbL 1.0. Bkz. `dist/fieldwatch-sensors.txt` |
| `dist/instruction.txt` | İzinler, ilk açılış |
| `dist/Fieldwatch_User_Manual.pdf` | Kullanıcı kılavuzu |
| [`CHANGELOG.md`](CHANGELOG.md) | Her derlemedeki yenilikler |
| `LICENSE` | MIT Lisansı |
| `NOTICE` | Üçüncü taraf atıfları |

Android 10+. APK'yı açmak için kullandığınız uygulamadan kuruluma izin verin. Play Protect, Play'den gelmediği için uyarabilir — beklenen durumdur. Tam adımlar `instruction.txt` içindedir. Android, Fieldwatch tarama yaparken bir bildirim gösterir; böylece ekran kapalıyken tarama sürdürülebilir. Uyarı bildirimlerini reddedip uygulamayı yine de kullanabilirsiniz.

```bash
adb install -r dist/Fieldwatch.apk
```

### 1.0.4 veya öncesinden yükseltme — Fieldwatch artık gerçek bir yayıncı sertifikasına sahip (tek seferlik yeniden kurulum)

Bu sürüm, APK'nın nasıl imzalandığı konusunda biraz daha profesyonel. Android, telefonun "bu güncelleme zaten sahip olduğum uygulamayla aynı yayıncıdan mı?" diyebilmesi için her uygulamaya bir sertifika ekler. 1.0.4'e kadar Fieldwatch, derleme araçlarının sunduğu genel Android geliştirici sertifikasını kullanıyordu. Üzerinde çalışırken bu normaldir; ancak yan yüklenen bir APK'yı tarayan kişiler (ve bazı tarayıcılar) bunu işaretler: herkese açık bir derleme hata ayıklama artığı gibi görünmemelidir. 1.0.5 bunun yerine Off Grid Pete LLC sertifikasıyla imzalanmıştır. Aynı hobi uygulaması; dosyada artık tarayıcıların kontrol edebileceği bir yayıncı adı var. Parmak izini karşılaştırmak isterseniz `instruction.txt` içindedir.

Tek seferlik sorun şudur: Telefon yeni sertifikayı farklı bir yayıncı olarak görür, bu yüzden 1.0.5'i 1.0.4 veya öncesinin üzerine kurmaz. Eski Fieldwatch'u kaldırır, sonra bu APK'yı kurarsınız. Bundan sonra sonraki sürümler aynı sertifikayı kullanır, yani normal güncellemeler yine çalışır. 1.2.2 için kaldırmanız gerekmeyecek.

Kaldırma, telefondaki verileri siler. İmza eklediyseniz, Ayarları değiştirdiyseniz, radyoları adlandırdıysanız veya filtre ön ayarları kaydettiyseniz önce şunu yapın: Ayarlar → **İmzaları dışa aktar** ve **Ayarları dışa aktar**. Bu iki dosyayı sonradan ulaşabileceğiniz bir yere kaydedin/paylaşın. Bunlar günlük değildir ve GPS değildir. Sonra kaldırın (Fieldwatch simgesine uzun basın ya da `adb uninstall app.fieldwatch`), 1.0.5'i kurun, açın, sorumluluk reddinden geçin ve **İmzaları içe aktar** ile **Ayarları içe aktar** kullanın. Hiç özelleştirmediyseniz dışa aktarmayı atlayıp sadece kaldırıp kurabilirsiniz.

## Fieldwatch ne değildir

- Wi-Fi istemcileri, yalnızca probe istasyonları veya 802.11 monitor modu değil
- Bluetooth Classic sorgulaması değil (HC-05 / HC-06 görünmez)
- Hücresel değil
- Yön bulma değil

---

1.2.14'e kadar adı Spectre idi. Daha sonra bu adın başka bir uygulama tarafından kullanıldığını öğrendim, bu yüzden ikisinin karışmaması için adını Fieldwatch olarak değiştirdim. Aynı saha aracı, yeni uygulama kimliği (`app.fieldwatch`), MIT Lisansı. Fieldwatch'u kurmak telefondaki Spectre'u değiştirmez; ayrı bir uygulamadır.

## Telif hakkı ve lisans

Telif hakkı (c) 2026 Off Grid Pete LLC.

Fieldwatch™ Off Grid Pete LLC'nin ticari markasıdır. Tescil beklemededir.

Fieldwatch kaynak kodu [MIT Lisansı](LICENSE) altında lisanslanmıştır. AndroidX, Kotlin ve ilgili kütüphaneler Apache-2.0 olarak kalır. `radiodb.bin` içindeki IEEE ve Bluetooth SIG atanmış numara tabloları bu kuruluşların koşullarına tabidir. Bkz. [NOTICE](NOTICE).
