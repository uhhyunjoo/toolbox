# Windows

> 윈도우 초기화 후에 뭐했는지 적어두는 문서

- 초기화할 때 네트워크 연결 x, 마소 계정 연결 x
- 사용자 폴더 이름 한글로 되면 초기화 다시 해야됨 ㅠㅠ
- `Windows` + `v` 켜놓기

## Install
- Chrome, Discord, Slack, VSCode, KakaoTalk

## 참고 문서
- [windows/wsl](https://docs.microsoft.com/ko-kr/windows/wsl/)
- [how-to-install-wsl2-and-use-linux-on-windows-10](https://www.lainyzine.com/ko/article/how-to-install-wsl2-and-use-linux-on-windows-10/)
 ```
 # Powershell 관리자 권한으로 실행
 wsl --install
 
 # DISM으로 WSL 관련 기능 활성화
 dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
 dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
 
 # WSL 설치
https://docs.microsoft.com/ko-kr/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package

 # WSL 2 를 default 로 설정
 wsl --set-default-version 2
 
 # Microsoft store 에서 ubuntu 다운로드 (현재 20.04 가 기본인듯)
 
```

```
Please create a default UNIX user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username: uhhyunjoo
New password:
Retype new password:
passwd: password updated successfully
Installation successful!
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

Welcome to Ubuntu 20.04 LTS (GNU/Linux 5.10.16.3-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Mon May 30 17:59:00 KST 2022

  System load:  0.0                Processes:             8
  Usage of /:   0.4% of 250.98GB   Users logged in:       0
  Memory usage: 1%                 IPv4 address for eth0: 172.26.155.182
  Swap usage:   0%

0 updates can be installed immediately.
0 of these updates are security updates.


The list of available updates is more than a week old.
To check for new updates run: sudo apt update


This message is shown once once a day. To disable it please create the
/home/uhhyunjoo/.hushlogin file.
uhhyunjoo@LAPTOP-E0O29DK4:~$
```

```
# ubuntu 상태 확인
PS C:\Users\uhhyunjoo> wsl -l -v
  NAME      STATE           VERSION
* Ubuntu    Stopped         2

# ubuntu 버전확인
PS C:\Users\uhhyunjoo> wsl cat /etc/lsb-release
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=20.04
DISTRIB_CODENAME=focal
DISTRIB_DESCRIPTION="Ubuntu 20.04 LTS"

# bash 실행
PS C:\Users\uhhyunjoo> wsl bash
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

uhhyunjoo@LAPTOP-E0O29DK4:/mnt/c/Users/uhhyunjoo$
```

- [a-complete-guide-to-how-to-install-docker-desktop-on-windows-10/](https://www.lainyzine.com/ko/article/a-complete-guide-to-how-to-install-docker-desktop-on-windows-10/)
