# AmCache Nedir?
AmCache.hve, program yürütmeleriyle ilgili bilgileri depolamak için oluşturulmuş bir Windows sistem dosyasıdır.Bu dosyadaki yapılar bir soruşturmada büyük bir yardım görevi görebilir; sistemde yakın zamanda yürütülen işlemleri kaydeder ve yürütülen dosyaların yollarını listeler.
Shimcache"e çok benzer şekilde Amcache, bir dosyanın bir sistemde bulunduğunu veya var olduğunu kanıtlamak için kullanılabilir.

* **Amacı, yüklü uygulamalar, sürücüler ve yürütülebilir dosyalar hakkında bilgi sağlamaktır; buna yükleme tarihleri, sürümler vb. dahildir.**
* **Daha yeni Windows sistemleriyle uyumluluk için kullanılır**
* **Adli tıp açısından bakıldığında, bir dosyanın/programın sistemde varlığını göstermek için kullanılır.**
* **Kaydedilmişse bir dosyanın SHA1 karmasını sağlayabilir**
* **Bir dosyanın tam yolunu, son değiştirilme zamanını, yayıncı bilgilerini, boyutunu ve muhtemelen derleme süresini kaydeder**
* **Ayrıştırmak için bir adli tıp aracı gerektirir**
* **C:\Windows\AppCompat\Programs konumunda bulunur Amcache.hve**
  
# AmCache Yapılarının Dijital Adli Tıp Değeri
AmCache eserleri, harici depolama cihazlarının, taşınabilir programların ve adli tıp karşıtı programların izlenmesinin gerekli olabileceği araştırmalar için önemlidir.
Dosyanın içerdiği veriler yürütme yollarını, kurulumu, yürütmeyi, silme zamanlarını ve daha fazlasını içerir.Ayrıca, genel veritabanında bulunan kötü amaçlı programların karmalarıyla karşılaştırmak için kullanılabilecek programların SHA1 karmalarını da saklar.

# Yüklü uygulamaları ve sürücüleri neden önemsiyoruz?
Adli tıp açısından bakıldığında bu bilgiler, kapsam belirleme/avlama çabalarına yardımcı olmak amacıyla genel tehdit istihbaratı toplanmasına katkıda bulunabilir.
Ayrıca bir analist olarak olayın öyküsünü anlatmaya yardımcı olacak bulguların zaman çizelgesini oluşturacaksınız; Bununla birlikte, programın/dosyanın ne zaman kurulduğuna dair zaman damgalarına sahip olmak bu zaman çizelgesine katkıda bulunabilir.
Belki bir dosya yeniden adlandırılmıştır? Yayıncı bilgilerine ve SHA1 karmasına sahip olarak, 'svchost'un yasal bir sürümü olduğunu düşündüğümüz dosyanın aslında kötü amaçlı yazılım olduğunu belirleyebiliriz!

# AmCache Yapılarının Konumu
AmCache.hve dosyası şu konumda bulunur: **C:\Windows\appcompat\Programs\Amcache.hve**

# AmCache Yapılarının Yapısı
AmCache.hve dosyası bir kayıt defteri kovanı dosyasıdır. Kayıt defteri dosyası formatı, bir grup anahtar, alt anahtar ve değerden oluşan, dosya sistemine benzer bir ikili dosyadır.
Bu dosyalar işletim sistemi tarafından kullanıcı, sistem ve uygulama yapılandırmalarını depolamak için kullanılır.

# ArtiFast Windows ile AmCache Yapılarını Analiz Etme
Bu bölümde, Windows makinelerinden AmCache yapıtlarını çıkarmak için ArtiFast Windows'un nasıl kullanılacağı ve bu yapıtlardan ne tür dijital adli bilgiler elde edebileceğimiz tartışılacak.
Vakanızı oluşturduktan ve soruşturma için kanıt ekledikten sonra, Artifact Ayrıştırıcı Seçim Aşamasında AmCache Artifact'lerini seçebilirsiniz:

