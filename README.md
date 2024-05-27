# Docker_command
docker often command

# Docker Server 

`docker info`

`docker --help`

`docker -cm- --help`

`docker system df`　　

# Docker image

`docker images`

`docker Search`

`docker pull  _image_:latest`

`docker rmi _image_:latest`

`docker run -d --name _image_ --restart -p 80:80 -p 443:443`

`docker run -it ubuntu:latest bash(or /bin/bash)`

# Docker container

`docker ps`

`docker start/stop/restart/kill _containerID_`

`docker rm _containerID_` 

`docker rm -f _containerID_` 強制刪除

`docker top _containerID_`

`docker inspect _containerID`

`docker exec -it _containerID_ /bin/bash` 推薦，重新載入後，再離開container繼續運行

`docker attach _containerID_` 重新載入後，再離開container停止運行

# Docker import and export

export: `docker export _containerID > ___.tar` 備份/導出

import: `cat ___.tar | docker import -___/ubuntu:1.5` 還原/導入

※ Container 中資料存在本機

`docker cp _containerID_ 來源路徑 目的路徑`

# Docker dockerfile

```CMD
From                ---基礎image

Maintainer          ---維護人

WORKDIR             ---指定目錄

RUN/ADD/COPY....    ---image操作指令

CMD,ENTRYPOINT      ---container執行時指令
```
建立image: `docker build -t test2:1.2 .`

# 增加功能再基礎image中，並另存新image

`docker commit -m 'add_new_function' -a='author' _containerID_ ubuntu:2.1`







