# Arduino Tabanlı Akıllı Saksı

Akıllı saksı, özellikle bitki yetiştirme sürecinde elle müdahaleyi minimuma indirmek ve bitkilerin ideal koşullarda büyümesini sağlamak için tasarlanmış bir sistemdir. Bu sistem ile internet üzerinden bitkilerin ışık seviyesi, toprak nemi, hava sıcaklığı ve nem gibi çevresel koşullarını anlık olarak izleyebilirsiniz.

## Donanım Bileşenleri
Proje aşağıdaki donanımları kullanmaktadır:

1. Arduino Uno R3: Sistemin beynini oluşturan mikrodenetleyici kartı. Sensörlerden gelen verileri işler ve diğer modülleri kontrol eder.
2. DHT11 Sıcaklık ve Nem Sensörü: Havanın sıcaklık ve nem değerlerini ölçerek verileri Arduino'ya iletir.
3. LDR (Light Dependent Resistor) Sensörü: Ortamdaki ışık seviyesini ölçer.
4. Kapasitif Toprak Nem Sensörü v1.2: Toprağın nem seviyesini ölçerek bitkinin sulama ihtiyacını belirler.
5. ESP8266 Wi-Fi Modülü: Verileri internet üzerinden uzaktan erişilebilir hale getiren Wi-Fi bağlantısını sağlar.
6. Mini Dalgıç Su Pompası: Gerekli durumlarda otomatik sulama işlemi gerçekleştirir.
7. Saksı: Sistemin fiziksel altyapısını sağlayacaktır.

## Yazılım Bileşenleri
Projenin yazılım tarafında kullanılan bileşenler şunlardır:

1. Arduino IDE: Mikrodenetleyici programlama için kullanılır.
2. Bootstrap 5.3: Web arayüzü tasarımında modern ve şık bir kullanıcı deneyimi sağlar.
3. Chart.js: Grafiksel verilerin görselleştirilmesinde kullanılır.
4. HTML, CSS ve JavaScript: Web sitesinin temel yapı taşlarıdır.
5. ThingSpeak: Verilerin internet üzerinden alınmasını ve API ile web siteye entegre edilmesini sağlar.

## Projenin İşleyişi

1. Veri Toplama
- DHT11 Sensörü havanın sıcaklık ve nem değerlerini ölçer.
- LDR Sensörü ortam ışığını ölçerek bitkinin ne kadar ışık aldığı bilgisini sağlar.
- Toprak Nem Sensörü, toprağın sulama gereksinimini belirlemek için nem seviyesini ölçer.
- Tüm sensörlerden alınan veriler, Arduino tarafından işlenir ve anlamlı hale getirilir.

2. Verilerin İnternet Üzerinden Erişimi
- Sensörlerden alınan veriler, ESP8266 Wi-Fi Modülü sayesinde ThingSpeak'e yüklenir.
- ThingSpeak, bu verileri bir kanal içinde saklar ve gerektiğinde API üzerinden veri çekilmesine olanak tanır.

3. Web Arayüzü ile Görselleştirme
- Web arayüzü, kullanıcıların sensörlerden gelen verileri gerçek zamanlı olarak takip edebilmesine olanak sağlar. 
- Grafikler: Işık seviyesi, sıcaklık, nem ve toprak nem değerleri çizgi grafikleriyle görselleştirilir. Kullanıcılar, bu grafiklerden çevresel değişiklikleri kolayca analiz edebilir.
- Kutucuklar: En son alınan veriler, özet bir şekilde kutucuklarda gösterilir.

## Projenin Kullanım Alanları
Bu proje birçok farklı alanda kullanılabilir:
1. Ev Bitkileri Yetiştiriciliği: Özellikle yoğun yaşam temposuna sahip bireyler için bitki bakımını kolaylaştırır.
2. Seralar ve Tarım: Büyük ölçekli tarım veya seralarda çevresel verilerin kontrolü ve otomasyonunu sağlar.
3. Eğitim: Arduino ve sensör teknolojilerini öğrenmek isteyen öğrenciler için mükemmel bir başlangıç projesidir.
4. Nesnelerin İnterneti (IoT): IoT uygulamaları geliştirmek isteyen mühendisler veya geliştiriciler için iyi bir örnek oluşturur.

## Avantajlar
- Zamandan Tasarruf: Kullanıcıların bitki bakımına harcadığı zamanı azaltır.
- Doğru Verilerle Karar Verme: Bitkinin ihtiyaçlarını anlık verilerle belirleyerek doğru müdahalelerde bulunmayı sağlar.
- Uzaktan Kontrol ve İzleme: Kullanıcı, istediği yerden bitkisini kontrol edebilir.
- Özelleştirilebilirlik: Kullanıcı ihtiyaçlarına göre sistem kolayca genişletilebilir.
