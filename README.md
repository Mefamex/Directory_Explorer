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
os.chdir("..") # kütüphanenin dizinine çıkıyoruz
import main
DirExVis= main.DirExVis

# os.chdir("Your full path of dir")
DirExVis() #bu kodu çalıştırdığınızda işlemlere başlıyacak
```
`DirExVis()` kodu ile ekranınıza tüm alt klasörler ve mevcut dosyaların içerikleri gelicektir.
### Detayları Ayarlama
```python
########################## PYTHON ######################
DİrExVis.tab_size = 4 # default :4 ,
DİrExVis.details_size = True # default :False , dosya boyutu görünsün mü? 
DİrExVis.details_date = True # default :False , son kayıt tarihi görünsün mü? 
DİrExVis.details_folderCount = True # default :False ,
#                                   klasörlerin alt item sayısı görünsün mü? 

```
## Örnek Kod ve Çıktı
```Python
########################## PYTHON ######################
>>> import main
>>> x = main.DirExVis
>>> x.details_size = True
>>> x.details_folderCount=True
>>> x()

########################## OUTPUT ######################
C:\Users\User\Desktop\Directory_Explorer(0)                0.0mb 1724596396.0260692
|    Scripts(0)---------------------------------------------0.0mb 2024-08-25 17:24:19
|    |    activate                                        0.002mb 2024-08-25 17:24:19
|    |    activate.bat------------------------------------0.001mb 2024-08-25 17:24:19
|    |    Activate.ps1                                    0.025mb 2024-08-25 17:24:19
|    |    deactivate.bat------------------------------------0.0mb 2024-08-25 17:24:19
|    |    pip.exe                                         0.103mb 2024-08-25 17:24:19
|    |    pip3.11.exe-------------------------------------0.103mb 2024-08-25 17:24:19
|    |    pip3.exe                                        0.103mb 2024-08-25 17:24:19
|    |    python.exe--------------------------------------0.258mb 2024-08-25 17:24:19
|    |    pythonw.exe                                     0.247mb 2024-08-25 17:24:19
|    __pycache__(0)-----------------------------------------0.0mb 2024-08-25 17:33:16
|    |    main.cpython-311.pyc                            0.014mb 2024-08-25 17:33:16
|    .gitignore-------------------------------------------0.003mb 2024-08-25 17:24:19
|    LICENSE                                              0.001mb 2024-08-25 17:24:19
|    main.py----------------------------------------------0.012mb 2024-08-25 17:24:19
|    README.md                                            0.002mb 2024-08-25 17:26:20
```

## Uyarılar
- Çok büyük dizinlerde performans düşüşü yaşanabilir.
- Dosya erişim haklarına dikkat edilmelidir. Yeterli izne sahip olmadığınız dosya veya dizinler üzerinde çalışırken sorunlar yaşayabilirsiniz.
