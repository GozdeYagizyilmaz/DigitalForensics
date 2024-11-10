Ev kullanıcılarının büyük çoğunluğu Windows sistemlerinde yerel yönetici olarak oturum açmıştır.
Bir kullanıcının, internette gezinme, Word belgesi üzerinde çalışma vb. gibi ayrıcalık gerektirmeyen görevleri çalıştırmak için sistemde yüksek (yükseltilmiş) ayrıcalıklarla çalışmasına gerek yoktur. Bu yükseltilmiş ayrıcalık, kötü amaçlı yazılımların sistemi enfekte etmesini kolaylaştırdığı için sistemin tehlikeye girme riskini artırır.

Yerel kullanıcıyı bu tür ayrıcalıklarla korumak için Microsoft, Kullanıcı Hesabı Denetimi'ni (UAC) tanıttı. Bu kavram ilk olarak kısa ömürlü Windows Vista ile tanıtıldı ve onu izleyen Windows sürümleriyle devam etti.

### UAC nasıl çalışır? 
Yönetici hesap türüne sahip bir kullanıcı bir sisteme giriş yaptığında, geçerli oturum yükseltilmiş izinlerle çalışmaz. Daha yüksek düzeyde ayrıcalıklar gerektiren bir işlemin yürütülmesi gerektiğinde, kullanıcıdan işlemin çalışmasına izin verip vermediğini onaylaması istenir.

Şu anda oturum açmış olduğunuz hesaptaki programa, yani yerleşik yönetici hesabına bir bakalım. Özelliklerini görüntülemek için sağ tıklayın.

Güvenlik sekmesinde, kullanıcıları/grupları ve bu dosyaya olan izinlerini görebiliriz. Standart kullanıcının listelenmediğine dikkat edin.

![image](https://github.com/user-attachments/assets/cdc152a4-6691-4263-a7c3-4ea805837add)

Bu kalkan simgesi, UAC'nin programı yüklemek için daha üst düzey ayrıcalıklara izin vermesini isteyeceğinin bir göstergesidir.

![image](https://github.com/user-attachments/assets/157275be-fa17-4a14-bd90-f3da9d26bac2)

Programa çift tıklayın ve UAC istemini göreceksiniz. Dahili yönetici hesabının zaten kullanıcı adı olarak ayarlandığını ve hesabın parolasını istediğini fark edin. 

![image](https://github.com/user-attachments/assets/f3719073-00e5-468c-be4f-5b37bd83b6a1)

Bir süre sonra, bir parola girilmezse, UAC istemi kaybolur ve program yüklenmez.  Bu özellik, kötü amaçlı yazılımın sisteminizi başarıyla tehlikeye atma olasılığını azaltır
