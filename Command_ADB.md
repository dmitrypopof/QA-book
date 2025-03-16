[Назад](README.md)

Команды ADB 

* [50 команд](https://xakep.ru/2016/05/12/android-adb/)
* [Широковещательные сообщения](https://github.com/ViliusKraujutis/AndroidBroadcastsMonitor/wiki/List-of-all-Broadcast-Intent-actions.-API-17)
$ am broadcast -a android.intent.action.AIRPLANE_MODE --ez state true - телефон в режим самолета


Установка сертификата на эмулятор:
1. adb root — получение root-доступа.
2. adb remount — перемонтирование файловой системы в режиме чтения/записи.
3. adb push your-cert.crt /sdcard/your-cert.crt — копирование сертификата на устройство.
4. adb shell 'cat /sdcard/your-cert.crt > /system/etc/security/cacerts/your-cert.crt' — перемещение сертификата в директорию доверенных корневых сертификатов.
5. adb shell 'chmod 644 /system/etc/security/cacerts/your-cert.crt' — установка прав доступа для сертификата.
6. adb reboot — перезагрузка устройства после установки сертификата.
7. Проверка установки сертификата:
adb shell ls /system/etc/security/cacerts/ — просмотр списка установленных сертификатов на устройстве.