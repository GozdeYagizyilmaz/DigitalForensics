## CLI açıklama sözdizimi kuralları

#### Bir CLI'nin belgelerini veya bir "man" sayfasını okurken, muhtemelen komutları, bunların argümanlarını ve seçeneklerini (genellikle "Özet" altında bulunur) tanımlamak için kullanılan belirli bir sözdizimiyle karşılaşacaksınız.

### 1- Gerekli Parametreler

**Gerekli parametreler genellikle sadece parametrenin adı kullanılarak temsil edilir, ancak bazı durumlarda bunları köşeli ayraçların arasında bulabilirsiniz:**

* **dotnet new <template>:** Şablon belirtmeden yeni bir dotnet projesi oluşturamayız.
* **mv kaynak hedef:** Bir dosyayı/dizini taşırken kaynak ve hedef parametrelerini belirtmeliyiz.

### 2- İsteğe Bağlı Parametreler

**İsteğe bağlı parametreler en yaygın olarak köşeli parantezler kullanılarak temsil edilir:** 

**mycli komutu [isteğe bağlıParametre]**

* ![image](https://github.com/user-attachments/assets/5cc18a97-8235-4f6c-bee7-35e0579c1ae3)  **Komutun davranışını değiştirmek için bazı bayraklar ve seçenekler ekleyebiliriz.**

* ![image](https://github.com/user-attachments/assets/d84fe307-324a-4199-9506-5055a49ce2ae)  **Her git uzaktan kumandası hakkında daha fazla bilgi almak için -v veya --verbose komutunu kullanabiliriz.**

### 3- Çok sayıda değer alabilen argümanlar

**Üç nokta, argümanın/seçeneğin birçok değer beklediğini gösterir. İsteğe bağlı veya gerekli parametrelere uygulanabilir İsteğe bağlı parametrelere uygulanmış gibi görünmesi şu şekildedir:**

![image](https://github.com/user-attachments/assets/50a7524a-6e0e-4ac5-a7ba-fc0cda5ff4c5)

**Önceki ifade bize parametremizin 0'dan N'ye kadar değerler beklediğini söylüyor. Birçok değer alan gerekli parametreler genellikle iki yoldan biriyle temsil edilir. İşte onlardan biri:**

![image](https://github.com/user-attachments/assets/7f842bed-4532-45b4-8a52-08e7860aaeb9)

**Bu ifade bize, komutun <myParameter> için en az tek bir değer aldığını ancak aynı zamanda [myParameter...] ile temsil edilen ve 1'den N'ye kadar değerlerle temsil edilen daha fazla değer alabileceğini söyler. İşte Docker CLI'den bir örnek:**

![image](https://github.com/user-attachments/assets/6ec63535-5227-4144-8714-5acb47fff268)

**Start komutunu çalıştırırken en az bir konteyner belirtmemiz gerekiyor ancak aynı komutta birden fazla konteyner de başlatabiliriz. Gerekli parametreleri 1'den N'ye kadar birçok değerle temsil etmenin ikinci yolu aşağıdaki gibidir:**

![image](https://github.com/user-attachments/assets/fd882fc3-cbce-4338-8f96-3a510a0e03f2)  yada  ![image](https://github.com/user-attachments/assets/7ca09b6c-237a-4b4f-886e-91f57cdb4844)

**Köşeli parantez kullanmadığımız için myParameter'ın gerekli olduğu açıktır, bu da en az bir değere (1'den N'ye) ihtiyaç duyduğunu gösterir. İşte bir örnek:**

![image](https://github.com/user-attachments/assets/e015b090-c56a-4c16-a0d3-dc4b6e991f73)

**Mkdir kullanırken oluşturulacak en az bir dizin belirtmemiz gerekiyor ancak birden fazla dizin de oluşturabiliriz.**

### 4- Birbirini dışlayan argümanlar

**Bazı argümanlar aynı komutta birlikte kullanılamaz. Özel ilişkileri borular kullanılarak temsil edilir:**

![image](https://github.com/user-attachments/assets/a426265c-c7fc-421b-b17e-ece2304e7669)

**Köşeli parantezler bize bu seçeneklerden hiçbirini kullanmak zorunda olmadığımızı söyler ve boru bize bunları kullanmaya karar verirsek ikisini aynı anda kullanamayacağımızı söyler. Yani aşağıdakilerden herhangi biri geçerlidir:**

![image](https://github.com/user-attachments/assets/7e9db34e-95ad-466f-955c-d69ba7b05730)

**Ancak aşağıdakiler geçersiz olacaktır:**

![image](https://github.com/user-attachments/assets/3c14884a-4233-4cf7-9933-54ab0565e888)

**git commit'ten bir örnek:**

![image](https://github.com/user-attachments/assets/27299989-3709-49c6-bd66-261ec7ed9609)

**Önceki ifade bize bu bayraklardan herhangi birini (-a, --interactive veya --patch) kullanabileceğimizi ancak birlikte kullanamayacağımızı söylüyor Ayrıca köşeli parantezler, bunlardan herhangi birini kullanmamaya da karar verebileceğimizi gösteriyor.**
**-a ve --patch'i birlikte kullanmaya çalıştığımızda şöyle olur:**

![image](https://github.com/user-attachments/assets/55d7b4c5-372d-4086-8a6a-2f23695e0293)

**Bu sözdizimi genellikle takma adları temsil etmek için kullanılır: git uzaktan [ - v | --ayrıntılı] Her iki bayrak da ayrı ayrı geçerlidir ancak bunları aynı anda kullanmak mantıklı değildir.**
**Benzer şekilde en az bir seçeneğin dahil edilmesi gereken durumlar da vardır. Bu durumlarda dikey çubuklar kullanırız ve parametreleri küme parantezleri veya parantezleri kullanarak şu şekilde gruplandırırız:**

![image](https://github.com/user-attachments/assets/e4898824-e95d-44ab-bc68-94f2521828ac)

**Kıvrımlı parantezler veya parantezler en az bir seçeneğin dahil edilmesi gerektiğini belirtir.**

![image](https://github.com/user-attachments/assets/7ab6fefc-9bc4-4bc0-aba2-c8bae6ad16f6)

**Parantez bu seçeneklerden en az birini seçmemiz gerektiğini belirtir Borular bize iki veya daha fazlasını seçemeyeceğimizi söylüyor Gerekli seçeneklerden herhangi birini kullanmazsak şu hatayı alırız:**

![image](https://github.com/user-attachments/assets/8c170fe0-e5ef-4d40-8600-65a5aa2010d3)























