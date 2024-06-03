<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Çalıştıran bir Mi 9">

# Xiaomi Mi 9'da Windows Çalıştırma

## Windows Kurulumu

### Gerekenler
- [Windows on ARM sistem dosyası](https://worproject.com/esd)

- [Sürücüler](https://github.com/qaz6750/XiaoMi9-Drivers/releases)

- [Modifiyeli TWRP](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.4/recovery-cepheus.img) (Zaten kurulu olması lazım)

### Modifiyeli TWRP'ye geçin
> Eğer önceki sayfadaki son adım kurtarma bölümünü sıfırladıysa aşağıdaki komutla yeniden yükleyin:
```cmd
fastboot flash dosyaya\giden\yol\recovery-cepheus.img reboot recovery
```

#### Depolama Komutunu çalıştırın
> Eğer yeniden çalıştırın derse çalıştırın
```cmd
adb shell msc
```
  
#### Windows Disk Yöneticisi ile başlayın
> [!Warning]
> Eğer Diskpart kullanarak telefonu bölümlendirmeye çalışırsanız Windows hatalı bir UFS komutu göndererek telefondaki HER BÖLMEYİ VE İÇİNDEKİLERİ SİLER! 
```cmd
diskpart
```

#### Telefondaki Windows bölümünü seçin
> Bölüm sayısını bulmak için Diskpart'a `list volume` yazın, adı **WINCEPHEUS** olarak çıkacaktır
```diskpart
select volume <bölüm sayısı>
```

#### X Harfini Atayın
```diskpart
assign letter x
```

#### Telefondaki ESP Bölümünü seçin
> Bölüm sayısını bulmak için Diskpart'a `list volume` yazın, adı **ESPCEPHEUS** olarak çıkacaktır
```diskpart
select volume <bölüm sayısı>
```

#### Y Harfini Atayın
```diskpart
assign letter y
```

#### Diskpart'tan çıkın
```diskpart
exit
```

### Windows'un kurulumu
> `dosyaya\giden\yol\install.esd`'u install.esd dosyasına giden yol ile değiştirin.

> ISO dosyası indirdiyseniz .esd dosyası ISO içinde sources klasöründe olmalı. ISO'ya Explorer'da (Dosya Gezgini) çift tıklayarak bağlayın ve .esd dosyasını oradan kopyalayın.

> Dosyanızı verdiğimiz linkten almadıysanız `index:6`'yı `index:1` olarak değiştirin.

```cmd
dism /apply-image /ImageFile:dosyaya\giden\yol\install.esd /index:6 /ApplyDir:X:\
```

### Sürücülerin Kurulumu
> Sürücülerin olduğu sıkıştırılmış dosyayı ayıklayın 'OfflineUpdater.cmd' dosyasını çalıştırın. **WINCEPHEUS** Bölmesinin harfini (X olmalı) girin ve Enter'a basın.

#### Windows EFI Önyükleyici dosyalarını oluşturun
```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

#### Harf atamasını kaldırın
> Diskpart ile **ESPCEPHEUS**'un harfini kaldırın, yoksa bilgisayarı yeniden başlatana kadar dosya gezgininde boş sürücü olarak gözükecektir.

> **ESPCEPHEUS**'un numarasını bulmak için `list volume` kullanın, `select volume <numara>` ile seçin, son olarak `remove letter y` ile kaldırın

### Reboot to Android
> To set up dualboot

## [Son Adım: Çift Sistem Kurulumu](dualboot-tr.md)












