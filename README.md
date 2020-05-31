# vimeo-download

Esse é para baixar urls que tenha o arquivo master.json. Para streams que tenha uma lista m3u8, usar o ffmpeg. 

Referência: https://stackoverflow.com/questions/47233304/how-to-download-m3u8-in-once-time

Escolher a lista m3u8 baseado na resolução preferida. 

```
ffmpeg -i "http://example.com/chunklist.m3u8" -codec copy file.mp4
```

## Pré-Requisito

* ffmpeg

```
brew install ffmpeg
```

## Modo de uso

```
python vimeo-download.py -u "<url master.json>" -o "<nome do arquivo>"
```
