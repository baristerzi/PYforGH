# Grasshopper'da Python Kullanımı - Metametrik
## 01. Kurulum ve Temel Bilgiler

https://www.youtube.com/watch?v=Fh9616vr5oU&list=PLuRrB0FqYDhCJrFeZKBtNKs3X2D51bTwB&ab_channel=Metametrik

Kurulum ve Temel Bilgiler bulunan bu bölümde listelenen bilgilere ulaşabilirsiniz.

  - Komut istemi kullanımı
  - Python kurulumu
  - Jupyter Notebook kurulumu
  - Grasshopper Python node temel kullanımı
  
  ### Komut İstemini Açmak ve Temel Kullanımı;
  
  -Başlat + "cmd"/"Komut istemi" 
  -(Windows simgesi+R) tuşlarına basılıp "cmd"/"Komut istemi" yazılarak açılır.
 
 Temel Komutlar;
 - "cd" => Dosyalar arası geçişlerde kullanılan komuttur. (cd desktop => masaüstünüze ulaşırsınız.)
 - "cd.." => Klasörlerde bir önce ki klasöre erişmek için kullanılır.
 - "cls" => Komut ekranını temizlemek için kullanılır.
 - "cd\" => C diskine dönmenizi sağlar.
 - "dir" => komutu ile metodlar yazılıp çalıştırılabilir.
    "mkdir" => Bir dosya oluşturur. (mkdir text.py) => py uzantılı bir python dosyası oluşturur.
    "rmdir" => Bir dosya siler. (rmdir text.py) => py uzantılı python dosyasını silersiniz.
   
  ### Python Versiyon Sorgulamak ve Kurulum;
   
 Komut istemine "py --version" yazılarak => Python programının bilgisayarınızdaki sürüm bilgilerine ulaşılır.
  
  Python Kurulum Dosyaları;  
 https://www.python.org/downloads/
 
 ### Jupyter Notebook Çalıştırmak ve Basit Kod Denemeleri;
 
 Komut istemine "py jupyter notebook" / "py -m notebook" yazılarak Jupyter web tarayıcınız üzerinden çalıştırılır.
 
  Basit Kod Denemeleri;
  
    String(Metinsel) bir ifadeyi yazdırmak=>
    Print("Hello World!") => Hello World!
    
    String(Metinsel) bir ifadeyi basit bir değişkene atayarak yazdırmak=>
    say = "Hello World!"
    print(say) => Hello World!
    
    Basit bir fonksiyon ile bir ifadeyi yazdırmak=>
    
    "def" => fonksiyon oluşturma kodu.
    "sayHello(name):" => fonksiyonAdi(değişkenİsmi): => ":"dan sonra fonksiyon tanımlanmış olur.
      "print("Hello"+degiskenİsmi)" => "print" koduyla fonksiyona yazı yazdırma görevi tanımlanır.
    fonksiyonAdi(değişkenİsmi) => değişkenİsmi kısmına fonksiyona yazılacak ifade tanımlanır.
    
    Örnek;
    
    def sayHello(name):
      print("Hello"+name)
     sayHello(name)
     
     sayHello(Baha) yazılırsa => Hello Baha 
   
   ### Grasshopper'da Python kurmak ve Python nodunu açmak;
   
   Grasshopper Python nodu kurulum dosyaları;
   https://www.food4rhino.com/app/ghpython
    
   Temel Bilgilere rhino'nun kendi sitesinden de ulaşabilirsiniz;
   https://developer.rhino3d.com/guides/rhinopython/your-first-python-script-in-grasshopper/;
    
   
   -Grasshopper ekranında çift tık yapılarak "ghpythonscript" veya sadece "python" yazarak modülü oluşturabilirsiniz.
   
   -Temel node kullanımları;
   Python nodunu oluşturduğunuzda x ve y olarak input, out ve a olarak da output oluşturulur.
   Dikkat etmeniz gereken nokta herhangi bir input'a veya output'a sağ tıklayarak unitinizin türünü tariflemeniz gerekir."TYPE HINT" e tıklayarak açılan formdan unitinizi belirleyebilirsiniz.(int,float, point3d vb.)
   Python modulü üzerine çift sol tık yaptığınızda ise kod editör ekranı açılacaktır ve kod yazmaya başlayabilirsiniz.
   
   
   ### Grasshopper'da Python node input ve outputlarını tanımlamak;
   
   Basit bir egzersiz ile bir girdiyi kod vasıtası ile dönüştürelim;
  
    1) Öncelikle; ghpythonscript veya math sekmesi içerisindeki script tag'ı altında bulunan ikona tıklayarak bir python modülü oluşturalım. 
    2) input ve output isimleri değişken isimlerini ifade eder ve bu değişkenler ile basit bir fonksiyon yazalım. 
    3) Basit bir fonskiyonel kod;
    
    def sayhello(name)
      return "Hello" + name
    
    output = sayhello(input)
    
    4) input ve outputa iki tane panel bağladığımız zaman, input ifadesi yazdırılır.
    
    def sayhello(name)
      return "Hello" + name
    
     output = sayhello(Metametrik) ==> (Hello Metametrik) yazdırılır.  
     
   İkinci bir egzersiz ile grasshopper'da girilen bir nokta bilgisini kod vasıtası ile çizgiye dönüştürelim dönüştürelim;
      
      1) Öncelikle; bir python modülü oluşturuyoruz ve devamında grasshopper içerisinden 2 tane point oluşturuyoruz(construct point). 
      2) Python modülünün inputlarının "x=>point1" , "y=>point2" isimlerini üzerlerine çift tık yaparak okunaklı olması için değiştirebiliriz. ve "a" outputunu silerek de tek çıktı olarak ayarlamılıyız.
      3) Değişken isimleri oluşturulduktan sonra "TYPE HINT" kısmında inputlarımızın türlerini "3dpoint" olarak değiştirmemiz gerekmekte ki fonksiyonumuzun girdileri çalışabilsin.
      4) Değişken isimlerimizi ve türlerini ayarladığımıza göre, iki tane oluşturduğumuz pointleri python modülü girdilerine bağlayabiliriz. Devamında çift tıklayarak girdiğimiz editör sayfamızdan kodlarımızı yazmaya başlayabiliriz;
     
      """
      import ghpythonlib.components as ghcomp
      
      output =  ghcomp.line(point1,point2)
      
      """
      ;bu kod zinciri ile bir line oluşturmuş oluyoruz.
      
      A1) import ile (ghpythonlib) kütüphanesinden (.components) modülünü çağırarak "as" (ghcomp) olarak kodumuza tanımlatıyoruz. => import ghpython.components as ghcomp
      
      A2) (ghcomp) olarak tanımladığımız modüle (.line) modulünü ekleyerek bir line tanımlamak istiyoruz ve .line(STARTPOINT,ENDPOINT) şeklinde başlangıç ve bitiş noktalarını tanımlamamız gerekmektedir ve bunu da bir çıkış verisine dönüştürmemiz gerektiği için "output" a eşlememiz gerekmektedir.
      => output = ghcomp.line(point1,point2)
  
      Sonuç: 2 ayrı nokta girdi olarak verilen bir python kodu ile bir line oluşturulmuş oldu.
    
    

      
      
      
      

      
    
    
    
    
    
     
      
     
    
    
    
 
 
 
 
 
 
 
