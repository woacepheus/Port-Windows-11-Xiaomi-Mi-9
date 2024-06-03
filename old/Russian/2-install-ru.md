<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Запуск Windows 11 на Xiaomi Mi 9 

## Установка Windows

### Необходимое
- [ARM-образ Windows](https://worproject.com/esd)

- [Драйвера](https://github.com/qaz6750/XiaoMi9-Drivers/releases)

- [Модифицированное тврп](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.4/recovery-cepheus.img) (Должно быть уже установленно)


### Перезагрузитесь в модифицированное рекавери
```cmd
fastboot flash recovery путь\к\recovery-cepheus.img reboot recovery
```

#### Выполните скрипт msc
```cmd
adb shell msc
```

#### Запустите diskpart
> [!Warning]
> Если вы удалите любой раздел с помощью diskpart сейчас или позже, Windows рано или поздно отправит команду памяти, которая будет неправильно распознана в следствие чего вся память будет стерта.

```cmd
diskpart
```

#### Выберите раздел для Windows
> Используйте `list volume` чтобы найти его, это будет **WINCEPHEUS**
```diskpart
select volume <number>
```

#### Выделение буквы X
```diskpart
assign letter x
```

#### Выберите ESP раздел
> Используйте `list volume` чтобы найти его, это будет **ESPCEPHEUS**
```diskpart
select volume <number>
```

#### Выделение буквы Y
```diskpart
assign letter y
```

#### Выйдите с  diskpart
```diskpart
exit
```

### Установка Windows 
> Замените `<path/to/install.esd>` на свой путь до install.esd

> Если вы используйте ISO файл, то файл образа находится в ISO. Монтируйте ISO через Windows Explorer, а затем скопируйте путь к нему

> Замените `index:6` на `index:1` если ваш образ не из ссылки которая предоставленна в инструкции

```cmd
dism /apply-image /ImageFile:path\to\install.esd /index:6 /ApplyDir:X:\
```

### Установка драйверов
> Распакуйте драйвера из архива и откройте 'OfflineUpdater.cmd' файл. Впишите букву диска **WINCEPHEUS** (Должно быть X) и нажмите enter.

#### Создание загрузчика для этого EFI
```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

#### Уберите букву диска
> Используйте diskpart чтобы убрать букву с  **ESPCEPHEUS**, если буква осталась

> Используйте `list volume` чтобы найти **ESPCEPHEUS**, выберите его с помощью `select volume <number>`, потом уберите букву Y с помощью `remove letter y`

### Reboot to Android
> To set up dualboot

### [Последний шаг: двойная загрузка](dualboot-ru.md)















