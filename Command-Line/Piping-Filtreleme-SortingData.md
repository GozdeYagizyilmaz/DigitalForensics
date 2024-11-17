## Piping
Piping
Borulama, komut satırı ortamlarında kullanılan ve bir komutun çıktısının başka bir komutun girdisi olarak kullanılmasına olanak tanıyan bir tekniktir.

Bu, verilerin bir komuttan diğerine aktığı bir işlem dizisi oluşturur. | sembolüyle temsil edilen borulama,  Windows CLI'da ve Unix tabanlı kabuklarda yaygın olarak kullanılır.

PowerShell'de, borulama daha da güçlüdür çünkü yalnızca metinden ziyade nesneleri iletir. Bu nesneler yalnızca verileri değil, aynı zamanda verileri tanımlayan ve onlarla etkileşime giren özellikleri ve yöntemleri de taşır.

Örneğin, bir dizindeki dosyaların listesini almak ve bunları boyuta göre sıralamak istiyorsanız, PowerShell'de aşağıdaki komutu kullanabilirsiniz:


![image](https://github.com/user-attachments/assets/59694079-a3b0-4912-adae-88d03364308e)

Burada, Get-ChildItem dosyaları (nesneler olarak) alır ve boru (|) bu dosya nesnelerini Sort-Object'e gönderir, Sort-Object de bunları Length (boyut) özelliğine göre sıralar.
Bu nesne tabanlı yaklaşım daha ayrıntılı ve esnek komut dizilerine olanak tanır.

## Filtreleme
Belirtilen koşullara göre nesneleri filtrelemek ve yalnızca ölçütleri karşılayanları döndürmek için Where-Object cmdlet'ini kullanabiliriz. Örneğin, bir dizindeki yalnızca .txt dosyalarını listelemek için şunları kullanabiliriz:


![image](https://github.com/user-attachments/assets/0f0e00f7-b3b6-496c-a9ae-cc87cf696842)

Burada, Where-Object dosyaları Uzantı özelliğine göre filtreler ve yalnızca (-eq) uzantısına sahip dosyaların .txt ile listelenmesini sağlar.
-eq (yani "eşittir") operatörü, diğer betik dilleriyle (örneğin Bash, Python) paylaşılan bir dizi karşılaştırma operatöründen biridir.

PowerShell'in filtrelemesinin potansiyelini göstermek için, bu listeden en kullanışlı operatörlerden bazıları aşağıda eklendi:


![image](https://github.com/user-attachments/assets/2490056a-8422-4e90-8752-b3a44f8050c7)

Aşağıda, nesnelerin belirli bir desene (-like) uyan özelliklerin seçilmesiyle de filtrelenebileceğini gösteren başka bir örnek bulunmaktadır:

Bir sonraki filtreleme cmdlet'i, Select-Object, nesnelerden belirli özellikleri seçmek veya döndürülen nesne sayısını sınırlamak için kullanılır. Çıktıyı yalnızca ihtiyaç duyulan ayrıntıları gösterecek şekilde iyileştirmek için kullanışlıdır.


![image](https://github.com/user-attachments/assets/bddfd507-3291-4e97-9e82-e3ae910ad1a2)


