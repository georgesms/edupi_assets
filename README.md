# edupi_assets

Compressing photos
```bash
for i in *.webp; do convert $i -quality 20% compressed/compr-$i; done;
```


Compressing videos
```bash
ffmpeg -i input.mp4 -vf "setpts=PTS/1.25" -filter:a "atempo=1.25" -c:v libvpx -b:v 100k -c:a libvorbis output.webm
```
