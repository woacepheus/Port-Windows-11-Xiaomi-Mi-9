<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Windows на Xiaomi Mi 9

## Удаление

### Зачем это нужно?

Если вы хотите удалить Windows, это используется вместо удаления разделов вручную, чтобы избежать человеческой ошибки + написание целого специального руководства по простому удалению.

Если вы хотите заблокировать загрузчик, вам понадобится стандартная таблица разделов.

### Требования

- [ADB и Fastboot](https://developer.android.com/studio/releases/platform-tools)
- [gpt_both0.bin](../../../../releases/tag/1.0)

### Восстановление GPT
> Замените ```<gpt_both0.bin>``` путём к файлу `gpt_both0.bin`.

```cmd
fastboot flash partition:0 <gpt_both0.bin>
```

### Очистите раздел `userdata` чтобы избежать цикличной перезагрузки и восстановить размер файловой системы
```cmd
fastboot -w
```
