# TSDebugger
用于调试RTMP、KMP、HTTP(S)-FLV、Websocket(s)-FLV流时间戳的小工具  

## Download
- https://cdn.nodemedia.cn/tsdebugger/0.1.4/tsdebugger_windows_amd64.zip
- https://cdn.nodemedia.cn/tsdebugger/0.1.4/tsdebugger_linux_amd64.tar.gz
- https://cdn.nodemedia.cn/tsdebugger/0.1.4/tsdebugger_linux_arm64.tar.gz
- https://cdn.nodemedia.cn/tsdebugger/0.1.4/tsdebugger_darwin_amd64.tar.gz
- https://cdn.nodemedia.cn/tsdebugger/0.1.4/tsdebugger_darwin_arm64.tar.gz

## changelog
v0.1.4
- 增加aac/opus 头的打印  

v0.1.3
- 增加avcc/hvcc 头的打印  
- 增加关键帧标识打印  
- 增加关键帧间隔时长统计  
- 增加音视频每秒帧率，码率统计

## Usage
```
tsdebugger rtmp://192.168.0.3/live/stream
```

```
tsdebugger kmp://192.168.0.3/live/stream
```

```
tsdebugger http://192.168.0.3:8000/live/stream.flv
```

```
tsdebugger ws://192.168.0.3:8000/live/stream.flv
```

```
2020/07/07 18:06:38 [I] onStatus level=status code=NetStream.Play.Start description=Started playing bbb.
2020/07/07 18:06:38 [D] rtmp type=metadata pts=0 dts=0 size=333
2020/07/07 18:06:38 [D] AAC sequence header
00000000  11 88 56 e5 00                                    |..V..|

2020/07/07 18:06:38 [D] AVC sequence header
00000000  01 64 00 1f ff e1 00 24  67 64 00 1f ac b2 01 e0  |.d.....$gd......|
00000010  22 fd c2 00 00 03 00 02  00 00 03 00 60 c0 c0 01  |"...........`...|
00000020  e8 48 00 3d 09 cd 46 00  f1 83 24 80 01 00 05 68  |.H.=..F...$....h|
00000030  eb cc b2 2c fd f8 f8 00                           |...,....|

2020/07/07 18:06:38 [D] rtmp ReadMessage type=metadata time=0 size=269
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=0 size=7
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=0 size=57
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9735863 size=34558
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9735868 size=180
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9735892 size=160
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9735896 size=1934
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9735915 size=186
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9735930 size=364
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9735938 size=188
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9735961 size=201
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9735963 size=2116
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9735985 size=186
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9735996 size=2673
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736008 size=174
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9736030 size=2279
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736031 size=187
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736054 size=237
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9736063 size=2430
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736077 size=187
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9736096 size=636
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736101 size=161
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736124 size=166
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9736130 size=2029
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736147 size=191
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9736163 size=2684
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736170 size=206
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736194 size=177
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9736196 size=2747
2020/07/07 18:06:38 [D] rtmp ReadMessage type=audio time=9736217 size=178
2020/07/07 18:06:38 [D] rtmp ReadMessage type=video time=9736230 size=2513


```
