# Giriş: "Hello, World!" Programı Nedir?

Çoğu programlama diline başlarken ilk örnek, "Hello, World!" programıdır. 
Bu basit ve kısa program, ekrana "Hello, World!" yazdırarak sonlanır. 
Bu program, o dilin temel kavramlarını tanıtmak açısından büyük önem taşır.

## 1. D Dilinde "Hello, World!" Programı

Aşağıda D dilinde yazılmış bir "Hello, World!" programı örneği bulunmaktadır:

```d
import std.stdio;

void main() {
    writeln("Hello, World!");
}
```

Yukarıdaki kaynak kodu, bir D derleyicisi tarafından derlenerek çalıştırılabilir bir program haline getirilmelidir.

## 2. D Derleyici Kurulumu

Bu bölümde, D dilini kullanmak için gerekli olan derleyicilerin nasıl kurulacağına dair bilgiler verilecektir. 

D programlama dili için üç farklı D derleyicisi:

- dmd: Digital Mars derleyicisi
- gdc: GCC’nin D derleyicisi
- ldc: LLVM derleyici altyapısını hedefleyen D derleyicisi

DMD, dilin tasarım ve geliştirilmesinde yıllar boyunca kullanılan derleyicidir. 
Burada tüm örnekler 'dmd' ile test edilmiştir. 
Bu nedenle, başlamak için dmd’yi tercih etmeniz en kolay yol olacaktır. 
Diğer derleyicilere yalnızca belirli bir ihtiyacınız varsa yönelmelisiniz. 

## 2.1 DMD Kurulumu

En güncel dmd sürümünü kurmak için Digital Mars’ın [indirme sayfasına](https://dlang.org/download.html) gidin ve bilgisayar ortamınıza uygun derleyici sürümünü seçin. 
İşletim sisteminiz ve paket yönetim sisteminiz ile uyumlu dmd sürümünü seçmelisiniz; 
ayrıca 32-bit veya 64-bit CPU ve işletim sistemine sahip olup olmadığınızı belirtmelisiniz. 

Not: D1 derleyicisini kurmaktan kaçının.

Kurulum adımları farklı ortamlarda değişiklik gösterebilir, ancak genellikle basit ekran talimatlarını takip etmek ve birkaç butona tıklamak kadar kolaydır.

## 3. Kaynak Dosyası Nedir?

Programcıların D derleyicisi için yazdığı dosyaya kaynak dosyası denir. 
D genellikle derlenen bir dil olduğu için kaynak dosyası kendiliğinden çalıştırılabilir bir program değildir. 
Derleyici tarafından çalıştırılabilir bir programa dönüştürülmesi gerekmektedir.

Her dosya gibi, kaynak dosyasının da bir adı olmalıdır. 
Dosya adı dosya sisteminde yasal olan herhangi bir şey olabilir; ancak, .d uzantısı kullanmak yaygın bir uygulamadır.
Bu, geliştirme ortamları, programlama araçları ve programcılar tarafından beklenmektedir.
Örneğin, test.d, oyun.d, fatura.d gibi isimler uygun D kaynak dosyası adlarıdır.

# Programlama Dili ile "Hello, World!" Programını Derleme

## 1. Giriş: "Hello, World!" Programı Nedir?

"Hello, World!" programı, birçok programlama dilinde yazılışına başlanan ilk örnektir. 
Bu basit program, ekrana "Hello, World!" yazdırarak dilin temel özelliklerini tanıtır. 
D programlama dili ile bu programı yazmak oldukça kolaydır.

## 2. Kaynak Dosyasını Oluşturma

İlk adım olarak, bir metin editörü veya IDE kullanarak kaynak dosyanızı oluşturmalısınız. 

Aşağıdaki adımları izleyin:

1. Bir metin editörü açın.

2. Aşağıdaki kodu kopyalayın veya yazın:

```d
import std.stdio;

void main() {
    writeln("Hello, World!");
}
```

3. Dosyayı hello.d adıyla kaydedin.

## 3. Programı Derleme

D derleyicisi ile programınızı derlemek için aşağıdaki adımları izleyin:

3.1 Terminali Açma

1. Terminal penceresini açın.
2. hello.d dosyasını kaydettiğiniz dizine gidin.

3.2 Derleme Komutunu Girme

Aşağıdaki komutu terminale yazın:

```bash
dmd hello.d
```

Eğer hata almadıysanız, her şey yolunda demektir. 
Derleyici, hello (Windows'ta hello.exe) adında bir çalıştırılabilir dosya oluşturmuş olmalıdır.

Resim :

![Resim](https://iili.io/dsNDsBn.png)

3.3 Hataları Düzeltme

Eğer derleyici hata mesajları verdiyse, muhtemelen kodu kopyalarken bir hata yaptınız. 
Hataları bulup düzeltin ve derlemeyi tekrar deneyin. 
Programlama sırasında hatalar yapmanız oldukça normaldir; düzeltme ve derleme süreci zamanla alışkanlık haline gelecektir.

3.4 Programı Çalıştırma

Program başarıyla oluşturulduktan sonra, aşağıdaki komutu yazarak çalıştırabilirsiniz:

```bash
hello.exe
```

Ekranda "Hello, World!" mesajını görmelisiniz. Tebrikler! İlk D programınız başarıyla çalıştı.

Resim : 

![Resim](https://iili.io/dsNLXPj.png)

## 4. Derleyici Seçenekleri

D derleyicisi, programın nasıl derleneceğini etkileyen birçok komut satırı seçeneğine sahiptir. 
Derleyici seçeneklerini görmek için sadece derleyicinin adını girin:

```bash
dmd
```

Bu komut, derleyici hakkında bilgi verecek ve kullanılabilir seçenekleri listeleyecektir.

Resim : 

![Resim](https://iili.io/dsOKBXj.png)

## 4.1 Önerilen Seçenekler

Aşağıda önerilen bazı seçenekler bulunmaktadır:

- -de: Kullanımdan kaldırılmış özellikleri hata olarak gösterir.
- -unittest: Birim testlerini derler.
- -w: Uyarıları hata olarak gösterir.

Aşağıdaki komut, bu seçenekleri kullanarak programınızı derlemenizi sağlar:

```bash
dmd hello.d -de -w -unittest
```

## 4.2 Tek Komutla Derleme ve Çalıştırma

-run seçeneği ile hem derleme yapabilir hem de programı tek bir komutla çalıştırabilirsiniz. 
Bu seçeneği kullanmak için en son yazmanız gereken komut:

```bash
dmd -de -w -unittest -run hello.d
```

Bu komut, programı otomatik olarak çalıştıracak ve "Hello, World!" mesajını gösterecektir.

Resim : 

![Resim](https://iili.io/dsOx78Q.png)
