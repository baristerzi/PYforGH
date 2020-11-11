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
   
 -Komut istemine "py --version" yazılarak => Python programının bilgisayarınızdaki sürüm bilgilerine ulaşılır.
  
  Python Kurulum Dosyaları;  
 -https://www.python.org/downloads/
 
 ### Jupyter Notebook Çalıştırmak ve Basit Kod Denemeleri;
 
 -Komut istemine "py jupyter notebook" / "py -m notebook" yazılarak Jupyter web tarayıcınız üzerinden çalıştırılır.
 
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
      
     
    
    
    
 
 
 
 
 
 
 
