<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Çalıştıran bir Mi 9">

# Xiaomi Mi 9'da Windows Çalıştırma

## Kaldırma

### Neden kaldırmak için ayrı bir sayfa var?

Eğer Windows'u kaldıracaksanız bölüm tablosunu değiştirirken hataları minimuma indirmek ve sadece kaldırmaya özel başka bir rehber oluşturmamak için.

Eğer Önyükleyiciyi kilitlemek istiyorsanız bölüm tablosunun fabrika çıkışında olduğu gibi olması lazım.

### Gerekenler

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)
- [Modifiyeli TWRP](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.0/recovery-cepheus.img) (Should already be installed)

### Modifiyeli TWRP'ye geç
> Eğer Xiaomi'nin yazılımı kurtarma bölümünü değiştirdiyse modifiyeli TWRP'yi şu komutla geri yükleyebilirsin:
```cmd
fastboot flash recovery dosyaya\giden\yol\recovery-cepheus.img reboot recovery
```

### Bölümleri eski haline getirme
> Modifiyeli TWRP'ye girdikten sonra:
```cmd
adb shell restore
```

## Bitti!
