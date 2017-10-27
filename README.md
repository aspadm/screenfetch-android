# Screenfetch for Android

This program was created from scratch and do not use any part of original `screenfetch`. And sorry for my bad english...  

![example screen](https://github.com/aspadm/screenfetch-android/raw/master/example.jpg)

## Features

After run in console, program (or script?) print Android logo and some system info.  

Screenshots also can be taken using special key.  

System parameters:  
1. name and hosname  
2. os name + sdk version  
3. kernel  
4. uptime  
5. packages(apk) count  
6. busybox version (if installed)  
7. device name  
8. display resolution 
9. launcher name (need root)  
10. chipset  
11. CPU - name (cores) @freq  
12. RAM - used(without cache)/all  

## How to install/start

If your device rooted, I strongly recommend put `sfa` file into `/system/bin` and use `chmod 755` - it allow you to start program with simple `sfa` in your console emulator.  

But the way, you still can download `sfa` file and run it using `sh sfa` in folder.  

## Usage  
  
 `sfa <-hctsv>`  
  
where:  
 `h` - show help  
 `v` - show version  
 `c` - take screenshot (need root access)  
 `s` - show system info with simple no utf8 logo  
 `t` - as is prev, but without color (simple text)  
  
examples:  
        1. `sfa -tc` - show textual sysinfo and take 2 screenshot(console and homescreen) to your /sdcard  
        2. `sfa`     - just show sysinfo (with colored utf8 logo)  

## Known issues  

1. `Service display not found`/`wm not found`  
I don't know, how it may be, but... I use `wm` to detect screen resolution if `dumpsys` not work. `dumpsys` works with root in 99.97%

2. Incorrect message `busybox: not installed`  
I search `busybox` in `/system/bin` and `/system/xbin`. And use `ls` for it. Some devices not contain `ls`. I was shocked when saw it by myself...

3. `Launcher: can't detect` or just print package name  
Root access needed to detect launcher package. If detection complete, program try to link package name with readable name using `case` operator. I not found another way, so write me missing package name and launcher name and I add it to the new version.

# For носителей русского языка  

Программа написана с нуля и не содержит элементов оригинального `screenfetch`. Ну, кроме упоминания в названии.  

## Возможности  

После запуска в консоли, программа (или корректнее скрипт?) выводит логотип Андроид и выдаёт краткую информацию о системе.  

А используя специальный ключ, ещё и скииншоты делает, да.  

Выдаваемая информация:  
1. имя пользователя и хоста
2. имя операционки + версия sdk
3. ядро
4. время от запуска (uptime)
5. количество приложений (apk)
6. версия busybox (если установлен)
7. название устройства
8. разрешение экрана
9. название лаунчера (нужны рут права)
10. чипсет
11. CPU - имя (ядра) @частота
12. RAM - занято(без учёта кэша)/всего

## Как поставить/запустить

Если есть рут права, рекомендую поместить файл sfa в `/system/bin` и применить `chmod 755` к файлу. Тогда запуск возможен просто коммандой `sfa` в эмуляторе консоли.

Тем не менее, можно просто загрузить этот файл и, перейдя с помощью `cd` в каталог с ним, выполнить `sh sfa`, даже без рут прав.

## Использование
  
 `sfa <-hctsv>`  

где:  
 `h` - показать справку  
 `v` - вывести версию  
 `c` - дополнительно сделать скриншоты (нужен рут)  
 `s` - простое лого без использования utf8  
 `t` - то же, но без цвета (чистый текст)  

примеры:  
        1. `sfa -tc` - покажет информацию и сделает 2 скриншота(консоли и домашнего экрана) на /sdcard  
        2. `sfa`     - просто покажет информацию о системе (с цветным utf8 лого)  

## Известные баги

1. `service display not found`/`wm not found`  
Вот тут меня попёрло... Я использую `wm` для получения разрешения экрана, если `dumpsys` не сработал. С рутом он работает в 99.97% случаев.

2. Неверное сообщение, что `busybox: not installed`  
Я проверяю `/system/bin` и `/system/xbin` на наличие бинарника `busybox`. И использую для этого `ls`. Когда на одном устройстве `ls` не оказалось, я лежал на полу и плакал...

3. `launcher: can't detect` или выводит имя пакета лаунчера  
Для определения пакета лаунчера нужны рут права. Если имя пакета получено, то программа пытается сопоставить его с человекочитаемым именем используя `case` (по словарю). Я не нашёл другого способа, поэтому присылайте имя пакета/лаунчера, если их нет в скрипте.

From Russia with love :)
