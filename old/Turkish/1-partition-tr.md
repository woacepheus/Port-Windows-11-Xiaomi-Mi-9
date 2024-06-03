<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Çalıştıran Mi 9">

# Xiaomi Mi 9'da Windows Çalıştırma

## Cihazı Bölümlendirme

### Gerekenler
- Bir beyin (aşırı önemli)

- [Modifiyeli TWRP](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.4/recovery-cepheus.img)

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

### Notlar:
> [!Warning]
>
> Bütün bilgileriniz silinecek, şimdiden yedeklerinizi alın!
> 
> Göreceğiniz komutlar denenmiştir ve çalışıyor.
> 
>  Aynı komutu lütfen iki kez çalıştırmayın.
> 
> Eğer bir hata yaptığınızı düşünüyorsanız SAKIN TELEFONU KAPATMAYIN VE YA YENİDEN BAŞLATMAYIN, [Telegram grubuna](https://t.me/woacepheus) katılıp yardım isteyin.
>
> Sakın bütün komutları aynı anda yürütmeye kalkmayın!
>
> EĞER AŞAĞIDAKİ KOMUTLARI YAZARKEN BİR YANLIŞLIK YAPARSANIZ TELEFONU HURDA EDERSİNİZ!

### Modifiyeli Kurtarma imajını atma ve kurtarma menüsüne girme
```cmd
fastboot flash dosyaya\giden\yol\recovery-cepheus.img reboot recovery
```

#### Bölümlendirme komutu
> Sadece komutu bir daha girmenizi isterse ikinci kez girin

> Bu **isteğe bağlıdır** ama isterseniz **altdaki komutla bölümleri istediğiniz boyuta ayırabilirsiniz**

> Telefondaki bölümleri istedğiniz boyuta ayırmak için ```adb shell partition [WİNDOWS'A ATANACAK GB SAYISI]```

> Köşeli parentezleri koymadığınızdan ve sayının sonuna GB koymadığınızdan emin olun, sadece sayıyı yazın

> 12/256GB MODELDE (Mi 9 Explorer Edition) SAKIN DENEMEYİN

```cmd
adb shell partition
```

### Android'in hâla çalıştığından emin olun
Telefonu yeniden başlatın, eğer açılmazsa kurtarma menüsüne girip telefona format atın (Wipe => Format Data)


### [Sonraki Adım: Windows kurulumu](/guide/Turkish/2-install-tr.md)
