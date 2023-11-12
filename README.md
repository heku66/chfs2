# chfs
[CuteHttpFileServer/chfs](http://iscute.cn/chfs) 是一个免费的、HTTP协议的文件共享服务器，使用浏览器可以快速访问。

## 用法 / Usage
```
docker run -d -p 8008:80 -v <data_path>:/home solyhe84/chfs
```
## docker-compose用法
```
version: "3"

services:
  chfs:
    image: solyhe84/chfs
    container_name: chfs
    restart: always
    environment:
      - TZ=Asia/Shanghai
    volumes:
      - ./data:/home
      - ./chfs.ini:/app/chfs.ini
    ports:
      - 8008:80
```
规则详见 [chfs 网页](http://iscute.cn/chfs)

