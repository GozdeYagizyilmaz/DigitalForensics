### Özellikle çalışan işlemler, hizmetler ve etkin ağ bağlantıları gibi dinamik yönlerle ilgili daha gelişmiş sistem bilgileri toplamak için, statik makine ayrıntılarının ötesine geçen bir dizi cmdlet'ten yararlanabiliriz. 
Get-Process, CPU ve bellek kullanımı dahil olmak üzere şu anda çalışan tüm işlemlerin ayrıntılı bir görünümünü sağlar ve bu da onu izleme ve sorun giderme için güçlü bir araç haline getirir.

![image](https://github.com/user-attachments/assets/56722acd-964c-4668-87f9-379a9908a5a1)

Benzer şekilde, Get-Service, makinedeki hizmetlerin durumu hakkında, hangi hizmetlerin çalıştığı, durdurulduğu veya duraklatıldığı gibi bilgilerin alınmasına olanak tanır. Sistem yöneticileri tarafından sorun gidermede yaygın olarak kullanılır, ancak aynı zamanda sistemde yüklü anormal hizmetleri arayan adli tıp analistleri tarafından da kullanılır.

![image](https://github.com/user-attachments/assets/816779f5-a9bb-4964-9df3-72fda9080949)

Etkin ağ bağlantılarını izlemek için Get-NetTCPConnection geçerli TCP bağlantılarını görüntüler ve hem yerel hem de uzak uç noktalara ilişkin içgörüler sunar. Bu cmdlet, bir olay yanıtlama veya kötü amaçlı yazılım analizi görevi sırasında özellikle kullanışlıdır, çünkü saldırgan tarafından kontrol edilen bir sunucuya yönelik gizli arka kapıları veya yerleşik bağlantıları ortaya çıkarabilir.

![image](https://github.com/user-attachments/assets/bc48c8e4-42c2-4498-a36d-75f6121b3ba0)

Ayrıca, dosya karma değerleri oluşturmak için kullanışlı bir cmdlet olan Get-FileHash'ten de bahsedeceğiz. Bu cmdlet, özellikle olay müdahalesi, tehdit avcılığı ve kötü amaçlı yazılım analizinde değerlidir; çünkü dosya bütünlüğünü doğrulamaya ve olası kurcalamaları tespit etmeye yardımcı olur.

![image](https://github.com/user-attachments/assets/dd173953-3aba-4c9d-a10c-399208889c18)


## NOT: Bu cmdlet'ler toplu olarak gerçek zamanlı sistem izleme ve analizi için kapsamlı bir araç seti sunar ve özellikle olay müdahale ekipleri ve tehdit avcıları için oldukça faydalıdır.


