### PowerShell, dosya sisteminde gezinmek ve dosyaları yönetmek için bir dizi cmdlet sağlar; bunların birçoğunun geleneksel Windows CLI'da karşılıkları vardır.

### Komut İstemi'ndeki dir komutuna (veya Unix benzeri sistemlerde ls) benzer şekilde, Get-ChildItem, -Path parametresiyle belirtilen bir konumdaki dosyaları ve dizinleri listeler.


![image](https://github.com/user-attachments/assets/58a7b0aa-f2d9-433f-bbe0-7fe021658429)

Farklı bir dizine gitmek için Set-Location cmdlet'ini kullanabiliriz. Komut İstemi'ndeki cd komutuna benzer şekilde, geçerli dizini değiştirir ve bizi belirtilen yola götürür.


![image](https://github.com/user-attachments/assets/116971c3-af83-491b-a1fb-6d340c648197)

Geleneksel Windows CLI, dizinler ve dosyalar gibi farklı öğeleri oluşturmak ve yönetmek için ayrı komutlar kullanırken, PowerShell, hem dosyaların hem de dizinlerin oluşturulmasını ve yönetilmesini ele alan tek bir cmdlet kümesi sağlayarak bu süreci basitleştirir.
PowerShell'de bir öğe oluşturmak için New-Item kullanabiliriz. Öğenin yolunu ve türünü (bir dosya mı yoksa dizin mi olduğunu) belirtmemiz gerekecektir.


![image](https://github.com/user-attachments/assets/ae645156-47c6-4c7d-bac2-635171f5521f)

Benzer şekilde, Remove-Item cmdlet'i hem dizinleri hem de dosyaları kaldırır, oysa Windows CLI'da rmdir ve del olmak üzere ayrı komutlarımız vardır.

![image](https://github.com/user-attachments/assets/4ce7518d-4f81-48ad-abf3-932bb204c308)

Dosyaları ve dizinleri sırasıyla Copy-Item (kopyalama işlemine eşdeğer) ve Move-Item (taşıma işlemine eşdeğer) kullanarak kopyalayabilir veya taşıyabiliriz.

Son olarak, bir dosyanın içeriğini okumak ve görüntülemek için, Komut İstemi'ndeki type komutuna (veya Unix benzeri sistemlerde cat komutuna) benzer şekilde çalışan Get-Content cmdlet'ini kullanabiliriz.

