<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Запуск Windows на Xiaomi Mi 9

## Двойная загрузка Android и Windows
> [!Important]
> Ваше устройство должно быть с рут правами чтобы использовать этот гайд.

### Требования
- [Magisk](https://github.com/topjohnwu/Magisk/releases/latest)

- [UEFI](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.2/MuCepheusSecureBoot.img)

- [WOA Helper app](https://github.com/Marius586/WoA-Helper-update/releases/tag/WOA)

- [StA Installer](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/Dualboot/StA_Installer_cepheus.exe)

#### Настройка - Android
> [!NOTE]
>
> Чтобы смонтировать Windows во время загрузки Android, вам необходимо правильно «выключить» Windows. Для этого перезагрузите Windows, а затем загрузитесь в TWRP, когда экран станет черным. Отсюда вы можете вернуться на Android, используя резервную копию, сделанную ранее.

- Скачайте и установите [WOA Helper](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/Dualboot/woahelper.apk)
- Скачайте [образ UEFI](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.2/MuCepheusDisableSecureBoot.img) и перенесите в папку с названием `UEFI` в внутренней памяти, если папки нету создайте её.
- Выберите «Backup to Android», а затем закройте всплывающее окно. Выберите обе `Windows` и `Android` опции.
- Сделайте то же самое, но выберете «Backup to Windows» 
- Нажмите кнопку «Mount Windows», после чего скачайте [StA_Installer_cepheus.exe](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/Dualboot/StA_Installer_cepheus.exe) и перенесите в новую папку `Windows` в вашей внутренней памяти.
- Вернитесь в приложение и нажмите «Quickboot to windows»

### Настройка - Windows
- Перейдите к `C:\StA_Installer_cepheus.exe` и запустите его. Если это не сработает, убедитесь, что все антивирусные программы отключены, поскольку они, вероятно, не позволят приложению запуститься.


#### Загрузка в Android
- Запустите новый ярлык на рабочем столе (вы также можете закрепить его в меню «Пуск» или на панели задач для удобства доступа).

#### Загрузка в Windows 
- Нажмите `Quickboot to Windows` внутри приложения или воспользуйтесь вновь созданным переключателем на панели быстрых настроек.

## Готово!
