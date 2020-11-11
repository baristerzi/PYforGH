# Grasshopper'da Python Kullanımı - Metametrik
## 01. Veri Tipleri ve Matematiksel İşlemler

https://www.youtube.com/watch?v=Fh9616vr5oU&list=PLuRrB0FqYDhCJrFeZKBtNKs3X2D51bTwB&ab_channel=Metametrik

Kurulum ve Temel Bilgiler bulunan bu bölümde listelenen bilgilere ulaşabilirsiniz.

  - Veri Tipleri(Str,int,float,boolean)
  - Değişken Tanımlamak ve Tür Dönüşümleri(int => float, int => str)
  - Temel Matematiksel İşlemler(-,+,*,/,%,//,**)
  - Metod kavramı ve String İfadelerde Temel Metodlar(.split, .replace)
  
  ### Datatype - Temel Veri Tipleri;
  
  Veri tipleri tüm kod yazın sürecimizde kullanacağım en temel birimlerdir;
  
    string = "Metametrik" => String yani metinsel bir ifadedir. ("str") kısaltması ile kullanılır.
    integer = 10          => integer, tam sayı bir ifadedir. ("int") kısaltması ile kullanılır.
    float = 3.45          => float, reel sayılar kümesini tanımlayan bir ifadedir. ("float") kısaltması ile kullanılır.
    boolean = True       => boolean, True/False doğru ya da yanlışı tanımlayan ifadedir. ("bool") kısaltması ile kullanılır.
    
  Veri tiplerini sisteme sorgulatmak için;
    
    "type()" komutu => bir değişkenin veya birimin türünü sorgulamamızı sağlar.
    
    Yukarıda belirttiğimiz (string,integer,float,boolean) değişkenleri type() komutu ile yazdırırsak eğer;
    print(type(string))   =>   <str> , sonucunu alırız. 
    print(type(float))    =>   <float> , sonucunu alırız.
        
   ### Değişken tanımlamak;
   
   Değişken tanımlamak verileri farklı kod parçaları içinde birlikte kullanabilmek adına önemli olan bir işlemdir;
      
      a = 10; a isimli bir kod parçasına 10 integer yani tam sayısal değeri olarak tanımlanmıştır.
      b = "Selam"; b isimli bir değişkene "Selam" string(metinsel) ifadesi tanımlanmıştır.
      c = 3.4; c isimli değişkene 3.4 float yani reel sayı, ondalıksal sayısal değer olarak tanımlanmıştır.
      
      print(a)   =>   10
      print(b)   =>   Selam
      print(c)   =>   3.4
      
      ;olarak yazdırılır.
      
   Değişkenler atama ile basit iki egzersiz yapalım;
      
      a = "Metametrik" 
      print("Hello "+a)    =>  Hello Metametrik (string bir ifade ile string ifade birleştirilmiştir.)
      
      //
      
      b= 10 
      c= 25
      #result = b + c
      #print(result)       =>  35 (yapacağımız işlemi de bir değişken olarak tanımlayıp, "result" değişkenini yazdırabiliriz.
      print(b+c)           =>  35 (integer ve integer türünde iki ifade toplanmıştır.)
      
   
   ### Veri Tipleri Dönüşümü ve Karşılaşılan Sorunlar;
   
   Veri tipleri dönüşümü ifadelerin sınıfsal değişimlerinde önemlidir. String bir ifade sayısal bir işleme sokulamaz.Bu sebeple; ifadeler arası dönüşümleri iyi bilmemiz gerekmektedir.
   
      a = "hello"     ==> string bir ifadedir.
      a1 = "5"       ==> string bir ifadedir.
      b = 10          ==> integer bir ifadedir.
      c = 3.4         ==> float bir ifadedir.
      d = True        ==> boolean bir ifadedir.
      
   int/str dönüşümleri;
      
      print(a+b) kod parçası hatalı olur ve "class" hatasıyla karşılaşırız.
      Bu durum a ifadesi string, b ifadesinin integer olmasıyla alakalıdır.
      
      eğer string/int dönüşümleri hakkında bir işlem yapıyorsak;
      print(a+str(b)) yazdırırsak ( str(b) ==> b değerinin string bir ifadeye dönüşümünü sağlandığı için)
      ==> hello10 
      cevabını alırız ve 10 sayısı metinsel bir ifade olarak sonuna eklenmiş olur.
      
      print(a+a1) yazdırırsak tırnak içinde bir ifade olduğu için, 10 sayısını metinsel bir ifadeye dönüştürmüş oluruz.
      ==>  hello5
      cevabını alırız.
      
      veya bir string ifadeyi matematiksel bir işleme sokalım;
      print(b+int(a1)) yazdırırsak eğer ( int(a1) ==> a1 değerinin integer bir değere dönüşümünü sağladığı için)
      ==> 15
      cevabını alırız.
    
   int/float dönüşümleri ve ayrımı;  
     
      b = 10          ==> integer bir ifadedir.
      c = 3.4         ==> float bir ifadedir.
      
      Basit olarak;
      print(int(c))   ==> 3    ,   float olan "3.4" sayısının ondalık kısmını atarak tam sayıya dönüştürür.
      print(float(b)) ==> 10.0 ,   int olan "10" sayısı ondalık kısım alarak 10.0 reel sayısal değere dönüşür.
      
      bir işlem içerisinde kullanırsak;
      
      print(b+c)      ==> 13.4 
      cevabını alırız. Çünkü, int + float bir hesaplamanın cevabı float cinsinden verilir.
      
      İşleme bir değişken tanımlayarak, bu işlemin cevabını "int" cinsinden yazdıralım;
      
      result = b+c     
      print(int(result))  ==> 13
      
      // veya
      
      result = b+int(c)
      print(result)       ==> 13 
      
   boolean/(int/float) dönüşümleri;
      
      True/False değerlerine sahip boolean türü unitler bilgisayar dilinde  True:1 / False:0 değeri olarak tanımlanmıştır.
      
      yani;
      
      print(bool(1))  ==> True
      print(bool(0))  ==> False,
      
      durumuna karşılık gelmektedir.
      
      print(float(True))  ==> 1.0
      print(int(False)) ==> 0
      
      tersine dönüşümünde de durumuna karşılık gelmektedir.  
                
   ### Basit Matematiksel İşlemler;
