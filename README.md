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

