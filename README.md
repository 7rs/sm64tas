<h1 align="center">SM64 TAS Archives</h1>
<p align="center">
    An Archive for publication and storage TASing files by Cbrnex.
    <img src="https://github.com/7rs/sm64tas/assets/31788262/afe4e2d8-7ed1-417f-8594-dc005e5ed861" />
</p>


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
  
  
  - ### Just encodes a video  
  
  ```bash
  ffmpeg -safe 0 -b "8M" -r "30" -s "1440x1080" -ab "384k" -sn -map 0:v -map 0:a output.mp4 -i ""
  ```  
  
  
  - ### Outputting Reference  
  
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
  