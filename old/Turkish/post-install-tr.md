<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Çalıştıran bir Mi 9">

# Xiaomi Mi 9'da Windows Çalıştırma

## İsteğe bağlı kurulum sonrası ayarlar

### Desteklenen Uygulama/Oyunların lsitesi
Büyük bir liste değil, milletin test ettiği oyunlar ve programların bir listesi

[Buradan Bakabilirsiniz](https://docs.google.com/spreadsheets/d/1XYuoySgYQE0HL573sA-0RGMX7I4lt5rWJuQ8Z8yRJNY/edit?usp=drivesdk)

ARM'a özel versiyonları olan programlaru [burada bulablirsiniz](https://armrepo.ver.lt/)


### USB Ana Makine (Host) modunu açıp kapatma
> [!Uyarı]
> Ekstradan bir güç kaynağı olan USB Hub'lar için USB Ana makine modunu kapatın yoksa telefona ciddi hasar verebilirsiniz. Eğer dışarıdan bir güç kaynağı (pil, adaptör vs.) olmayan bir hub kullanıyorsanız host modunu açmadan hub çalışmaz.

[USB Host modu Kontrol](https://github.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/releases/download/USBHost/USB.Host.Mode.Control.V4.0.vbs) uygulamasıyla açıp kapatabilirsiniz, Açma/Kapama seçeneğini onaylayın ve yeniden başlatın.


### D: Sürücüsünü gizleme (Modem bölümü)
> [!NOT]
> Bu adımın önerilme sebebi bazı programlar bunu sürücünün üstüne yazmaya çalışabilir fakat modem bölmesinin hiç bir şekilde değiştirilmemesi gerekir.

- Komut satırını açıp ```diskpart``` yazın
- Sonra ```list volume``` yazıp bütün bölümleri kontrol edin
- D harfi atanmış olan bölümü ```select volume $``` ile seçin, $ yerine o bölümün numarasını koymayı unutmayın
- Harf atamasını ```remove letter d``` ile kaldırın
- Diskpart'dan artık ```exit``` yazarak çıkabilirsiniz

#### Bitti!








