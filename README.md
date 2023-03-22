**Подключение  adb через WiFi**
 - [ ] Устройство подключено к компьютеру по USB
 - [ ] `adb tcpip 5555`
 - [ ]  `adb connect 192.168.0.101:5555`

**Основные команды ADB:**  
`adb devices` - список подключенных устройств  
`adb connect 192.168.0.101:5555 ` - подключение к девайсу  
`adb tcpip 5555 ` - переход на режим работы по TCP/IP  
`adb usb` - возврат в режим работы по USB  
`adb disconnect 192.168.0.101:5555` - отключить устройство  
`adb -s 59757787` - указание с каким устройством работать, где -s - серийный номер устройства из списка `adb devices`  
`adb install app-debug.apk ` - установка apk на девайс  
`adb shell pm list packages` - список всех установленных приложений.  
`adb shell pm list packages > list.txt` - перенаправление списка всех установленных приложений в файл.  
`adb uninstall com.qrolic.reminderapp` - удаление приложения.  
`adb shell pm clear com.qrolic.reminderapp` — очистка cache и data приложения.  
`adb shell screencap -p /sdcard/screen.png` — сделать скриншот экрана и положить в папку  
`adb pull /sdcard/screen.png` — скачать скриншот на ПК.  
`adb push .\screen.png sdcard` — скопировать скриншот с ПК на телефон  
`adb shell am kill com.qrolic.reminderapp` — убить процесс с тестируемым приложением  
`adb logcat` — логи устройства в реальном времени  
`adb logcat >>log.log` — запись лога в файл.  
`adb logcat '*:W'` — выводит в лог только варнинги.  
`adb logcat -c` —очистка буфера.  
`adb logcat -d` —вывод лога на момент запуска команды.  
`adb reboot` — перезагрузка устройства  
`adb shell am start -a android.intent.action.VIEW 'https://google.com'` — запуск браузера.  
`adb shell dumpsys battery` — вывод информации о батарее.  
`adb shell dumpsys package com.qrolic.reminderapp | findstr permission` — вывод разрешений приложения (или через grep для linux)  