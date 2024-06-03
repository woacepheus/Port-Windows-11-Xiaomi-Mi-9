<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Çalıştıran bir Mi 9">

# Xiaomi Mi 9'da Windows Çalıştırma

## Android ile Windows arasında kolayca geçiş
> [!ÖNEMLİ]
> Bu rehber ROOT izinleri gerektirir

### Gerekenler
- [Magisk](https://github.com/topjohnwu/Magisk/releases/latest)

- [UEFI imajı](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.2/MuCepheusSecureBoot.img)

- [WOA Yardımcı Uygulaması](https://github.com/Marius586/WoA-Helper-update/releases/tag/WOA)

- [StA Kurulumu](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/Dualboot/StA_Installer_cepheus.exe)

## Çift Sistem Uygulamalarının Kurulumu

### Kurulum - Android
> [!NOT]
> Eğer Windows klasörüne dosya atamıyorsanız Windows'u yeniden başlatmak yerine kapattığınızdandır. Düzeltmek için Windows'a geçin ve yeniden başlatın, telefon geri açılırken TWRP'ye girin ve Android'e geçmek için Önyükleyici yedeğini geri yükleyin.

- [WOA Yardımcı Uygulamasını](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/Dualboot/woahelper.apk) indirin ve kurun, açarken de root izinlerini verin.
- [UEFI imajını](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.2/MuCepheusDisableSecureBoot.img)indirin ve dahili depolamada `UEFI` klasörüne koyun , eğer bu klasör yoksa oluşturun.
- WOA Yardımcı Uygulamasına girin ve `Back up Android boot` butonuna bastıktan sonra `Windows` ve `Android`i seçin
- Sonra `Mount Windows` butonuna basın, Sonra [StA_Installer_cepheus.exe](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/Dualboot/StA_Installer_cepheus.exe) dosyasını dahili depolamada çıkan `Windows` klasörüne atın.
- WOA Yardımcı Uygulamasına dönün ve `Quickboot to Windows` butonuna basın.

### Kurulum - Windows
- `C:\StA_Installer_cepheus.exe` Konumuna gidip programı çalıştırın. Eğer çalışmıyorsa Antivirüs vs. kapatın çünkü büyük ihtimalle programı açtırtmayacaktır.

##### Android'e geçiş
  - Masaüstündeki kısayola tıklayın (İsterseniz Başlangıç Menüsüne ve ya Görev Çubuğuna sabitleyin)

##### Windows'a Geçiş
  - Programdan `Quickboot to Windows` butonuna basın
  
## Bitti!
