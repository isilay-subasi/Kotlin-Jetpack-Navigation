# Kotlin-Jetpack-Navigation


<h2>Uygulama Elementleri</h2> 

+ Activities 
+ Services -> Arka planda çalıştıracağımız işlemler için kullanılır
+ Broadcast Receivers(Yayın Alıcılar) -> Uygulamaların birbirleriyle haberleşmesini ve uygulama içerisindeki haberleşmeyi daha iyi yönetebilmek için kullanılır. 
+ Content Providers(İçerik Sağlayıcılar) -> Bir uygulamadan başka bir uygulamaya ya da uygulama içerisindeki bir veri sağlanacaksa bu veriyi daha iyi ele alabildiğimiz bileşendir.

Endüstride daha yeni bileşenlerle çalışılmak isteniyor.SQLite kullanarak veritabanı oluşturmak yerine Room veritabanını,framework kullanarak işlemleri yapmak çok daha avantaj sağlıyor.
<hr>
<h2>Android Jetpack</h2><br>
Farklı farklı kütüphaneler,araçlar ve framewoklere sahip topluluk.Yüksek kaliteli uygulamaları daha kolay yapmamıza olanak tanır.

+ Room
+ ViewModel -> MVVM mimari yapı.
+ Navigation -> Intentle yaptıgımız işlemleri daha kolay yapabilmemiz için.
+ LiveData ->Canlı veriyi nasıl tutacağımızı
+ Data Binding -> UI ile verimizi nasıl daha iyi bağlayacağımızı


<h2>Jetpack Navigation</h2>

Fragmentler arası geçişlerde activiteler arası geçişlerde daha kolay şekilde yapmamızı sağlayan yapıdır.Bir kütüphane gibi düşünebiliriz.
Bir örnek projeyle bu konuyu daha iyi öğrenelim.
Empty project oluşturuyoruz.

+ 2 tana fragment oluşturuyoruz.(Blank)
+ 2 fragment ve 1 activiteden oluşan bir projemiz oluştu.
+ fragment_first.xml kısmında layout tagleri arasına FrameLayout taglerini koyuyorum.
layout -> İçerisindeki FrameLayout navigasyonun bir parçası olduğunu söylüyor.
+ Ama ilk başta dependencies olarak eklemem gereken ilgili kodları ekliyorum.
Module:app -> dependencies -> 
  def nav_version = "2.4.0-rc01"
  implementation("androidx.navigation:navigation-fragment-ktx:$nav_version")
  implementation("androidx.navigation:navigation-ui-ktx:$nav_version")
+ FrameLayout icindeki ilk iki satir "xmlns" -> namespacedir.
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
Bu namespacelerin ilk tagin içerisinde olması gerekir. Onun için layout tagleri arasına alıyoruz.

+ Navigasyon Grafiği -> Fragmentlerin ve aktivitlerin nasıl birbirine bağlayacağımızı belirteceğimiz grafik.
res -> new -> Android Resource File -> Resource Type -> navigation seçiyoruz.
my_navigation.xml adında bir dosya hazırlıyoruz.

![action](https://github.com/isilay-subasi/Kotlin-Jetpack-Navigation/blob/main/images/action.PNG)

+ Activitemizle navigasyonda yaptıklarımızı bağlamam gerekiyor.
+ activity_main geliyorum. Ve <b>navHostFragment<b> viewini seçiyorum.Oluşturduğum grafiği burda host etmek için, burda barındırmak için kullandığımız görünüm elemanıdır.

![navHostFragment](https://github.com/isilay-subasi/Kotlin-Jetpack-Navigation/blob/main/images/navigasyon.PNG)




  



