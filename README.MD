Merhaba

İlk deneyim gibi baştan kurulum yaparak not almaya çalışacağım kurulumda bir kaç önemli faktör var,

özellikle NDK (Native C++) kullanacaksak kurulumu baştan yapmak en iyisi.

Benim kullandığım işletim sistemi Ubuntu 16 Linux, windows'a göre daha sorunsuz ve güvenli geliyor bana zaten android studio hemen hemen windows ile aynı çalışıyor sorun olacağını düşünmüyorum.

Öncelikle&nbsp;[Android Studio'u](https://developer.android.com) indirelim.

![2016](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-14-32-57-ekran-görüntüsü.png)

<span style="color: #0000ff;">android-studio-ide-XXX.XXXXXXX-linux.zip</span> şeklinde zip olarak bize ulaşacak,

içindeki "android-studio" klasörünü **"/home/<user>/android/"** klasörüne çıkartıyoruz.

64 Bit işletim sisteminde;

<span class="pln">lib32z1, lib32ncurses5, lib32bz2</span><span class="pun">-</span><span class="lit">1.0,</span><span class="pln"> lib32stdc</span><span class="pun">++</span><span class="lit">6 &nbsp;son sürüm olarak,</span>

gerekebilir varsa silip tekrar kurmakta fayda var android studio çalışırsa hiç dokunmayın.

Android Studio'nun ana dizininde uygulama klasörüne gelin **"/home/<user>/android/android-studio/bin"**

ve uçbirim açarak (sağ tık uçbirim aç) şu komutla android studio çalıştır "./studio.h"

Eğer "JDK Not Found","JAVA Development Kit Not Found","JDK old please update" gibi JDK yok hatası alırsanız

UBUNTU İÇİN terminali açıyoruz:

öncelikle eski sürüm javaları kaldırıyoruz aşağıdakileri terminale yapıştırın.

"sudo apt-get remove oracle-jdk7-installer"

"sudo apt-get remove oracle-java7-installer"

"sudo apt-get remove openjdk-8-jdk"

"sudo apt-get remove openjdk-7-jdk"

ve en son sürüm Oracle JDK 8 yüklüyoruz.

<span style="font-size: 16px;">"sudo apt-get install oracle-jdk8-installer"</span>

kurulum bitince alternatif seçimini yapıyoruz

"sudo update-alternatives --config java"

![2016-08-29 15-41-18 ekran görüntüsü](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-41-18-ekran-görüntüsü.png)

ve JDK hazır.

<span style="font-size: 16px;">Programı çalıştırıyoruz "./studio.sh", açılan pencerede ;</span>

![2016-08-29 15-03-01 ekran görüntüsü](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-03-01-ekran-görüntüsü.png)

resimdeki gibi işaretlenmiş olacak ve <span style="color: #ff0000;">OK</span> deyip devam ediyoruz.

Karşımıza kurulum sihirbazı çıkacak

[![2016-08-29 15-06-24 ekran görüntüsü](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-06-24-ekran-görüntüsü.png)](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-06-24-ekran-görüntüsü.png)

<span style="color: #ff0000;">Next</span> diyor ve sonraki adımda <span style="color: #ff0000;">"Standart Kurulum"</span> seçili şekilde <span style="color: #ff0000;">Next</span> diyor devam ediyoruz.

Aşağıdaki manzara eğer "/home/<user>/android/Sdk" diye bir klasör yoksa yani "Android Sdk" yüklü değil ise karşımıza çıkacak

![2016-08-29 15-12-51 ekran görüntüsü](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-12-51-ekran-görüntüsü.png)

<span style="color: #ff0000;">Next</span> diyor ve bir sonraki yani son adıma geçerek <span style="color: #ff0000;">Finish</span> diyoruz ve "Android Sdk" indirme işlemi başlıyor.

![2016-08-29 15-15-18 ekran görüntüsü](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-15-18-ekran-görüntüsü.png)

indirme işlemi bitince tekrar <span style="color: #ff0000;">Finish</span> diyoruz ve kurulum bitiyor.

![2016-08-29 15-19-24 ekran görüntüsü](http://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-19-24-ekran-görüntüsü.png)

Eğer böyle bir hata alırsanız da sol altta gördüğünüz <span style="color: #ff0000;">Configure</span> ye tıklayarak

açılan menüden <span style="color: #ff0000;">Project Defaults</span> a tıklayıp <span style="color: #ff0000;">Project Structure</span> yi seçiyoruz

![2016-08-29 15-22-48 ekran görüntüsü](http://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-22-48-ekran-görüntüsü.png)

Açılan pencereden Sdk Klasörünü "/home/<user>/android/Sdk" seçiyoruz.

![2016-08-29 15-26-04 ekran görüntüsü](https://github.com/quvven/android-studio-setup-ndk/tree/master/uploads/2016/08/2016-08-29-15-26-04-ekran-görüntüsü.png)

OK diyoruz ve sorun çözülüyor. ve Kurulum Bitti:)
