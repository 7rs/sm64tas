<h1 align="center">SM64 TAS Archives</h1>
<p align="center">
    This is Archives for publication and storage TASing files by Cbrnex.
</p>

---

## Resources  

- SMIoF (Integration of Fragments (v1.3.5))
- SMEJ (Endress Journey)
- SMCC (Cursed Castles)
- SR4.9 (Star Revenge 4.9 - Adulterated Realty)

[Records](https://docs.google.com/spreadsheets/d/1T3Jvo-Eos7cOatJ-g1GnOt9uuALvwnHk0hUVMKZKOMI/edit?usp=sharing)


## Encoding  


- ### Merges the videos  

```bash
ffmpeg -safe 0 -f concat -i paths.txt -b "8M" -r "30" -s "1440x1080" -ab "384k" -sn -map 0:v -map 0:a output.avi
```

```bash paths.txt
file './yourrecords1.avi'
file './yourrecords2.avi'
```

Required [FFmpeg](https://ffmpeg.org/)  


- ### Just encodes the videos  

```bash
ffmpeg -safe 0 -b "8M" -r "30" -s "1440x1080" -ab "384k" -sn -map 0:v -map 0:a output.avi
```  


- ### Video Reference  

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

- [YouTube recommended upload encoding settings](https://support.google.com/youtube/answer/1722171)  

