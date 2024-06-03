<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Çalıştıran bir Mi 9">

# Xiaomi Mi 9'da Windows Çalıştırma

## Yeniden Kurulum

### Herhangi bir sıkıntı olursa Windows'u yeniden kurmak

- Eğer Windows sürümünü değiştirmek istiyorsanız, kurulumda hata aldıysanız ve ya sistemi çökerttiyseniz korkmayın çünkü yeniden kurmak o kadar da zor değil.
- Eğer Bölüm tablosunu değiştirmediyseniz bölümlendirmenize gerek kalmayacaktır.

### Gerekenler

- Windows ve Önyükleyici bölümleri (eğer bu bölümler yoksa [lütfen geri dön ve bu sefer düzgün, ciddi bir şekilde oku](/guide/English/1-partition-en.md)*)
- [Modifiyeli TWRP](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.0/recovery-cepheus.img) (Should already be installed)
- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

### Modifiyeli TWRP'ye geç
> Eğer Xiaomi'nin yazılımı kurtarma bölümünü değiştirdiyse modifiyeli TWRP'yi şu komutla geri yükleyebilirsin:
```cmd
fastboot flash recovery dosyaya\giden\yol\recovery-cepheus.img reboot recovery
```

### Format atma

```cmd
adb shell format
```

### [Sonraki Adım: Windows'u yeniden kurma](/guide/TurkishEnglish/2-install-tr.md)
