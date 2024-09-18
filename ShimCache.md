## Başka bir harika Windows izinsiz giriş analizi eseri! Shimcache!

* **Sistemde bulunan çeşitli uygulamalarda uyumluluk kontrolleri yapmak için kullanılır**
* **Uyumluluk sorunu varsa, shimcache uygulamayı "kaydırmaya" çalışacak ve bu da dosyayı mevcut sistemde çalıştırmak amacıyla dosyanın özelliklerini değiştirecektir.**
* **"AppCompatCache" olarak da bilinir**
* **Zamanın durdurulduğunun kanıtı için zaman damgalarını karşılaştırmak yararlı olabilir**
* **'SİSTEM' kayıt defteri kovanında bulunur**
* **Uygulamanın yürütülüp yürütülmediğini belirlemeye yardımcı olmak için "yürütüldü" bayrağı bulunabilir**
* **AppCompatCache/Shimcache anahtarı yalnızca sistem kapatıldığında/yeniden başlatıldığında kayıt defterine yazılır**
* **Bir adli tıp aracıyla çıkarılıp analiz edilmesi gerekecek**

### Bu eser büyük ölçüde yanlış anlaşılıyor veya en azından yanlış yorumlanıyor. Bu neden?

Windows 10'dan başlayarak daha yeni sistemlerde, "kaydırma" işlemi artık işletim sistemi tarafından otomatik olarak yapılıyor.Ancak adli tıp açısından bakıldığında bu artık programın yürütüldüğünü kanıtlamak için kullanılamaz.
Bu nedenle Shimcache'i yalnızca söz konusu sistemde bir dosyanın var olduğunu bir şekilde kanıtlamanın bir yolu olarak kullanmalıyız.

## İşletim Sistemine (OS) bağlı olarak bu yapı iki konumdan birinde bulunabilir:
### Server 2003/2008/2012/2016+ and Windows 7-10+
* **SYSTEM\CurrentControlSet\Control\SessionManager\AppCompatCache\AppCompatCache**

* **512 entries on Server 2003**

* **1024 entries on the others**

### Windows XP

* **SYSTEM\CurrentControlSet\Control\SessionManager\AppCompatibility\AppCompatCache**

* **96 entries** 

Bu anahtarı ve verilerini doğru şekilde analiz etmek için bir adli tıp aracına ihtiyacınız olacak.Peki, buna doğrudan Windows'ta yerleşik olan varsayılan Kayıt Defteri Düzenleyicisi'nde bir göz atalım.

![image](https://github.com/user-attachments/assets/823ad29b-85db-4bf1-ba06-633351d61d5b)

Zaman damgaları aslında dosyanın "son değiştirilen" zaman damgalarıdır, yürütme zamanı değil.Bununla birlikte Shimcache'i raporunuza veya zaman çizelgenize dahil ederken son derece dikkatli olun.
"Shimcache" zaman damgasının 2015'e ait olduğunu görürseniz bu, TA'nın o tarihten bu yana erişime sahip olduğu anlamına gelmeyebilir!Aşağıda gösterildiği gibi, zaman damgalarının her yerde biraz olduğunu görebiliriz. Yine, bunlar en son değiştirilen zaman damgalarıdır.

![image](https://github.com/user-attachments/assets/49c9d07d-81b8-4d92-b81d-a88b71410e71)

AppCompatCache/Shimcache anahtarı yalnızca sistem kapatıldığında/yeniden başlatıldığında kayıt defterine yazılır.Aksi takdirde, bu değerler sistem kapatıldıktan sonra kayıt defterine işlenene kadar bellekte yalnızca bir "arabellek" olarak bulunur. Adli tıp açısından bu ne anlama geliyor?
Asistan veya sistem sahibi sistemi kapatmadıkça veya yeniden başlatmadıkça Shimcache anahtarı en güncel bilgileri içermeyebilir.Ancak Volatilite gibi bir araç kullanarak bunu kesinlikle bir bellek dökümünden çıkarabiliriz!

https://github.com/mandiant/Volatility-Plugins/blob/master/shimcachemem/README.md


Bunu canlı bir sistemde yapıyorsak PowerShell, CMD veya favori kabuğunuz içindeki AppCompatParser yürütülebilir dosyasına gidin ve aşağıdaki komutu yürütün:

![image](https://github.com/user-attachments/assets/13188ee4-d1a4-4ba3-8759-cd8ae3a5045c)

Çalışma Örneğim aşağıdaki gibidir:

![image](https://github.com/user-attachments/assets/7bafc39d-3154-432b-8ed3-f8506085737b)


