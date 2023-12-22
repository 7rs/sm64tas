<h1 align="center">スーパーマリオ64 TAS記録アーカイブ</h1>
<p align="center">
    Cbrnexによるスーパーマリオ64のTASの記録の公開・保管用のアーカイブ
    <img src="https://github.com/7rs/sm64tas/assets/31788262/afe4e2d8-7ed1-417f-8594-dc005e5ed861" />
</p>

[English](README.md)  

## 参考  

  | 略称      | 名前                                  | バージョン |
  | --------- | ------------------------------------- | ---------- |
  | SMIoF     | Integration of Fragments              | 1.3.5      |
  | SMEJ      | Endress Journey                       | β2.2       |
  | SMCC      | Cursed Castles                        | 1.02       |
  | SMSNR     | Super Mario SezNative Reminisence     |            |
  | SR4.9     | Star Revenge 4.9: Adulterated Reality |            |
  | SM4       | Super Mario 4                         |            |
  | Phenomena | Phenomena                             | 1.3.3      |

  - [TAS記録](https://docs.google.com/spreadsheets/d/1T3Jvo-Eos7cOatJ-g1GnOt9uuALvwnHk0hUVMKZKOMI/edit?usp=sharing)  
  - [入力ログ](https://docs.google.com/spreadsheets/d/1DsQFF0ahGCgXQ7CUcN3fhOEijFspUEYiew4IxnwdPt0/edit?usp=sharing)  


## エンコード  

  - ### 複数の動画を一つの動画に統合する  

  ```bash
  ffmpeg -safe 0 -f concat -i paths.txt -b "8M" -r "30" -s "1440x1080" -ab "384k" -sn -map 0:v -map 0:a output.avi
  ```  
  
  ```bash paths.txt
  file './yourrecords1.avi'
  file './yourrecords2.avi'
  ```  
  
  [FFmpeg](https://ffmpeg.org/) が必要です  
  
  
  - ### 動画をエンコードのみする  
  
  ```bash
  ffmpeg -safe 0 -b "8M" -r "30" -s "1440x1080" -ab "384k" -sn -map 0:v -map 0:a output.mp4 -i ""
  ```  
  
  
  - ### 動画の出力について  
  
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
  
  - [YouTube にアップロードする動画におすすめのエンコード設定](https://support.google.com/youtube/answer/1722171)  
  