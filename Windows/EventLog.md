## Windows Event Log (Olay Günlüğü) nedir?

#### Windows olay günlüğü, bir Microsoft sistemindeki sistem, güvenlik ve uygulamalarla ilgili belirli olayları kaydeder.

## Windows Olay Günlüğü Tanımı

Windows olay günlüğü, Windows işletim sisteminde depolanan sistem, güvenlik ve uygulamayla ilgili olayların ayrıntılı bir kaydıdır.  Olay günlükleri, sistemi ve bazı uygulama sorunlarını izlemek ve gelecekteki sorunları tahmin etmek için kullanılabilir.

## Windows Olay Günlüğünün Öğeleri

Windows olay günlüğü, Windows işletim sisteminde meydana gelen donanım ve yazılım olayları hakkında bilgi sağlar. Ağ yöneticilerinin potansiyel tehditleri ve performansı düşürebilecek sorunları izlemelerine yardımcı olur.
Windows, olay günlüklerini bilgilerin net bir şekilde anlaşılmasına olanak tanıyan standart bir biçimde saklar. Bir olay günlüğünün ana unsurları şunlardır:

* **Log Name (Günlük adı):** Farklı günlük oluşturma bileşenlerinden etkinliklerin yazılacağı etkinlik günlüğünün adı. Olaylar genellikle sistem, güvenlik ve uygulamalar için günlüğe kaydedilir.
* **Event Date/Time (Etkinlik tarihi/saati):** Olayın gerçekleştiği tarihi ve saati içerir.
* **Task Category (Görev kategorisi):** Kaydedilen olay günlüğünün türünü tanımlar. Uygulama geliştiricileri ayrıca etkinlik hakkında ek bilgi olarak hizmet verecek görev kategorilerini de tanımlayabilir.
* **Even ID (Etkinlik Kimliği):** Bu Windows kimlik numarası, ağ yöneticilerinin günlüğe kaydedilen belirli bir etkinliği benzersiz şekilde tanımlamasına yardımcı olur.
* **Source (Kaynak):** Olay günlüğüne neden olan programın veya yazılımın adı.
* **Level (Düzey):** Olay düzeyi, kaydedilen olay günlüğünün ciddiyetini temsil eder. Bunlar; bilgi, hata, ayrıntılı, uyarı ve kritiktir.
* **User (Kullanıcı):** Olay meydana geldiğinde Windows bilgisayarda oturum açan kullanıcının adı.
* **Computer (Bilgisayar):** Etkinliği kaydeden bilgisayarın adı.

## Windows Olay Günlüğünde Ne Tür Bilgiler Depolanır?

Windows olay günlükleri, sistem içinde meydana gelen farklı olaylarla ilgili bilgileri depolar. Saklanan bilgilerin türü, olay günlüğünün kategorisine göre değişir. Veriler dört Windows olay günlüğü türü için ortak olarak kaydedilir:

* system
* application
* setup
* security

**Windows System- sistem olay günlüğü**, Windows işletim sistemiyle ilgili olaylarla ilgili bilgileri içerir. 

**Application-Uygulama olay günlüğü**, makinede yüklü yazılımda meydana gelen hatalar hakkında bazı bilgiler sağlar.

**Security-Güvenlik olay günlüğü**, sistemdeki güvenlik olaylarıyla ilgili verileri içerirken 

**Setup-Kurulum günlüğü**, daha çok kurulumla ilgili olaylara odaklanır.

## Olay Günlüğü Kategorileri ve Türleri

Olay günlükleri uygulama, güvenlik, kurulum ve sistem olmak üzere dört kategoriye ayrılır. Ayrıca iletilen olaylar adı verilen özel bir olay günlüğü kategorisi de vardır.

* **Forwarded Events-İletilen Etkinlikler:** Aynı ağdaki diğer bilgisayarlardan iletilen olay günlüklerini içerir.

### Windows olayları ayrıca beş farklı türe ayrılmıştır:

1- **Information-Bilgi:** Bir uygulamanın veya hizmetin iyi çalıştığını gösterir. Örneğin Windows ağ sürücüsünü yüklediğinde olay bir bilgi olayı olarak günlüğe kaydedilir.
2- **Warning-Uyarı:** Gelecekte olası sorunlara işaret eden önemsiz olaylar. Disk alanının az olması gibi bir sorun için bir uyarı olayı günlüğe kaydedilir.
3- **Error-Hata:** Sistem normal şekilde çalışamadığında (örneğin, işletim sisteminin yanıt vermemesi) ortaya çıkan önemli bir sorunu açıklar.
4- **Success Audit-Başarı Denetimi:** Güvenlik günlüğü için denetlenen güvenlik erişiminin geçerli girişimini kaydeder. Örneğin, iyi giden bir oturum açma girişimi, bir başarı denetimi etkinliği kapsamına girecektir.
5- **Failure Audit-Arıza Denetimi:** Ağ sürücüsüne erişilememesi gibi, güvenlik günlüğü altında denetlenen güvenlik erişiminin başarısızlığını gösterir.

## Windows Olay Günlükleri Nasıl Kontrol Edilir ve Görüntülenir

Windows olay günlüğü konumu C:\WINDOWS\system32\config\ klasörüdür. Sistemdeki sorunları takip etmek için olay günlükleri 'Olay Görüntüleyici' yardımıyla kontrol edilebilir. İşte nasıl:

* Çalıştırma penceresini açmak için klavyenizdeki Windows tuşu + R'ye basın
* Çalıştır iletişim kutusuna eventvwr yazın ve Tamam'ı tıklayın
* Olay Görüntüleyici penceresinde Windows Günlükleri menüsünü genişletin
* Windows Günlükleri menüsünde farklı olay günlüğü kategorilerini (uygulama, güvenlik, kurulum, sistem ve iletilen etkinlikler) göreceksiniz.
* Altına kaydedilen olayları kontrol etmek ve görüntülemek için olay günlüklerinden birine tıklayın.

Kaynak : https://www.solarwinds.com/resources/it-glossary/windows-event-log
