# Windows'ta Prefetch dosyalarının Adli Analizi

## Prefetch Dosyaları Nedir ?

Prefetch dosyaları, bir sistemde çalıştırılan uygulamaları analiz etmeye çalışan adli tıp araştırmacıları için harika eserlerdir.Bir uygulama belirli bir konumdan ilk kez çalıştırıldığında Windows bir Prefetch dosyası oluşturur.
Bu, uygulamaların yüklenmesini hızlandırmaya yardımcı olmak için kullanılır. Araştırmacılar için bu dosyalar, kullanıcının bilgisayardaki uygulama geçmişine ilişkin bazı değerli veriler içeriyor.

## Prefetch Dosyalar Nerede Bulunur ?

![image](https://github.com/user-attachments/assets/6eb5fbbb-8d96-4d23-a2c0-6f2c3f3d63a0)


## Önceden getirilen(Prefetch) dosyalar dijital adli tıp araştırmanız için neden önemlidir?

Programın yürütülmesine ilişkin kanıtlar adli araştırmacılar için değerli bir kaynak olabilir. Bir şüphelinin olası bir yanlışı örtbas etmek için CCleaner gibi bir program çalıştırdığını kanıtlayabilirler.
Program o zamandan beri silinmişse, yürütme kanıtı sağlamak için sistemde hala bir prefetch dosyası mevcut olabilir.

Prefetch dosyalarının bir diğer değerli kullanımı, inceleme yapanların kötü amaçlı bir programın ne zaman çalıştırıldığını belirlemesine yardımcı olabilecek kötü amaçlı yazılım araştırmalarıdır.

Bunu bazı temel zaman çizelgesi analizleriyle birleştiren araştırmacılar, sisteme indirilen veya oluşturulan ek kötü amaçlı dosyaları tanımlayabilir ve bir olayın temel nedeninin belirlenmesine yardımcı olabilir.

## Perfetch dosyalarını araştırırken bulunması gereken önemli yapılar

Prefetch dosyalarının tümü, uygulamanın adının, ardından uygulamanın çalıştırıldığı konumun sekiz karakterlik karmasının ve ardından  .PF uzantısının listelendiği ortak bir formatta adlandırılır.
Örneğin, Snipping Tool (SNIPPINGTOOL.EXE) uygulamasının ön getirme dosyası SNIPPINGTOOL.EXE-9A9B0B31.pf olarak görünecektir,burada 9A9B0B31, dosyanın yürütüldüğü yolun karmasıdır. Bu dosyaların tümü ROOT/Windows/Prefetch klasöründe saklanır.

## Prefetch dosyalarını analiz etmek nispeten basittir. İçerik şunları içerir:

* **File Name(Dosya adı):** Yürütülebilir dosyanın adı.
* **Timestamps(Zaman damgaları):** Yürütülebilir dosyanın ne zaman çalıştırıldığına ilişkin bilgiler.
* **Run Counts(Çalıştırma sayıları):** Yürütülebilir dosyanın yürütülme sayısı.
* **File and directory paths(Dosya ve dizin yolları):** Yürütülebilir dosyanın eriştiği dosyalar ve dizinler hakkında ayrıntılar

## Magnet Axiom ile Prefetch dosya analizini kolaylaştırma

Magnet Axiom, hızlı bulma ve inceleme için Windows'un tüm sürümlerinden Prefetch dosyaları ayrı bir yapı kategorisine ayrıştırır.Aşağıdaki ekran görüntüsü (ayrıştırılmış bir Windows 11 görüntüsünden), önceden getirme yapıtı için bir arama sonucunu gösterir (yukarıda başvurulan ve gösterilen aynı SNIPPINGTOOL.EXE dosyası).
Magnet Axiom, Prefetch dosyasında yer alan zaman damgalarını ve ek ayrıntıları toplayıp düzenledi ve ayrıca bunları araştırmacıya okunması kolay bir formatta bildirdi:

![image](https://github.com/user-attachments/assets/bcde690a-b857-4033-95a6-178f1fe6b5a4)

* **1-Uygulamanın orijinal yolunun karması**
* **2-Uygulama adı**
* **3-Uygulamanın çalıştırılma sayısı**
* **4-Uygulamanın son sekiz kez çalıştırıldığı zaman damgaları**

### Önceden getirme dosyaları, araştırmacıların bir kullanıcının belirli bir zamanda sistemde ne yaptığını anlamalarına yardımcı olan birçok Windows işletim sistemi eserinden yalnızca biridir.Bir olayın veya soruşturmanın büyük resmini ortaya çıkarmak için tüm Windows işletim sistemi eserleri birlikte incelenmelidir.

### Kaynak : https://www.magnetforensics.com/blog/forensic-analysis-of-prefetch-files-in-windows/
