# Pré-Requisito

* ffmpeg

```
brew install ffmpeg
```

# Para listas m3u8
Referência: https://stackoverflow.com/questions/47233304/how-to-download-m3u8-in-once-time

Para baixar stream que tenha uma lista m3u8. Apertar F12 e pesqusiar na aba rede pelo termo playlist.m3u8, e então escolher a lista m3u8 baseado na resolução preferida.

```
#EXTM3U
#EXT-X-VERSION:3
#EXT-X-STREAM-INF:BANDWIDTH=165888,RESOLUTION=426x240
chunklist_b165888.m3u8
#EXT-X-STREAM-INF:BANDWIDTH=217088,RESOLUTION=640x360
chunklist_b217088.m3u8
#EXT-X-STREAM-INF:BANDWIDTH=272384,RESOLUTION=854x480
chunklist_b272384.m3u8
#EXT-X-STREAM-INF:BANDWIDTH=390144,RESOLUTION=1280x720
chunklist_b390144.m3u8
#EXT-X-STREAM-INF:BANDWIDTH=652288,RESOLUTION=1920x1080
chunklist_b652288.m3u8
```

```
ffmpeg -i "http://example.com/chunklist_b652288.m3u8" -codec copy file.mp4
```


## Para arquivo master.json

Apertar F12 e pesqusiar na aba rede pelo termo master.json, copiar a url e aplicar o comando abaixo. Dentro de vimeo-download.py pode-se escolher a resolução de download. 

```
python vimeo-download.py -u "<url master.json>" -o "<nome do arquivo>"
```
