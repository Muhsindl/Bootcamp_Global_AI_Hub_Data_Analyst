# Electric Motor Temperature


![image](https://static.vecteezy.com/system/resources/thumbnails/028/197/869/small_2x/liquid-transfer-pump-with-asynchronous-electric-motor-modern-chemical-industrial-equipment-in-an-oil-refinery-petrochemical-plant-ai-generated-free-photo.jpg)


Bu proje, Elektrikli motor sıcaklıklarının farklı bileşenlerdeki etkisini analiz ederek verilerin görselleştirmesini ele almıştır.

# Proje Özeti
13 sütundan oluşan 695275 veri incelenmiştir.
Analiz edilen verisetinde NaN değer bulunmamaktadır.
Öncesinde NaN değerler eklenip analiz edildi daha sonra veri ön işleme adımında tekrar NaN değerler silindi.
Veriseti;

*u_q :* Voltaj q-bileşeni ölçümü dq-koordinatlarında (V cinsinden)

*coolant :* Soğutucu sıcaklığı (°C cinsinden)

*stator_winding :* Stator sargı sıcaklığı (°C cinsinden) termokupllarla ölçülmüştür

*u_d :* Voltaj d-bileşeni ölçümü dq-koordinatlarında

*stator_tooth :* Stator diş sıcaklığı (°C cinsinden) termokupllarla ölçülmüştür

*motor_speed :* Motor hızı (dev/dak cinsinden)

*i_d :* Mevcut d-bileşeni ölçümü dq-koordinatlarında

*i_q :* Mevcut q-bileşeni ölçümü dq-koordinatlarında

*pm :* Kalıcı mıknatıs sıcaklığı (°C cinsinden) termokupllarla ölçülmüştür ve bir termografi ünitesi aracılığıyla 
kablosuz olarak iletilmiştir.

*stator_yoke :* Stator boyunduruğu sıcaklığı (°C cinsinden) termokupllarla ölçülmüştür

*ambient :* Ortam

*torque :* Tork

*profile_id :* Id

gibi bilgileri içermektedir.


# Çalışmada Uygulanan Adımlar
# 1. Veri İncelemesi ve Ön İşleme
- Veri setinde eksik değer bulunmamaktadır.
- Sıcaklık, tork, voltaj gibi farklı değişkenler arasındaki ilişkiler incelenmiştir.
- Aykırı değerler tespit edilerek gerekli düzenlemeler yapılmıştır.
- Değişkenler normalize edilmiştir.

# 2. Veri Analizi
- Sıcaklık ölçümlerinin motor hızına ve torka etkisi analiz edilmiştir.
- Voltaj ve akım bileşenlerinin (u_d, u_q, i_d, i_q) motor performansı üzerindeki etkileri değerlendirilmiştir.
- Zaman serisi analizleri ile motor sıcaklık bileşenleri arasındaki ilişkiler görselleştirilmiştir.

# 3. Görselleştirme
- Korelasyon Matrisi 
- Seaborn
- Matplotlib
  

# Elde Edilen Bulgular
# 1. Motor Performansı
- Kalıcı mıknatıs sıcaklığı (pm), motor hızından ve stator sıcaklıklarından büyük ölçüde etkilenmektedir.
- Voltaj ve akım bileşenlerinin tork üzerinde güçlü bir etkisi vardır.
- Motor performansı üzerinde en önemli değişkenler sırasıyla tork, stator sıcaklıkları ve motor hızı olarak belirlenmiştir.

# 2. Isı Yönetimi
- Stator diş sıcaklığı ve soğutucu sıcaklık arasındaki ilişki, motorun termal stabilitesini korumak için kritik bir rol 
  oynamaktadır.
- Yüksek hızda çalışan motorların, soğutucu sıcaklığının belirli bir seviyede tutulması ile performans kaybı minimize 
  edilebilir.

# 3. Zaman Serisi Analizi
- Sıcaklık artışları motor hızındaki ani değişimlerle ilişkilidir.
- Motor sıcaklıklarının zaman içindeki davranışlarını tahmin etmek, aşırı ısınmayı önlemek için erken uyarı sistemlerinin 
  geliştirilmesini mümkün kılar.


# Problemin İşlevsel Kullanımı ve Çözüm Önerisi
# Problem
Motor sıcaklık bileşenleri, elektrik motorlarının performansı ve ömrü üzerinde doğrudan etkilidir. Ani sıcaklık artışları motor arızalarına yol açabilir. Bu veri seti, elektrikli motorların sıcaklıklarını izleyerek performansı optimize etmeye yönelik bir tahmin modeli oluşturmak için kullanılabilir.

# Kullanım Alanı
- *Elektrikli Araç Üreticileri:* Elektrikli araç motorlarının sıcaklık yönetimini optimize ederek enerji verimliliğini 
  artırabilir ve aşırı ısınmayı önleyebilir.
- *Sanayi Motorları:* Endüstriyel motorlarda arıza öncesi tahmin yaparak bakım maliyetlerini azaltabilir.
- *IoT Uygulamaları:* Sensörlerle entegre bir sistem geliştirerek motor sıcaklıklarını gerçek zamanlı izleme ve kontrol 
  mekanizmaları kurulabilir.

# Önerilen Model ve Algoritmalar
- *XGBoost:* Özellikle büyük veri setlerinde ve karmaşık ilişkilere sahip değişkenlerde yüksek performans gösterir. Bu model, sıcaklık değişimlerini tahmin etmek için uygundur.
- *LSTM (Uzun Kısa Süreli Bellek Ağları):* Motor sıcaklıklarının zaman içindeki davranışlarını modellemek ve gelecekteki 
  sıcaklık değerlerini tahmin etmek için kullanılabilir.
- *Random Forest Regressor:* Özellikle değişkenler arasındaki doğrusal olmayan ilişkilerin analizi için etkili bir 
 yöntemdir.


# Öneriler
- *Termal Yönetim Sistemi:* Motor sıcaklıklarını sürekli izleyen ve yüksek sıcaklık durumlarında uyarı veren bir sistem 
  geliştirilmelidir.
- *Model Entegrasyonu:* Seçilen ML modelinin IoT sensör sistemlerine entegre edilmesi, sıcaklık tahmini doğruluğunu 
  artıracaktır.
- *Enerji Verimliliği:* Motorun çalıştırılma parametreleri optimize edilerek enerji verimliliği sağlanabilir.

<hr>

#*Kaggle Bağlantısı:*

https://www.kaggle.com/code/muhsindolu/electric-motor-temperature
