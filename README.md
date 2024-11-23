# depresyon_dataset_eda_Buket_Kalfa
Veri Kümesi Hakkında

[Kaggle Linki] (https://www.kaggle.com/code/buketkalfa/depresyon-dataset-eda)

## Veri Kümesi Genel Bakış (Sentetik):

Bu veri kümesi, bireylerin kişisel ve yaşam tarzı faktörleriyle ilgili çeşitli özelliklerini içermektedir. Sağlık, yaşam tarzı ve sosyo-ekonomik durum gibi alanlarda analiz yapmayı kolaylaştırmak için tasarlanmıştır.
## Özellikler


Name: Bireyin tam adı.

Age: Bireyin yaşı (yıl cinsinden).

Marital Status: Bireyin medeni durumu. Olası değerler: Single, Married, Divorced, Widowed.

Education Level: Bireyin elde ettiği en yüksek eğitim seviyesi. Olası değerler: High School, Associate Degree, Bachelor's Degree, Master's Degree, PhD.

Number of Children: Bireyin sahip olduğu çocuk sayısı.

Smoking Status: Bireyin sigara içme durumu. Olası değerler: Smoker, Former, Non-smoker.

Physical Activity Level: Bireyin yaptığı fiziksel aktivite düzeyi. Olası değerler: Sedentary, Moderate, Active.

Employment Status: Bireyin istihdam durumu. Olası değerler: Employed, Unemployed.
Income: Bireyin yıllık geliri (USD cinsinden).

Alcohol Consumption: Alkol tüketim düzeyi. Olası değerler: Low, Moderate, High.

Dietary Habits: Bireyin diyet alışkanlıkları. Olası değerler: Healthy, Moderate, Unhealthy.

Sleep Patterns: Uyku kalitesi. Olası değerler: Good, Fair, Poor.

History of Mental Illness: Bireyin mental hastalık geçmişi olup olmadığı. Olası değerler: Yes, No.

History of Substance Abuse: Bireyin madde bağımlılığı geçmişi olup olmadığı. Olası değerler: Yes, No.

Family History of Depression: Ailede depresyon geçmişi olup olmadığını belirtir. Olası değerler: Yes, No.

Chronic Medical Conditions: Bireyin kronik tıbbi durumları olup olmadığını belirtir. Olası değerler: Yes, No.

Kullanım Alanları

Bu veri kümesi, çeşitli sağlık, yaşam tarzı ve sosyo-ekonomik faktörlerin analizinde kullanılmak üzere tasarlanmıştır. Predictive modeling (tahmin modelleri), clustering (kümeleme) ve exploratory data analysis (keşifsel veri analizi) gibi görevler için uygundur.
[Kaggle Linki] (https://www.kaggle.com/code/buketkalfa/depresyon-dataset-eda)

## 1. Kütüphaneleri Yükleme İşlemi
## 2.Veri Setini Yükleme İşlemi ve Veri Hakkında Bilgiler
## 3. Veri Setinde Yapay Olarak Eksik Değerler Oluşturma
## 4. Eksik Veri Analizi
Veri seti içerisinde eksik değerler bulunması yapısal bir bozukluğa işaret eder ve mutlaka uygun yöntemlerle ele alınmalıdır.

Eksik veriler, duruma bağlı olarak veri setinden silinebilir veya uygun veriler ile doldurulabilir. Ancak eksik verilerin silinmesi, silinen satır veya sütunlar içerisinde yer alan diğer verilerin kaybedilmesi anlamına gelir. Eksik verilerin doldurulması işleminde ise, veri setine sentetik bir girdi yapacağımızdan dolayı, doldurma işlemleri veri setindeki dağılımları manipüle edebilir (veri setinde yanlılık oluşturabilir).

Eksik verilerin ne sebeple ortaya çıktığı hassas bir şekilde değerlendirilmeli, nasıl ele alınacağı da bu değerlendirme sonucunda uygun şekilde karar verilmelidir.
## 4.2 Yöntem 1: Eksik Verilerin Silinmesi
Veri setinde bulunan eksik verilere müdahale yöntemlerinden birisi, eksik verilerin silinmesidir. Uygulaması oldukça kolay bir yöntem olsa da eksik verileri silmeden önce dikkat edilmesi gereken önemli hususlar vardır.

Eksik bir verinin bulunduğu gözlemi silmeya karar verebilmek için, bu eksikliğin doğal olmayan bir şekilde ortaya çıktığından emin olmamız gerekir. Örneğin elimizdeki bir araç veri setinde elektrikli araçlar için motor hacmi kolonunda Na değer bulunması doğal bir eksikliğe işaret eder. Bu durumda silme işlemi yerine uygun bir şekilde doldurmak tercih edilebilir.

Eksik veriler veri setinde kayda değer bir yüzdeyi oluşturuyorsa, eksik verilerin silinmesi durumunda veri setindeki birçok gözlemi kaybedeceğimiz unutulmamalıdır. Bu durumda veri seti içerisinde bize bilgi sağlayabilecek birçok veriyi de kaybetmiş olacağız. Verinin olabildiğince fazla olması, hem analitik yöntemler hem de makine öğrenmesi yöntemleri için oldukça önemli olduğuna göre, veri setinden olabildiğince az kayıp verecek yöntemler denemeliyiz.
## 4.3 Yöntem 2: Eksik Verilerin Doldurulması
Eksik verilerin doldurulması kararı, silinmesi işleminde olduğu gibi hassas ve bilinçli bir şekilde değerlendirilmesi gereken bir karardır. Zira doldurma işlemi veride gürültü (noise) oluşturabilir ve verinin istatistiksel olarak güvenilirliğini zedeleyebilir. Analitik durumlar içinse yanlış bilgi çıkarımlarına sebebiyet verebilir. Bu nedenle en sağlıklı doldurma kararının alındığı durumlarda dahi bu yanlılık durumu mutlaka göz önünde bulundurulmalıdır
4.3.1 Sayısal Değişkenlerin Doldurulması

4.3.2 Kategorik Değişkenlerin Doldurulması
4.3.3 Kategorik Kırılım İle Doldurma İşlemi
Burada basitçe mean ve median değerler ile doldurma işlemi yapmış olsak da, eksik veri durumunu bu kadar basit bir şekilde ele almak her zaman doğru olmayacaktır. Bu tarz basit doldurma işlemleri hızlı bir çözüm olarak ele alınmalıdır. Daha analitik bir yaklaşım için veri içerisinde benzetimler uygulayarak doldurma işlemlerini buna göre gerçekleştirebiliriz.
4.3.4 Makine Öğrenmesi ile Değer Atama Teknikleri¶
Makine öğrenmesi yöntemleri kullanarak da eksik verileri doldurmak mümkündür. Makine Öğrenmesi modelleri bu bootcamp'in konusu olmadığı için detaylı bir anlatım gerçekleştirilmeyecektir.

Hangi yöntemler kullanılabilir?:

KNNImputer (K-Nearest Neighbor) Random Forest Classifier Google -> "How can I fill missing values by using Machine Learning techniques in Python?", "Python ile eksik verileri Makine Öğrenmesi teknikleri kullanarak nasıl doldurabilirim?"
## 5. Kategorik Değişken Analizi
## 6. Sürekli Değişken Analizi
## 7. Aykırı Değer Analizi (Outliers)
Aykırı değerlerin analizi de tıpkı eksik verilerde olduğu gibi hassasiyetle değerlendirilmelidir. Aykırı değerlerin varlığı veri setindeki dağılımları etkileyeceği için, aykırı değere sahip bir veri setiyle tahmin modeli oluşturduğumuzda modelimizin genellenebilirliğinin düşmesine sebep olacaktır.

Aykırı değerlerin değerlendirilmesi için sektörel bilgi, standart sapma yaklaşımı, Z-skoru, IQR yöntemi gibi yöntemler kullanılabilir. Biz burada IQR yöntemi ile basitçe bir düzeltme işlemi uygulayacağız.
## 8. Feature Engineering
## EDA
