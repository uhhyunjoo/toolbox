# Linux Command

### 서버 관련
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
```

- copy folder [recursive] [force]
```
cp -Rf [FROM_HERE] ./
```

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

### 다운로드 관련
- download file with url
```
wget --no-check-certificate [DOWNLOAD_FILE_URL]
```

- unzip .tar file [extract files from archive] [verbose] [read from or write to archive (default : current directory]
- [OPENBSD/tar](http://man.openbsd.org/tar)
```
tar xvf [FILE_NAME].tar
```
```
tar xvf [FILE_NAME].tar -C [PATH]
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
