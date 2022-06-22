# Docker


```
docker version
```
```
Client:
 Cloud integration: v1.0.24
 Version:           20.10.14
 API version:       1.41
 Go version:        go1.16.15
 Git commit:        a224086
 Built:             Thu Mar 24 01:53:11 2022
 OS/Arch:           windows/amd64
 Context:           default
 Experimental:      true

Server: Docker Desktop 4.8.2 (79419)
 Engine:
  Version:          20.10.14
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.16.15
  Git commit:       87a90dc
  Built:            Thu Mar 24 01:46:14 2022
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.5.11
  GitCommit:        3df54a852345ae127d1fa3092b95168e4a88e2f8
 runc:
  Version:          1.0.3
  GitCommit:        v1.0.3-0-gf46b6ba
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

## How to use SER_IMGAE
```
cd docker
```
```
make docker-base
```
```
make docker-run TBP=8883 JNBP=8884
```

```
This is the Z Shell configuration function for new users,
zsh-newuser-install.
You are seeing this message because you have no zsh startup files
(the files .zshenv, .zprofile, .zshrc, .zlogin in the directory
~).  This function can help you with a few settings that should
make your use of the shell easier.

You can:

(q)  Quit and do nothing.  The function will be run again next time.

(0)  Exit, creating the file ~/.zshrc containing just a comment.
     That will prevent this function being run again.

(1)  Continue to the main menu.

(2)  Populate your ~/.zshrc with the configuration recommended
     by the system administrator and exit (you will need to edit
     the file by hand, if so desired).

--- Type one of the keys in parentheses --- 
```
```
2 # recommend setting
```

<img src='https://user-images.githubusercontent.com/41139770/174969621-06b8f83c-c420-4973-aace-7aa692f663b5.png' width=600 alt='shell output'>

```
conda env list
> # conda environments:
> #
> base                  *  /usr/local
> torch                    /usr/local/envs/torch
```
```
conda activate torch

> CommandNotFoundError: Your shell has not been properly configured to use 'conda activate'.
> To initialize your shell, run
> 
>     $ conda init <SHELL_NAME>
> 
> Currently supported shells are:
>   - bash
>   - fish
>   - tcsh
>   - xonsh
>   - zsh
>   - powershell
> 
> See 'conda init --help' for more information and options.
> 
> IMPORTANT: You may need to close and restart your shell after running 'conda init'.
```
```
conda init zsh

> no change     /usr/local/condabin/conda
> no change     /usr/local/bin/conda
> no change     /usr/local/bin/conda-env
> no change     /usr/local/bin/activate
> no change     /usr/local/bin/deactivate
> no change     /usr/local/etc/profile.d/conda.sh
> no change     /usr/local/etc/fish/conf.d/conda.fish
> no change     /usr/local/shell/condabin/Conda.psm1
> no change     /usr/local/shell/condabin/conda-hook.ps1
> no change     /usr/local/lib/python3.9/site-packages/xontrib/conda.xsh
> no change     /usr/local/etc/profile.d/conda.csh
> modified      /home/hjlee/.zshrc
> 
> ==> For changes to take effect, close and re-open your current shell. <==
```

- Reopen the shell

```
docker ps
```
```
docker exec -it hjlee_ser_container /bin/zsh
```
