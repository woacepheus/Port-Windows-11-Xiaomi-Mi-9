<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Çalıştıran bir Mi 9">

# Xiaomi Mi 9'da Windows Çalıştırma

## Sürücüleri Güncelleme

### Gerekenler
- Telefonunuzda hâlihazırda kurulmuş bir windows
- [Sürücüler](https://github.com/qaz6750/XiaoMi9-Drivers/releases)
- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

### Modifiyeli TWRP'ye geç
> Eğer Xiaomi'nin yazılımı kurtarma bölümünü değiştirdiyse modifiyeli TWRP'yi şu komutla geri yükleyebilirsin:
```cmd
fastboot flash recovery dosyaya\giden\yol\recovery-cepheus.img reboot recovery
```

#### Depolama moduna geçin
> Eğer yeniden çalıştırın derse çalıştırın
```cmd
adb shell msc
```

#### Windows Disk Yöneticisi ile başlayın
> Xiaomi Mi 9 telefonuz bilgisayarda gözüktüğü anda
```cmd
diskpart
```

### Windows Bölümüne `X` Harfini Atayın

#### Telefondaki Windows bölümünü seçin
> Bölüm sayısını bulmak için Diskpart'a `list volume` yazın, adı "WINCEPHEUS" olarak çıkacaktır

```diskpart
select volume <bölüm sayısı>
```

#### X Harfini Atayın
```diskpart
assign letter x
```

#### Diskpart'tan çıkın
```diskpart
exit
```

### Sürücülerin Kurulumu
> Sürücülerin olduğu sıkıştırılmış dosyayı ayıklayın 'OfflineUpdater.cmd' dosyasını çalıştırın. WINCEPHEUS Bölmesinin harfini (X olmalı) girin ve Enter'a basın.

### Windows'a girin
> TWRP'den "Windows" yedeğini geri yükleyin ve telefonu yeniden başlatın

## Finished!
