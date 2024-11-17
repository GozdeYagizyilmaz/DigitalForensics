## Powershell Başlatma
PowerShell, ihtiyaçlarınıza ve ortamınıza bağlı olarak çeşitli şekillerde başlatılabilir. Grafiksel arayüzden (GUI) bir Windows sisteminde çalışıyorsanız, başlatmanın olası yollarından bazıları şunlardır:

![image](https://github.com/user-attachments/assets/6e14801d-2727-43d9-a91c-8e508aa31d7c)

## Temel Sözdizimi: Fiil-İsim

PowerShell komutları cmdlet'ler (command-lets olarak okunur) olarak bilinir.Geleneksel Windows komutlarından çok daha güçlüdürler ve daha gelişmiş veri manipülasyonuna olanak tanırlar.

Bu yapı, her cmdlet'in ne yaptığını anlamayı kolaylaştırır. Fiil, eylemi tanımlar ve İsim, eylemin gerçekleştirildiği nesneyi belirtir. Örneğin:

* **Get-Content:** Bir dosyanın içeriğini alır (alır) ve konsolda görüntüler.
* **Set-Location:** Geçerli çalışma dizinini değiştirir (ayarlar).

## Temel Cmdlet'ler

Mevcut PowerShell oturumunda çalıştırılabilecek tüm kullanılabilir cmdlet'leri, işlevleri, takma adları ve betikleri listelemek için *Get-Command'ı* kullanabiliriz.

![image](https://github.com/user-attachments/assets/60eb8b87-83a2-426b-9d2d-e0b4c86723a0)

Cmdlet tarafından alınan her CommandInfo nesnesi için konsolda bazı temel bilgiler (özellikler) görüntülenir.Komut listesini görüntülenen özellik değerlerine göre filtrelemek mümkündür. Örneğin, yalnızca "function" türündeki kullanılabilir komutları görüntülemek istiyorsak, aşağıda gösterildiği gibi -CommandType "Function" kullanabiliriz: 

![image](https://github.com/user-attachments/assets/180865fe-31a0-474f-89a5-6c4af8d79f17)

Araç kemerinizde bulundurmanız gereken bir diğer temel cmdlet Get-Help'tir: Kullanım, parametreler ve örnekler dahil olmak üzere cmdlet'ler hakkında ayrıntılı bilgi sağlar. PowerShell komutlarını nasıl kullanacağınızı öğrenmek için başvurulacak cmdlet'tir.

![image](https://github.com/user-attachments/assets/99a5320a-eff8-408d-a8a1-c8558040b5cd)

Komuta -examples eklendiğinde, seçilen cmdlet'in kullanılabileceği yaygın yolların bir listesi gösterilecektir.


![image](https://github.com/user-attachments/assets/13360b98-a7aa-4673-a76e-891f62f884f4)

BT profesyonelleri için geçişi kolaylaştırmak amacıyla PowerShell, birçok geleneksel Windows komutu için cmdlet'ler için kısayollar veya alternatif adlar olan takma adlar içerir.
Diğer komut satırı araçlarına aşina olan kullanıcılar için vazgeçilmez olan Get-Alias, mevcut tüm takma adları listeler. Örneğin, dir, Get-ChildItem için bir takma addır ve cd, Set-Location için bir takma addır.


![image](https://github.com/user-attachments/assets/af3b5852-c53c-43c8-874d-ef4b81ff36a4)

## Cmdlet'leri Nerede Bulabilirim ve İndirebilirim?

PowerShell'in bir diğer güçlü özelliği de çevrimiçi depolarından ek cmdlet'ler indirerek işlevselliğini genişletebilme olanağıdır.PowerShell Galerisi gibi çevrimiçi depolarında modülleri (cmdlet koleksiyonlarını) aramak için Find-Module komutunu kullanabiliriz.
Bazen, modülün tam adını bilmiyorsak, benzer ada sahip modülleri aramak faydalı olabilir.
Bunu, Name özelliğini filtreleyerek ve modülün kısmi adına bir joker karakter (*) ekleyerek, aşağıdaki standart PowerShell sözdizimini kullanarak başarabiliriz: Cmdlet -Property "pattern*".


![image](https://github.com/user-attachments/assets/553795da-254d-4dbb-b9d1-fa63c14b1b7e)

Tanımlandıktan sonra, modüller Install-Module ile depodan indirilebilir ve kurulabilir, böylece modülde bulunan yeni cmdlet'ler kullanıma hazır hale gelir. 

