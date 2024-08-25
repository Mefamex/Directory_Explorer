# Dizin Yapısı Görselleştirme Aracı

Bu Python uygulaması, belirtilen bir dizin yolundaki tüm dosya ve dizinleri detaylı bir şekilde analiz ederek, dosya boyutları, oluşturulma tarihleri, dizin hiyerarşisi gibi bilgileri görsel ve metinsel olarak sunar. Sistem yöneticileri, geliştiriciler ve veri bilimcileri için disk kullanımını optimize etmek, dosya yönetimini kolaylaştırmak ve veri analizi yapmak için ideal bir araçtır.

## Özellikler

- **Rekürsif Dizin Gezimi:** Belirtilen dizin ve tüm alt dizinlerini inceler.
- **Detaylı Bilgi Toplama:** Dosya boyutu, oluşturulma tarihi, dizin derinliği gibi bilgileri hesaplar.
- **Formatlı Çıkış:** Tablo şeklinde okunaklı bir terminal çıktısı sunar.
- **Metin Dosyasına Kaydetme:** Sonuçları otomatik olarak bir metin dosyasına kaydeder.
- **Özelleştirilebilir:** Çıkış formatı, analiz derinliği gibi ayarlar yapılabilir.

## Kurulum

Bu uygulamayı kullanabilmek için Python 3.x sürümünün yüklü olması gerekmektedir. Gerekli Python modülleri, Python'un standart kütüphanesinde bulunduğundan, herhangi bir ek modül yüklemesine gerek yoktur.
```bash 
git clone https://github.com/Mefamex/Directory_Explorer.git
```


## Kullanım

Komut panelinden `Python`'u aktifleştirmek ve istediğimiz klasöre gitmek için:   

```bash
cd Directory_Explorer
cd Scripts
activate.bat
python.exe
```
```python
########################## PYTHON ######################
import os
os.chdir("..") # main dizinine çıkmak için
from main.py import DİrExVis
os.chdir("..") # !!! Your full path of dir

# ------- tips -------
# os.chdir içine .. yazarak üst dizinlere ulaşabilirsiniz
# os.getcwd() yazarak mevcut konumunuzu görebilirsiniz

DirExVis() #bu kodu çalıştırdığınızda işlemlere başlıyacak
```
`DirExVis()` kodu ile ekranınıza tüm alt klasörler ve mevcut dosyaların içerikleri gelicektir.
### Detayları Ayarlama
```python
########################## PYTHON ######################
from main.py import DİrExVis
DİrExVis.tab_size = 4 # default :4 ,
DİrExVis.details_size = True # default :False , dosya boyutu görünsün mü? 
DİrExVis.details_date = True # default :False , son kayıt tarihi görünsün mü? 
DİrExVis.details_folderCount = True # default :False ,
#                                   klasörlerin alt item sayısı görünsün mü? 

```


## Uyarılar
- Çok büyük dizinlerde performans düşüşü yaşanabilir.
- Dosya erişim haklarına dikkat edilmelidir. Yeterli izne sahip olmadığınız dosya veya dizinler üzerinde çalışırken sorunlar yaşayabilirsiniz.
