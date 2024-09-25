### Pek çok geliştirici PowerShell'i seviyor ve bunun iyi bir nedeni var: çoğumuzun çok fazla zaman harcadığı Windows Komut İstemi'ne güç, işlevsellik ve esneklik katıyor.PowerShell komutları cmdlet'ler olarak bilinir ve bu cmdlet'ler, işlevsel yeteneklerinin arkasındaki itici güçtür.Genel Windows deneyimini geliştiren komutlardan, geliştirme çalışmaları için faydalı komutlara kadar geliştiricilerin bilmesi gereken onlarca önemli komut vardır.Bu listeyi, PowerShell'in gücünden yeni yararlanmaya başlayanlar ve PowerShell deneyimlerini yükseltmek isteyenler için kullanışlı bir referans kılavuzu olarak hazırladım:

## Temel PowerShell Cmdlet'leri

**1- Get-Command**

Get-Command, mevcut oturumunuzda kullanabileceğiniz tüm komutları getiren, kullanımı kolay bir referans cmdlet'idir. Bu komutu yazmanız yeterlidir:

![image](https://github.com/user-attachments/assets/d517df83-dda8-4ad1-9ed6-45101adc521c)

Şu şekilde gözükecektir:

![image](https://github.com/user-attachments/assets/a2dd9336-a06b-4bc1-8e42-456ea1e25729)

**2- Get-Help**

Get-Help komutu, PowerShell kullanan herkes için gereklidir ve mevcut tüm komutları çalıştırmak ve bunlarla çalışmak için ihtiyaç duyduğunuz bilgilere hızlı erişim sağlar. Örneğin bazı örnekler istiyorsanız aşağıdakileri girersiniz:

![image](https://github.com/user-attachments/assets/e660d132-05b3-4e58-9d8f-3dadc12c3904)

**3- Set-ExecutionPolicy**

Microsoft, kötü amaçlı komut dosyalarının PowerShell ortamında yürütülmesini önlemek için komut dosyası oluşturmayı varsayılan olarak devre dışı bırakır.Ancak geliştiriciler komut dosyaları yazıp yürütebilmek isterler; bu nedenle Set-ExecutionPolicy komutu, PowerShell komut dosyalarını çevreleyen güvenlik düzeyini denetlemenize olanak tanır.
Dört güvenlik seviyesinden birini ayarlayabilirsiniz:

* **Restricted:(Sınırlı):** Bu, PowerShell betiklerinin çalışmasını engelleyen varsayılan güvenlik düzeyidir. Bu güvenlik seviyesinde komutları yalnızca etkileşimli olarak girebilirsiniz.
* **All Signed(Tamamı İmzalı):** Bu güvenlik düzeyi, komut dosyalarının yalnızca güvenilir bir yayıncı tarafından imzalanması durumunda çalıştırılmasına izin verir.
* **Remote Signed(Uzaktan İmzalı):** Bu güvenlik düzeyinde, yerel olarak oluşturulan tüm PowerShell betiklerinin çalıştırılmasına izin verilir. Uzaktan oluşturulan komut dosyalarının yalnızca saygın bir yayıncı tarafından imzalanmış olması durumunda çalıştırılmasına izin verilir.
* **Unrestricted: (Sınırsız)** Adından da anlaşılacağı gibi, sınırsız güvenlik düzeyi, yürütme politikasındaki tüm kısıtlamaları kaldırarak tüm komut dosyalarının çalışmasına izin verir.

Benzer şekilde, alışılmadık bir ortamda çalışıyorsanız, bu komutu kullanarak mevcut yürütme politikasının ne olduğunu kolayca öğrenebilirsiniz:

![image](https://github.com/user-attachments/assets/789f6fe7-b13e-45a0-b16e-008d47a94158)

**4- Get-Service**

Sistemde hangi hizmetlerin yüklü olduğunu bilmek de faydalıdır. Bu bilgilere aşağıdaki komutla kolayca ulaşabilirsiniz:

![image](https://github.com/user-attachments/assets/7ea883d2-e0f7-40f2-b1a1-5e048ea1776a)

Belirli bir hizmetin yüklü olup olmadığını bilmeniz gerekiyorsa -Name anahtarını ve hizmetin adını ekleyebilirsiniz; Windows, hizmetin durumunu gösterecektir.Ek olarak, halihazırda yüklü olan hizmetlerin belirli bir alt kümesini döndürmek için filtreleme özelliklerinden yararlanabilirsiniz.
Aşağıdaki örnek, Get-Service komutundan Where-Object cmdlet'ine aktarılan bir veri çıkışıyla sonuçlanacak ve bu daha sonra durdurulan hizmetler dışındaki her şeyi filtreleyecektir:

![image](https://github.com/user-attachments/assets/3fe2ff16-8833-45ea-8eda-51c5748b9473)

**5- ConvertTo-HTML**

Bir raporda kullanabileceğiniz veya başka birine gönderebileceğiniz verileri çıkarmanız gerekiyorsa, ConvertTo-HTML bunu yapmanın basit bir yoludur.Bunu kullanmak için, başka bir komutun çıktısını ConvertTo-HTML komutuna aktarın ve HTML dosyasında hangi çıktı özelliklerini istediğinizi belirtmek için -Property anahtarını kullanın. Ayrıca bir dosya adı da sağlamanız gerekir.
Örneğin, aşağıdaki kod mevcut konsoldaki PowerShell takma adlarını listeleyen bir HTML sayfası oluşturur:

![image](https://github.com/user-attachments/assets/27980c92-3cf9-4980-aaa6-338cc140a2ed)

cmdlet hemen hemen aynı şekilde çalışır ancak verileri HTML yerine .CSV dosyasına aktarır.

![image](https://github.com/user-attachments/assets/e95f3de8-17b5-4f38-8ca4-9912b78ee146)

**6- Get-EventLog**

Get-EventLog cmdlet'ini kullanarak makinenizin olay günlüklerini ayrıştırmak için aslında PowerShell'i kullanabilirsiniz. Çeşitli parametreler mevcuttur.
Belirli bir günlüğü görüntülemek için -Log anahtarını ve ardından günlük dosyasının adını kullanın. Örneğin Uygulama günlüğünü görüntülemek için aşağıdaki komutu kullanırsınız:

![image](https://github.com/user-attachments/assets/57f13840-7061-40fe-bdfb-d33f28886935)

**7- Get-Process**
Kullanılabilir hizmetlerin bir listesini almak gibi, o anda çalışan tüm işlemlerin hızlı bir listesini alabilmek de genellikle faydalıdır. Get-Process komutu bu bilgiyi parmaklarınızın ucuna getirir.

## #DİPNOT: 
Bonus: Donmuş veya artık yanıt vermeyen işlemleri durdurmak için İşlemi Durdur'u kullanın. Hangi sürecin sizi engellediğinden emin değilseniz sorunlu süreci hızlı bir şekilde tanımlamak için Get-Process'i kullanın.
İşte bir örnek. Şu anda çalışan tüm Not Defteri örneklerini sonlandırmak için bu komutu çalıştırın

![image](https://github.com/user-attachments/assets/d620903c-67c5-4d2c-9809-c343a036c3fe)

Notepad'in tüm örneklerini ve note ile başlayan diğer işlemleri sonlandıran aşağıdaki örnek gibi joker karakterleri de kullanabilirsiniz:

![image](https://github.com/user-attachments/assets/7e24a0f9-eb6e-42a0-99c2-bf93fe82cb31)

**8-  Clear-History**
Komut geçmişinizdeki girişleri temizlemek isterseniz ne olur? Kolay – Clear-History cmdlet'ini kullanın. Bunu yalnızca belirli komutları silmek için de kullanabilirsiniz.
Örneğin, aşağıdaki komut "yardım" içeren veya "komut" ile biten komutları siler

![image](https://github.com/user-attachments/assets/d9cdb691-e2ef-4ab4-9000-8e7fcc0eb615)

**9- Format-Table**
Bu cmdlet herhangi bir çıktıyı tablo olarak biçimlendirmek için kullanılır. Örneğin, aşağıdaki komut çalışan işlemleri alır, bunları BasePriority'ye göre sıralar ve bir tablodaki listeyi biçimlendirir:

![image](https://github.com/user-attachments/assets/3159b421-a437-4b56-ada0-0108dfbbce65)

Yukarıdaki örnek aşağıdakine benzer bir tablo formatı üretir:

![image](https://github.com/user-attachments/assets/fffe02b6-647d-4e0c-99a3-53fccea67b0c)

**10- Select-Object**
Select-Object cmdlet'i tek bir nesnenin veya nesne grubunun belirtilen özelliklerini seçer. Ek olarak, bir diziden benzersiz nesneleri veya bir dizinin başından veya sonundan belirli sayıda nesneyi seçebilir.

![image](https://github.com/user-attachments/assets/c0b062f1-9ab5-43ca-93b5-3c9273bc31f0)

Benzer işlevlere sahip başka cmdlet'ler de vardır: 
**Select-String:** Dizeler veya dosyalardaki metni bulur. 
**Select-XML:** Bir XML dizesi veya belgesindeki metni bulur.











