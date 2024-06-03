<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Windows на Xiaomi Mi 9

## Переустановка
### Переустановка Windows если что-то пошло не так

- Если текущая версия Windows не подходит или была испорчена, вероятно, Вам поможет переустановка Windows, благо это довольно простой процесс.
- Если Вы не восстанавливали таблицу разделов, то используйте этот гайд с текущей таблицей разделов.

### Требования

- Существующие разделы для Windows и загрузки (*если их нет, [используйте данную инструкцию](/guide/Russian/partition-ru.md)*)
- [Образ рекавери](../../../../releases/tag/1.0)
- [ADB и Fastboot](https://developer.android.com/studio/releases/platform-tools)



### Запустите модифицированное рекавери
> Если Xiaomi заменил ваше рекавери на miui рекавери, то прошейте через fastboot:
```cmd
fastboot flash recovery путь\к\recovery-cepheus.img reboot recovery
```

### Форматирование разделов

```cmd
adb shell format
```

### [Следующий шаг](/guide/Russian/install-ru.md#установка-windows)
