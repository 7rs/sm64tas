# SM64 TAS Archives  


## Romhacks list  
[smiof]: https://youtube.com/playlist?list=PLsprkNPmlpByj9nrsupld-aBIvvdo1wqQ  
| Name                   | Works | Videos                    |
| ---------------------- | -----:| ------------------------- |
| [SMIoF](iof/README.md) | 8/182 | [YouTube Playlist][smiof] |
|                        |       |                           |


## Resources  


## Encoding  

[YouTube recommended upload encoding settings](https://support.google.com/youtube/answer/1722171)  

| Resolution | Bitrate Bitlate (30fps) |
| ---------- | ----------------------- |
| 1080p      | 8 Mbps                  |
| 720p       | 5 Mbps                  |
| 480p       | 2.5 Mbps                |

| Type   | Audio Bitrate |
| ------ | ------------- |
| Mono   | 128 kbps      |
| Stereo | 384 kbps      |
| 5.1    | 512 kbps      |


```bash
ffmpeg -safe 0 -f concat -i paths.txt -b "8M" -r "30" -s "1440x1080" -ab "384k" -sn -map 0:v -map 0:a output.avi
```

```bash paths.txt
file './yourrecords.avi'
```
