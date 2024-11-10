Tipik bir yerel Windows sisteminde ser hesapları iki türden biri olabilir: **Yönetici ve Standart Kullanıcı**.
Kullanıcı hesabı türü, kullanıcının belirli Windows sisteminde hangi eylemleri gerçekleştirebileceğini belirler.
* **Bir Yönetici** sistemde değişiklikler yapabilir: kullanıcı ekleyebilir, kullanıcıları silebilir, grupları değiştirebilir, sistemdeki ayarları değiştirebilir, vb.
* **Standart Kullanıcı** yalnızca kendisine atfedilen klasörlerde/dosyalarda değişiklik yapabilir ve program yükleme gibi sistem düzeyinde değişiklikler gerçekleştiremez.

Sistemde hangi kullanıcı hesaplarının bulunduğunu belirlemenin birkaç yolu vardır. Bir yol, **Başlat Menüsüne** tıklamak ve **Diğer Kullanıcı** yazmaktır. **Sistem Ayarları > Diğer kullanıcılar** için bir kısayol görünmelidir.

![image](https://github.com/user-attachments/assets/aa2e088b-ade2-4d9d-87b6-33207da306d7)

Yönetici olduğunuz için, bu bilgisayara başka birini ekleme seçeneğini görürsünüz. Not: Standart Kullanıcı bu seçeneği görmeyecektir.   
Yerel kullanıcı hesabına tıklayın. Daha fazla seçenek görünmelidir: Hesap türünü değiştir ve Kaldır.

![image](https://github.com/user-attachments/assets/73ca92eb-3ad2-4c6a-8283-dc89507479a2)

Hesap türünü değiştir'e tıklayın. Açılır kutudaki değer (ya da açılır kutuyu tıklarsanız vurgulanan değer) cari hesap türüdür.

![image](https://github.com/user-attachments/assets/00c179e8-b7ad-4dad-9930-d2e4bb1ae4a1)

Bir kullanıcı hesabı oluşturulduğunda, kullanıcı için bir profil oluşturulur. Her kullanıcı profili klasörünün konumu C:\Users altına düşecektir. Örneğin, Max kullanıcı hesabı için kullanıcı profili klasörü **C:\Users\Max** olacaktır.

Kullanıcı profilinin oluşturulması ilk oturum açma sırasında yapılır. Yeni bir kullanıcı hesabı ilk kez yerel bir sisteme oturum açtığında, oturum açma ekranında birkaç mesaj görür. Mesajlardan biri olan Kullanıcı Profili Hizmeti, bir süre oturum açma ekranında kalır ve kullanıcı profilini oluşturma işlemindedir. 

![image](https://github.com/user-attachments/assets/400402ee-30fd-4f6e-8231-458c48542dd1)

Giriş yaptıktan sonra kullanıcı, profilin oluşturulduğunu belirten aşağıdakine benzer bir iletişim kutusu görecektir.

![image](https://github.com/user-attachments/assets/3d38e54b-131b-4fe6-ade4-d56120df8ba1)

Her kullanıcı profili aynı klasörlere sahip olacak; bunlardan birkaçı şunlardır:

* Masaüstü
* Belgeler
* İndirilenler
* Müzik
* Resimler

Bu bilgilere ve daha fazlasına ulaşmanın bir başka yolu da Yerel Kullanıcı ve Grup Yönetimi'ni kullanmaktır.Başlat Menüsüne sağ tıklayın ve Çalıştır'a tıklayın. **lusrmgr.msc** yazın. 

![image](https://github.com/user-attachments/assets/5fa91ae8-70c4-4cd6-a1c3-e8d1515e305a)

Not: Çalıştır İletişim Kutusu öğeleri hızlı bir şekilde açmamızı sağlar.  lusrmgr'ye geri dönersek, iki klasör görmelisiniz: Kullanıcılar ve Gruplar.
Gruplar'a tıkladığınızda yerel grupların tüm isimlerini, her grup için kısa bir açıklamayla birlikte görürsünüz.

Her grubun kendisine ayarlanmış izinleri vardır ve kullanıcılar Yönetici tarafından gruplara atanır/eklenir. Bir kullanıcı bir gruba atandığında, kullanıcı o grubun izinlerini devralır. Bir kullanıcı birden fazla gruba atanabilir.

### Not: Diğer kullanıcılar'dan Bu Bilgisayara Başkasını Ekle'ye tıkladığınızda Yerel Kullanıcılar ve Yönetim açılacaktır.
