# Soyutlama-Abstraction-ozet-anlatim
Soyutlama (abstraction), bir nesnenin veya bir sürecin önemli özelliklerini vurgulayarak ayrıntıları gizlemeyi ve yalnızca gerekli olan bilgileri sunmayı ifade eder. C++ gibi bir programlama dilinde soyutlama, verileri ve işlevleri bir sınıfta veya arayüzde birleştirerek gerçek dünyadaki nesneleri veya kavramları modellemek için kullanılır.

Örneğin, bir araba sınıfını düşünelim. Bir araba, özellikle markası, modeli, hızı, yakıt seviyesi gibi özelliklere sahip olabilir ve ayrıca hareket etme, fren yapma, yakıt alımı gibi işlevlere de sahip olabilir. Ancak, bir araba nesnesini kullanacak olan kişinin, arabanın iç işleyişine veya karmaşık detaylarına hakim olması gerekmez.

Bu durumda, soyutlama devreye girer. Arabayı temsil etmek için bir sınıf oluşturabiliriz. Sınıfın içinde araba özelliklerini (marka, model, hız, yakıt seviyesi) ve işlevlerini (hareket etme, fren yapma) tanımlayabiliriz. Dışarıdan sınıfı kullanan bir kişi, yalnızca arabanın hareket etmesi için bir komut vermek veya hızını kontrol etmek gibi basit işlemler yapabilir. Detaylar, sınıfın içinde saklanır ve kullanıcıya sunulmayabilir.


ufak bir örnek: 
#include <iostream>
using namespace std;

    <pre style=”background-color: darkgrey; border: 2px dashed rgb(235, 243, 251); overflow: auto; padding: 5px; text-align: justify; width: 569.633px;”>public:
    Araba(string marka, string model) {
        this->marka = marka;
        this->model = model;
        hiz = 0;
        yakitSeviyesi = 100;
    }

    void HareketEt() {
        hiz = 50;
        yakitSeviyesi -= 10;
        cout << marka << " " << model << " hareket etti!" << endl;
    }

    void FrenYap() {
        hiz = 0;
        cout << marka << " " << model << " durdu!" << endl;
    }

    void YakitSeviyesiniGoster() {
        cout << "Yakıt seviyesi: " << yakitSeviyesi << endl;
    }
};

int main() {
    Araba myCar("BMW", "M5");
    myCar.HareketEt();
    myCar.FrenYap();
    myCar.YakitSeviyesiniGoster();

    return 0;
}</pre>
class Araba {
private:
    string marka;
    string model;
    int hiz;
    int yakitSeviyesi;


  
  Bu örnekte, "Araba" sınıfı marka, model, hız ve yakıt seviyesi gibi özellikleri içerir. "HareketEt" işlevi arabanın hızını artırır ve yakıt seviyesini azaltır. "FrenYap" işlevi arabanın hızını sıfıra ayarlar. "YakitSeviyesiniGoster" işlevi ise arabın yakıt seviyesini ekrana yazdırır.

"main" fonksiyonunda bir "Araba" nesnesi oluşturulur ve "HareketEt", "FrenYap" ve "YakitSeviyesiniGoster" işlevleri çağrılır. Kullanıcı, arabayı hareket ettirmek, durdurmak ve yakıt seviyesini kontrol etmek için sadece bu işlevleri kullanabilir. Arabanın iç detaylarına veya karmaşık işleyişine dair bilgiler gizlenmiştir.

Bu şekilde soyutlama, bir nesnenin temel işlevlerine odaklanmamızı ve karmaşıklığı azaltarak programları daha anlaşılır ve sürdürülebilir hale getirmemizi sağlar.
