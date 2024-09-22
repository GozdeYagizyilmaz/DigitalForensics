## Komut satırının en çok kullanılan ve işinize en çok yarayacak olan  komutlarını bilmeniz gerek. Windows İşletim Sisteminde size zaman kazandıracak ve bir çok işlemi yapmanızı sağlayacak olan temel komutlara gelin birlikte bakalım :

## cd (Change Directory)
**Hem Windows hem Linux için en çok kullanılan temel komutlardan birisi cd komutudur. Bir dizine gitmek için kullanılır.**

**Örneğin Desktop dizinine gitmek için:**

![image](https://github.com/user-attachments/assets/5addb2d4-2375-43d1-8306-7b76ef296d9d)

**Dizinde geri gelmek için: **cd..** kullanılır.Örnek olarak :**

![image](https://github.com/user-attachments/assets/ad59afe6-dbc7-4d9b-862a-067d3e9c9a2c)

**Bir dizinde en başa dönmek için kullanacağımız komut ise : cd../..** 

![image](https://github.com/user-attachments/assets/82b12245-4002-44fa-b9d6-a8673a71a5cc)

#### NOT:Komut satırında "Tab" kullanarak yazılan kelimeyi tamamlarız.Böylece hem zamandan kazanır hem de olası yazım yanlışlarını önlemiş oluruz.

## dir(Directory)
**Mevcut dizindeki dosya ve klasörlerin listesini gösterir.Ayrıca dosyaların boyut tarih ve saat gibi detaylarını verir.**
**Linuxtaki "ls" komutunun Windows karşılığı diyebiliriz.**

![image](https://github.com/user-attachments/assets/39a8a437-8eb9-4aa6-83d2-1303e1f930ff)

### dir komutu ile neler yapabiliriz?
**dir komutunun ne işe yaradığını basit bir örnekle öğrendik.Peki bununla ilgili başka neler yapabiliriz ?**

* **Gizli dizinleri listelemek(bilgisayarınızda bir virüs olduğu şüphesi ile kullanabilirsiniz) için *dir /a* kullanırız.**

![image](https://github.com/user-attachments/assets/4a2a6d13-6a22-40cd-a1f8-dbdae99ef046)

* **dir *.png komutu ise sadece belirtilen formattaki dosyaları görüntüler. "*" işareti burada joker karakterdir.**

  ![image](https://github.com/user-attachments/assets/035c1696-3c59-4dbd-8232-c7cdd39fd98c)

Örnekte görüldüğü gibi dosya içerisindeki *.exe* bağlantılı tüm dosyaları getirdi.

### NOT:Dizin içerisinde dosyanın ismini yazarsak dosyanın kendisini yüklü olan program eşliğinde çalıştırır. Örneğin *.jpg* uzantılı bir doya ismi verdiğimizde bunu tercih edilen ilk program eşliğinde açar.

##ipconfig
**Windows işletim sistemlerinde ağ yapılandırması hakkında bilgi veren bir komuttur. Bu komutu kullanarak aşağıdaki bilgileri görüntüleyebilirsiniz:**

* **IP adresi:** Bilgisayarın ağ üzerindeki kimliği.
* **Alt ağ maskesi(Subnet Mask):** IP adresinin hangi kısmının ağ adresi olduğunu belirler.
* **Varsayılan ağ geçidi(Default Gateway):** İnternete erişim için kullanılan ana yönlendirici.

**Kullanım**
Komut istemcisinde ipconfig yazarak çalıştırabilirsin. Bazı yaygın parametreleri:

* **ipconfig /all:** Tüm ağ adaptörlerinin ayrıntılı bilgilerini gösterir.
* **ipconfig /release:** Dinamik IP adresini serbest bırakır.
* **ipconfig /renew:** Yeni bir IP adresi almak için DHCP sunucusuna istek gönderir.

Bu komut, ağ sorunlarını giderirken oldukça faydalıdır.