![image](https://github.com/user-attachments/assets/1cb11cb1-da32-43d0-a756-d91db107f1ca)

ArtiFast, Windows 10 sistemlerinden AmCache uygulama dosyalarını, yürütülen programları, sürücü ikili dosyalarını, Pnp aygıtlarını, sürücü paketlerini, aygıt kapsayıcılarını ve uygulama kısayollarını analiz edebilir.

![image](https://github.com/user-attachments/assets/5efc3031-6941-4222-8ac7-b503832423f8)

ArtiFast ayrıştırıcı eklentileri, analiz için yapıtın işlenmesini tamamladıktan sonra, indeksleme, filtreleme ve arama yetenekleriyle "Yapı Görünümü" veya "Zaman Çizelgesi Görünümü" aracılığıyla incelenebilir.

# AmCache Uygulama Dosyaları Yapısı

* **Application ID(Uygulama Kimliği)** - Uygulamanın benzersiz tanımlayıcısı.
* **Application Name(Uygulama Adı)** – Uygulamanın adı.
* **File Path(Dosya Yolu)** - Uygulama dosyasının yolu.
* **Size(Boyut)** - Uygulama dosyasının boyutu.
* **SHA-1 Hash** - Uygulama dosyası imzası.
* **Long Path Hash (Uzun Yol Karması)** – Dosyayla ilişkili uzun yolun karması.
* **Publisher(Yayımcı)** - Yayınlanan uygulamanın adı.
* **Binary File Version(İkili Dosya Sürümü)** - Uygulamanın ikili dosya sürümü.
* **Binary Type(İkili Tür)** - Uygulamanın ikili türü.
* **Product Name(Ürün Adı)** – Ürünün adı.
*  **Product Version(Ürün Sürümü)** - Uygulamanın ürün sürümü.
* **Application Version(Uygulama Sürümü)** - Uygulama sürümü.
* **Lınk Date/Time(Bağlantı Tarihi/Saati)** - Dosyanın bağlantı tarihi ve saati.
* **Binary Product Version(İkili Ürün Sürümü)** - Ürünün ikili sürümü.
* **Language(Dil)** – Dosyanın dil kodu.
* **PE File(PE Dosyası)** - Dosyanın bir PE başlığı olup olmadığı.
* **OS Component(İşletim Sistemi Bileşeni)** - Dosyanın bir işletim sistemi bileşeni olup olmadığı.
* **USN** - USN.
* **Last Update Date/Time(Son Güncelleme Tarihi/Saati)** - Kayıt defteri anahtarının son güncelleme tarihi/saati.

# Amcache eseriyle kaydedilenlere kısaca geçelim:
* Yüklü uygulamalar/programlar
* Yürütülmüş olabilecek programlar
* Yüklü sürücüler
* Ürün adı
* İkili tip
* Dosya adı
* Ürün sürümü
* Yayıncı bilgileri
* SHA1 karması
* Sürücünün değiştirilmiş zaman damgası
* Sürücü imzalı mı?
* Sürücünün meta verileri
* Yol dosya boyutu
* Derleme zamanı
* Dil Kimliği ve daha fazlası..

# Gelin bu esere bir göz atalım! 
Daha önce de belirtildiği gibi, bu kovanı daha kolay ayrıştırmak için bir adli tıp aracına ihtiyacınız olacak.Ayrıca işletim sistemi tarafından kilitleneceği ve kullanımda olacağı için bunu canlı bir sistemde analiz edemezsiniz.
Peki bunu nasıl analiz edebiliriz? Bunu Autopsy gibi bir adli tıp aracıyla toplayabilirsiniz ya da Kroll'dan Eric Zimmerman'ın hazırladığı muhteşem "KAPE" aracıyla toplayabilirsiniz.

# KAPE
KAPE, işletim sistemi tarafından kullanılan kilitli dosyaları atlama ve toplama yeteneğine sahiptir.

![image](https://github.com/user-attachments/assets/ef8a3a71-bd32-4678-88f6-9a47abe06d5d)

Eric Zimmerman'ın "Kayıt Defteri Gezgini" adlı bir kayıt defteri adli tıp aracıyla manuel olarak inceleyerek başlayalım!

![image](https://github.com/user-attachments/assets/0419dd81-39b0-4421-8f53-a28ecf66be91)

Öncelikle ortak "InventoryApplicationFile" anahtarına bir göz atalım, çünkü bu anahtar yüklü uygulamalarla ilgili alt anahtarları içerir. Yüklü bir uygulama için bu alt anahtarlardan birini açalım ve hangi verilerin gösterildiğine bir göz atalım.

![image](https://github.com/user-attachments/assets/0a5da741-bf72-4a59-b904-a1007954a8e0)

Bu alt anahtarlarla ilişkili zaman damgalarını analiz ederken lütfen dikkatli olun. Belirtildiği gibi, kayıt defteri anahtarının son değiştirilme zaman damgaları, daha önce bahsedilen zamanlanmış görevin dosyayı taradığı zaman ile temsil edilebilir.

![image](https://github.com/user-attachments/assets/148d7900-2802-4208-bf8d-b35b47a99023)

Amcache'in sürücülerle ilgili bilgileri kaydedebildiğinden bahsettiğimi hatırlıyor musunuz? Peki "InventoryDriverBinary" alt anahtarının ne içerdiğini düşünüyoruz? Sürücü bilgisi!

![image](https://github.com/user-attachments/assets/7e8e13f4-3f5b-466a-a520-57eb15432b5c)

### Burada başka hangi güzellikleri bulabileceğinizi görmek için kalan anahtarları ve alt anahtarları incelemekten çekinmeyin! Ancak belirtildiği gibi bu yapıtı ayrıştırmanın çok daha kolay bir yolu var.
Başka bir Eric Zimmerman aracı olan 'Amcache Ayrıştırıcı'yı girin. Aşağıdaki komutu çalıştırarak bu aracı toplanan Amcache kovanına karşı çalıştıralım:

## Amcacheparser.exe -i -f AmcacheHiveHere.hve --csv C:\location_here
Bilgilendirme amacıyla bu sözdizimini hızlı bir şekilde parçalara ayıracağız:

* -i araca yüklü uygulamalarla ilgili tüm bilgileri eklemesini söyleyeceğim
* -f ayrıştırılacak kovandır
* --csv format türüdür
* C:\Location_here, çıktı CSV dosyalarını göndermek istediğiniz yerin çıktı konumunu temsil eder

Tüm bu dosyaların gözden geçirilmesi gerekmesine rağmen, burada Program Girişleri, İlişkili Dosya Girişleri ve İlişkisiz dosya girişleri dosyalarına odaklanacağız çünkü bunlar gözlemlenen programlarla ilgili bilgiler içerir
Lütfen "İlişkili dosya girişleri"nin genellikle yüklü uygulamalar olarak listelendiğini, "İlişkisiz" seçeneğinin ise genellikle bağımsız yürütülebilir dosyalar gibi bir yükleme dosyasının parçası olmayan dosyalarla ilgili olduğunu unutmayın.

![image](https://github.com/user-attachments/assets/6343d707-8413-4c37-933c-20cf9b180491)

Buradan itibaren bu verileri analizimizi yönlendirmek için kullanabiliriz; örneğin zaman damgaları, hatalı dosya karmaları, imzasız sürücüler/ikili dosyalar, şüpheli yollar vb.

Kaynak: https://forensafe.com/blogs/AmCache.html

Kaynak 2: https://www.thedfirspot.com/post/evidence-of-program-existence-amcache




