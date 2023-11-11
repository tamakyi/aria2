# aria2
 
## 自用aria2文件备份，基于1.36.0版本，在Windows x64下使用

### 注意事项：记得修改以下内容
#### aria2.conf
```base
dir=下载目录
input-file=下载会话文件</br>
save-session=下载会话文件</br>
dht-file-path=DHT 文件路径</br>
dht-file-path6=DHT IPv6 文件路径</br>
rpc-secret=RPC 密钥，默认为P3TERX</br>
bt-tracker=trackers列表，此文件中的trackers不一定是最新的，需要手动到https://cf.trackerslist.com/best_aria2.txt进行更新

```
___
#### hiderun.vbs
##### 主要用于Windows下自启，修改完成后放到`X:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup`下使用,X为系统盘。

```
CreateObject("WScript.Shell").Run "%aria2绝对路径%\aria2c.exe --conf-path=%aria2绝对路径%\aria2.conf",0
```
