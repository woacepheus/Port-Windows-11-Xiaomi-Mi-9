<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Windows на Xiaomi Mi 9

## Обновление драйверов

### Требования

- Windows на вашем Xiaomi Mi 9
- [Recovery](../../../../releases/tag/1.0)
- [Драйверы](https://github.com/qaz6750/XiaoMi9-Drivers/releases)

### Запустите модифицированное рекавери
> Если Xiaomi заменил ваше рекавери на miui рекавери, то прошейте через fastboot:
```cmd
fastboot flash recovery путь\к\recovery-cepheus.img reboot recovery
```

#### Запустите режим mass storage
```cmd
adb shell msc
```

### Привязка букв к разделам

#### Запустите Менеджер дисков Windows

> Как только планшет определился как диск

```cmd
diskpart
```


### Привязка буквы  `X` к разделу Windows

#### Выберите Windows раздел планшета
> Используйте команду `list volume` чтобы найти разделы "WINNABU"

```diskpart
select volume <number>
```

#### Привяжите букву X
```diskpart
assign letter=x
```

#### Закройте diskpart
```diskpart
exit
```


### Установка драйверов
> Распакуйте драйвера из архива и откройте 'OfflineUpdater.cmd' файл. Впишите букву диска WINCEPHEUS (Должно быть X) и нажмите enter. 

### Перезагрузитесь в Windows
> Восстановите резерную копию boot.img "Windows" в TWRP и перезагрузите телефон.

## Готово!
