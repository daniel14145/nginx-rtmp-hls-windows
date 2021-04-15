# nginx-rtmp-hls-windows

### OBS Studio Configuration
File->Settings -> Stream:
```
Streaming Service: Custom streaming server
Server: rtmp://<Server ip>/live
Stream Key: <Stream key>
```

Example: rtmp://127.0.0.1/live/boo

### Streaming URL

http://&lt;Server ip&gt;/hls/&lt;Stream key&gt;.m3u8


Example: http://127.0.0.1/hls/boo.m3u8


### Installation

1. Download the file "nginxgraphyon.zip" to your computer.
2. Extract `nginxgraphyon.zip`.
3. Open the file `C:\Users\**[Your_Nick]**\Downloads\nginxgraphyon\conf\nginx.conf`.
4. Replace this setting `hls_path "C:/Users/**mohan**/Downloads/nginxgraphyon/www/hls/";` on `hls_path "C:/Users/**[Your_Nick]**/Downloads/nginxgraphyon/html/hls/";`.
5. Open the file `C:\Users\[Your_Nick]\Downloads\nginxgraphyon\html\index.html`.
6. Replace this setting `<source src="**http://localhost:8080/hls/boo.m3u8**" type="application/x-mpegURL" />` on `<source src="**http://127.0.0.1/hls/boo.m3u8**" type="application/x-mpegURL" />`.
7. Run `C:\Users\[Your_Nick]\Downloads\nginxgraphyon\nginx.exe` as Administrator. 
Observation on windows 10, if we do not run as administrator, the application does not start.
