# lalmax
lalmax是以lal为内核的卍解

# 编译
./build.sh

# 运行
./run.sh

# 架构

![图片](image/init.png)

# 支持的协议
## 推流
(1) RTSP 

(2) SRT

(3) RTMP

(4) RTC(WHIP)

具体的推流url(除了SRT/WHIP)地址见https://pengrl.com/lal/#/streamurllist

## 拉流
(1) RTSP

(2) SRT

(3) RTMP

(4) HLS(S)

(5) HTTP(S)-FLV

(6) HTTP(S)-TS

(7) RTC(WHEP)


具体的拉流url(除了SRT/WHEP)地址见https://pengrl.com/lal/#/streamurllist 

## SRT
（1）SRT推拉流依赖libsrt库,run.sh中有编译libsrt，如果run.sh无法编译libsrt，需要自己另行编译libsrt

（2）暂时不支持SRT加密

（3）支持H264/H265/AAC

（4）可以对接OBS/VLC

推流url
srt://127.0.0.1:6001?streamid=#!::r=test110,m=publish

拉流url
srt://127.0.0.1:6001?streamid=#!::r=test110,m=request

## WebRTC
（1）支持WHIP推流和WHEP拉流,暂时只支持POST信令

（2）支持H264/G711A/G711U,后续支持opus音频

（3）可以对接vue-wish

WHIP推流url
http://127.0.0.1:1290/whip?streamid=test110

WHEP拉流url
http://127.0.0.1:1290/whep?streamid=test110



