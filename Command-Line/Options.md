## Options (SEÇENEKLER)

#### Seçenekler, bir komuta aktarılabilen ve anahtar/değer çiftleriyle temsil edilen adlandırılmış parametrelerdir. Konumsal argümanlardan farklı olarak konumları önemli değildir.

![image](https://github.com/user-attachments/assets/1aecbf3d-dac8-46a0-8bb6-d19d269375d5)

#### Seçenekler genellikle (her zaman değil) isteğe bağlı parametreleri temsil etmek için kullanılır. Çoğu durumda, eğer bir parametre gerekliyse, konumsal argüman en iyi yoldur.Bazı seçeneklerde, aynı seçeneğin kısa versiyonları olan, yazılması ve hatırlanması daha kolay olan takma adlar bulunur. Genellikle tek bir tire önekiyle tanımlanırlar:

![image](https://github.com/user-attachments/assets/4bd1e231-7fd0-4a85-a597-280a674d4bcf)

#### CLI'ye ve İşletim Sistemine bağlı olarak farklı sınırlayıcılar desteklenir. Bunlar en yaygın olanlardan bazılarıdır:

![image](https://github.com/user-attachments/assets/7c04bbe1-cb62-42ed-9327-047595b29b25)

## Flags (Değer Gerektirmeyen Seçenekler)

#### Değer gerektirmeyen seçeneklere genellikle Bayraklar adı verilir. Bunlar booleandır, yani varlıkları "doğru"yu, yoklukları ise "yanlış"ı belirtir. Bayrak kullanan bazı komut örnekleri:

![image](https://github.com/user-attachments/assets/6db8b1c6-193f-4451-ae26-9df11b2e83a2)

## The --help flag

#### Kullanıcılarımızı mevcut komutlar ve bunların argümanları ve seçenekleri hakkında bilgilendirmek GUI olmadan zor olabilir. İşte o zaman --help bayrağı devreye giriyor.Bir komutun ardından yardım bayrağını eklediğimizde CLI'den bize bu konuda daha fazla bilgi vermesini isteriz. Genellikle bu bilgiler komutun, argümanların, seçeneklerin ve takma adların kısa bir açıklamasını içerir.

![image](https://github.com/user-attachments/assets/e5f58129-3682-4c99-b11b-64206a2901dc)

#### --help bayrağının yaygın takma adları:

![image](https://github.com/user-attachments/assets/adb67e08-dfbf-430b-aa8d-a6262b43fd59)

## Ayrıntı seviyeleri

#### Bazı CLI'ler kullanıcının farklı düzeylerde yardım istemesine olanak tanır. Örneğin, dotnet CLI -h veya --help kullandığımızda kısa versiyonu, -H veya -HELP kullandığımızda ise uzun versiyonu yazdıracaktır.

![image](https://github.com/user-attachments/assets/c139e626-b5b1-415d-8628-310f80d04701)

#### Benzer şekilde, git CLI, -h kullandığımızda nasıl kullanılacağını kısaca açıklayan komutun bir özetini yazdırır, ancak --help kullandığımızda çevrimdışı HTML belgelerine yönlendirir:

![image](https://github.com/user-attachments/assets/93ca50bc-ef03-46b8-b310-8fd0c5cc1275)

## Help(Yardım)Komutu

#### Bazı CLI'ler genellikle --help bayrağından daha ayrıntılı bilgi veren bir yardım komutu da sağlar:

![image](https://github.com/user-attachments/assets/a9fb9a91-3250-49eb-9f52-27d63ba29571)

#### Örneğin, hem dotnet CLI hem de npm CLI, help komutunu kullandığımızda bir tarayıcı açacak ve sizi komutun tüm belgelerine yönlendirecektir:

![image](https://github.com/user-attachments/assets/76ae0332-0c56-4bc6-9ced-7b4f43c09010)





