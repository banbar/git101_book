# 1.6. Remote bir proje oluşturmak

Versiyon kontrolü Git ile yapılan bir projede yer alıyorsanız *remote repository*'lerinizi nasıl yöneteceğinizi de öğrenmeniz gerekiyor. Remote repository'leri projelerinizi internet'de veya sınırlı erişime izin verilen şirket ağında yer alan versiyonları olarak düşünebilirsiniz.

Diğer ekip üyeleri ile birlikte verimli çalışabilmek,  onların yaptığı değişiklikleri kendi yerel çalışma alanınıza almak, kendi yaptığınız değişiklikleri onlar ile paylaşabilmek için remote repository'lerinizi doğru ve etkin bir şekilde yönetmelisiniz.

Git ile versiyon kontrolü yapılan bir projeye dahil olduğunuzda size verilecek ilk bilgiler projenin adresi (URL) ve projeye erişim için kullanacağınız kullanıcı adınız ve şifrenizdir. Uzaktaki bir repository'nin (URL) adresi aşağıdaki formatlardan birinde olacaktır

* ssh://user@server/git-repo.git
* kullanıcıadı@sunucuadı:git-repo.git
* http://example.com/git-repo.git
* https://example.com/git-repo.git
* git://example.com/git-repo.git

Bu adres formatlarından ilk iki tanesi [SSH](http://en.wikipedia.org/wiki/Secure_Shell) (Secure Shell) protokolüne karşılık gelir. http:// ve https:// protokolleri ise normal internet erişimi için de kullanılan protokollerdir. Son format ise git'in kendi protokolüne karşılık gelir.

Remote repository'nizin adresini ve erişim için gerekli kullanıcı adınızı ve şifrenizi öğrendikten sonra yapmanız gerken tek şey bu adresten projenizin dosyalarını yerel diskinize klonlmak. Bunun için öncelikle yerel diskinizde projenizi indireceğiniz bir klasör oluşturmanız ve Terminal'den bu klasöre gitemeniz gerekiyor.Sırasıyla aşağıdaki komutları Terminal'de yazınız

![Boş Klasör Oluşturma](./01_emptyprojectdir.png "Boş Klasör Oluşturma")

Yukarıdaki ekran görüntüsünde yer alan ilk olan **cd** komutu ile proje klasörümü oluşturacağım ana klasör olan **Projects** klasörüne konumlanıyoruz. İkinci komut olan **mkdir** ile proje klasörümüz olan **git101_kitap** klasörünü oluşturuyoruz. Üçüncü komutumuz ile de yeni oluşturduğumuz **git101_kitap** klasörüne konumlanıyoruz.

Yerel diskimizde boş proje klasörümüzü oluştruduğumuza göre şimdi remote repository'mizi yerel klasörümüze **git clone** komutu ile indirebiliriz.

![Remote repository'yi klonlama](./02_cloneremote.png "Remote repository'yi klonlama")


> Kullanıcı adınızı ve şifrenizi vererek remote repository'yi klonlamak için aşağıdaki **git clone** komutuna bu bilgileri aşağıdaki formatta vermeniz gerekiyor

> git clone https://kullanıcıadı:şifre@github.com/username/repository.git