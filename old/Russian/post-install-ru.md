<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Запуск Windows на Xiaomi Mi 9

## Необязательные действия после установки

### Список поддерживаемого софта
Это не полный список, просто все то, что протестировало комьюнити.
[Ссылка на таблицу](https://docs.google.com/spreadsheets/d/1XYuoySgYQE0HL573sA-0RGMX7I4lt5rWJuQ8Z8yRJNY/edit?usp=drivesdk)

You can also find a list of dedicated ARM software [at this link](https://armrepo.ver.lt/)

#### Готово!

### Переключение в режим USB host mode
> [!Warning]
> Отключите USB host mode, если у вас подключен юсб-хаб с питанием, тк. это может повредить ваше устройство. Если вы используете юсб-хаб без питания, включите USB host mode, иначе вы не сможете использовать никакие юсб-устройства.

Запустите [USB Host Control](https://github.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/releases/download/USBHost/USB.Host.Mode.Control.V4.0.vbs) чтобы включить/выключить USB host mode, подтвердите, что вы хотите включить или выключить USB host mode и подтвердите перезагрузку.

#### Готово!

### Скрываем диск D: (раздел связанный с модемом)
> [!NOTE]
> Это очень рекомендуется сделать, тк. этот диск должен оставться не тронутым, а приложения или игры могут пытаться записать свои данные на этот том.  

- Откройте командную строку и запустите  ```diskpart```
- Затем пропишите ```list volume``` чтобы увидеть все тома.
- Выберите диск с буквой D с помощью команды ```select volume $``` (вместо $ прописываем номер тома, который мы узнали ранее)
- Удалите букву с помощью команды ```remove letter d```
- Закрываем diskpart с помощью команды ```exit```

#### Готово!
