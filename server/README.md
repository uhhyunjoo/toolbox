# Linux Command

### GPU 관련
```
nvidia-smi
```

```
nvcc --version
```

```
gpustat -i
```

```
history
```

### 도커 관련
```
sudo usermod -aG docker [USER_ID]
```

```
docker ps -a
```

```
docker start [CONTAINER_ID]
```

```
docker exec -it [CONTAINER_ID] /bin/bash
```

```
docker stop [CONTAINER_ID]
```

```
docker restart [CONTAINER_ID]
```

- 이미지 삭제하고 싶은데, 컨테이너가 사용중이라 삭제가 안될 때
```
docker images
```
```
docker ps -a --filter ancestor=[IMAGE_ID]
```
```
docker stop [CONTAINER_ID]
```
```
docker rm -f [CONTAINER_ID]
```
```
docker rmi [IMAGE_ID]
```

### 내 도커 이미지 기준
```
# /bin/zsh 
make docker-base
make docker-run
```

### 디렉토리 관련
- list directory contents [long listing format] [all] [human readable size] [columns] [sort by file size]
```
ls  -lahcs
```

- chage directory
```
cd [PATH]
```

- change mode
```
chomd 777 [FILE]
```

- remove [recursive] [force]
```
rm -rf [FOLDER]
```

```
rm [FILE]
```

- make directory
```
mkdir [FOLDER]
```

- link [soft]
```
ln -s [LINK_FOLDER] ./
ln -s [LINK_FOLDER] [FOLDER_NAME]
```

- copy folder [recursive] [force]
```
cp -Rf [FROM_HERE] ./
```

- move folder [recursive] [force]
```
mv -Rf [FROM_HERE] ./
```

- rename file / folder
```
mv test.txt retest.txt
mv folderA folderB
```

- 현재 폴더에서 폴더 개수 세기
```
ls -l | grep ^d | wc -l
```
- 현재 폴더에서 파일 개수 세기
```
ls -l | grep ^- | wc -l
```
- 현재 폴더 아래에 있는 파일 개수 세기
```
find . -type f | wc -l
```

![image](https://user-images.githubusercontent.com/41139770/169214773-ff61ad7e-e287-48e6-9e45-1e37315359e9.png)


### scp 관련
- local to server
```
scp [옵션] [원본 경로 및 파일] [계정명]@[원격지IP주소]:[전송받을 위치] 
```
```
scp -r -P [PORT_NUM] [ORIGINAL_PATH] [USER_ID]@[SERVER_IP]:[PATH]
```

- server to local
```
scp [옵션] [계정명]@[원격지IP주소]:[원본 경로 및 파일] [전송받을 위치]
```
```
scp -r -P [PORT_NUM] [USER_ID]@[SERVER_IP]:[ORIGINAL_PATH] ./
```
- server to server
```
scp [옵션] [원본 경로 및 파일] [계정명]@[원격지IP주소]:[전송받을 위치]
```
```
scp -r -P [PORT_NUM] [FILE] [USER_ID]@[SERVER_IP]:[PATH]
```

### 다운로드 관련
- download file with url
```
wget --no-check-certificate [DOWNLOAD_FILE_URL]
```

### 압축 관련 (.tar)

- unzip .tar file [extract files from archive] [verbose] [read from or write to archive (default : current directory]
- [OPENBSD/tar](http://man.openbsd.org/tar)
```
tar xvf [FILE_NAME].tar
```
```
tar xvf [FILE_NAME].tar -C [PATH]
```

### 압축 관련 (.zip)

- unzip .zip file
```
find . -name "*.zip" -exec unzip {} \;
```
```
unzip \*.zip
```
```
unzip [FILE_NAME].zip -d [SAVE_DIRECTORY]
```

### 용량 관련
- disk usage
```
du
```

- ncurses disk usage
```
ncdu
```
- disk free (file system storage info)
```
df -h
```


### 프로세스 관련
- visaul monitoring
```
top
```

- 향상된 top
```
htop
```

- kill process
```
kill -9 [PROCESS_ID]
```

- process status (standard syntax) [writes information] [full listing format] 
```
ps -ef
```
- 특정 프로세스 확인 
```
ps -ef | grep [PROCESS]
```
- process status (BSD syntax)
```
ps aux
```
- 특정 프로세스 확인 
```
ps aux | grep [PROCESS]
```

|  | description |
| --- | --- |
| USER | proces user (BSD) |
| UID | process user ID (SYSTEM V) | 
| PID | Process ID |
| PPID | Parent Process ID |
| %CPU | CPU 사용 비율 (BSD) |
| %MEM | Memory 사용 비율 (BSD) |

- [MAN7/ps](https://man7.org/linux/man-pages/man1/ps.1.html)



### 참고
- [자주 사용하는 linux command](https://koos808.tistory.com/89)
- [리눅스 top 정리 및 설명](https://zzsza.github.io/development/2018/07/18/linux-top/)
