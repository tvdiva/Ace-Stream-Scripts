# [Помойка](http://f27uk3gyl2gfu4z36eifv4ob73w6xgrcms4w4vdxzcsxsobgc766ityd.onion/trash/ttv-list/)
## pom
- Загружает весь архив или выборочные файлы.
- Меняет IP:Port Ace proxy на свой.
- Заменяет расширение потока с .mp4 на .ts.
- Убирает из названия канала идентификатор языка и раздела.
- Параметры не требуются. Необходимые файлы указываются в скрипте.
- Приводит плейлист к такому виду:
```
#EXTM3U
#EXTINF:-1,.sci-fi
http://192.168.1.2:8000/pid/ed6a12719fbc9c9b38c2ce69c065a84f3a9b42e6/stream.ts
#EXTINF:-1,Amedia 1
http://192.168.1.2:8000/pid/5b1f4a0fb8abc134de4692179b55e4008f0e5e82/stream.ts
```
## get-torrent-id 
- Получает content-id и имя торрента по ссылке на торрент файл.
- Позволяет задать произвольное имя раздачи для плейлиста.
- Из content-id и имени раздачи формирует поле mp3u файла с Ace-Stream ссылкой.

Например, для создания ссылки на раздачу [Дознание пилота Пиркса (1979) BDRip 1080p](http://rutor.info/torrent/926965/doznanie-pilota-pirksa-1979-bdrip-1080p-ot-megapeer-d-ger-transfer), необходимо выполнить:
```
get-torrent-id "http://d.rutor.info/download/926965" "Дознание пилота Пиркса [1979, BDRip, 1080p]"
```
В результате получим:
```
#EXTINF:-1,Дознание пилота Пиркса [1979, BDRip, 1080p]
http://192.168.1.2:8000/infohash/5e2f4dd981f06062bae9832b6e3bb196556ccc6f/0/stream.mp4
```
