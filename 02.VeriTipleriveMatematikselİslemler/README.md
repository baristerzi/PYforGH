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
      #result = a + c
      #print(result)       =>  35 (yapacağımız işlemi de bir değişken olarak tanımlayıp, "result" değişkenini yazdırabiliriz.
      print(a+b)           =>  35 (integer ve integer türünde iki ifade toplanmıştır.)
      
   
   ### Veri Tipleri Dönüşümü ve Karşılaşılan Sorunlar;
   
   
   ### Basit Matematiksel İşlemler;
