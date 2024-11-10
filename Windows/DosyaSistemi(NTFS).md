### Windows'un modern sürümlerinde kullanılan dosya sistemi Yeni Teknoloji Dosya Sistemi veya kısaca NTFS'dir.
### NTFS'den önce FAT16/FAT32 (Dosya Ayırma Tablosu) ve HPFS (Yüksek Performanslı Dosya Sistemi) vardı.NTFS, günlükleme dosya sistemi olarak bilinir. Bir arıza durumunda, dosya sistemi günlük dosyasında depolanan bilgileri kullanarak diskteki klasörleri/dosyaları otomatik olarak onarabilir. Bu işlev FAT ile mümkün değildir.

NTFS, önceki dosya sistemlerinin birçok sınırlamasını ele alır; 
* 4 GB'tan büyük dosyaları destekler 
* Klasörler ve dosyalar üzerinde belirli izinler ayarlar
* Klasör ve dosya sıkıştırma
* Şifreleme (Şifreleme Dosya Sistemi veya EFS)

### Windows çalıştırıyorsanız, Windows kurulumunuzun kullandığı dosya sistemi nedir? İşletim sisteminizin kurulu olduğu sürücünün Özelliklerini (sağ tıklama) kontrol edebilirsiniz, genellikle C sürücüsü (C:\).

![image](https://github.com/user-attachments/assets/5eb3ea23-2a4a-415a-89d8-e83162c5370d)

NTFS'ye özgü bazı özelliklerden kısaca bahsedelim. NTFS birimlerinde, dosyalara ve klasörlere erişim izni veren veya erişimi engelleyen izinler ayarlayabilirsiniz. İzinler şunlardır:

* Tam kontrol
* Değiştir
* Oku ve Çalıştır
* Klasör içeriklerini listele
* Oku
* Yaz

### Aşağıdaki görselde her bir iznin bir dosyaya ve klasöre nasıl uygulandığına dair anlamlar listelenmiştir. (Microsoft'a aittir)

![image](https://github.com/user-attachments/assets/b7d4c022-3347-4bbc-aee5-ba1791a70ef2)

Bir dosya veya klasörün izinlerini nasıl görüntüleyebilirsiniz?

* İzinlerini kontrol etmek istediğiniz dosya veya klasöre sağ tıklayın.
* Bağlam menüsünden **Özellikler’i** seçin.
* Özellikler içerisinde **Güvenlik** sekmesine tıklayın.
* **Grup veya kullanıcı adları** listesinde, izinlerini görüntülemek istediğiniz kullanıcıyı, bilgisayarı veya grubu seçin.

Aşağıdaki görselde Windows klasörü için Kullanıcılar grubunun izinlerini görebilirsiniz.

![image](https://github.com/user-attachments/assets/44e67002-e5e1-4b42-b427-983b1e98bbdd)

### NTFS'nin bir diğer özelliği ise Alternatif Veri Akışları'dır (ADS).
**Alternatif Veri Akışları (ADS)**, Windows NTFS'ye (Yeni Teknoloji Dosya Sistemi) özgü bir dosya niteliğidir.Her dosyanın en az bir veri akışı ($DATA) vardır ve ADS dosyaların birden fazla veri akışı içermesine izin verir.
Yerel olarak Window Explorer kullanıcıya ADS göstermez. Bu verileri görüntülemek için kullanılabilecek 3. parti yürütülebilir dosyalar vardır, ancak Powershell size dosyalar için ADS görüntüleme yeteneği verir.

Güvenlik açısından bakıldığında, kötü amaçlı yazılım yazarları verileri gizlemek için ADS'yi kullanmaktadır.

ADS hakkında daha fazla bilgi edinmek için MalwareBytes'ın aşağıdaki bağlantısına bakın.

https://www.malwarebytes.com/blog/101/2015/07/introduction-to-alternate-data-streams

