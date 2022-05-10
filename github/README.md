# Github
- Clone
```
git clone [REPO_URL]
```
```
git clone https://github.com/alro923/toolbox.git
```

- Add
```
git add [FOLDER]
```

- Commit
```
git commit -m '[COMMIT_MESSAGE]'
```

- Config
```
git config --global user.email "hjlee@rcv.sejong.ac.kr"
git config --global user.name "hjlee"
```

## private repo
```
ssh-keygen -t rsa -C "[EMAIL_ADDERESS]"
```
```
cd /home/hjlee/.ssh
```
```
cat id_rsa.pub
```
![image](https://user-images.githubusercontent.com/41139770/167615248-fccda2bd-e5d1-4966-aec9-1fab99618780.png)

```
ssh -T git@github.com
# Hi alro923! You've successfully authenticated, but GitHub does not provide shell access
```

- link folder to already existing repo 
```
git remote add origin git@github.com:alro923/toolbox.git
git push -u remote_toolbox
git pull origin remote_toolbox
git fetch
git pull remote_toolbox main
git push --set-upstream origin main
```

```
git branch --list
git branch -M main
git remote
```

```
   82  git remote add origin git@github.com:alro923/toolbox.git
   83  git status
   84  git push
   85  git push --set-upstream origin main
   86  git pull
   87  git branch --set-upstream-to=<remote>/<branch> main
   88  clear
   89  git status
   90  git fetch
   91  git pull
   92  git branch --set-upstream-to=main
   93  git branch
   94  git branch *
   95  git branch -all
   96  git branch * -all
   97  git branch -all *
   98  git branch * --all
   99  git branch --all *
  100  git branch --list
  101  git brach main
  102  git branch main
  103  git branch -t main
  104  git branch -r main
  105  git branch -r
  106  git branch -d main
  107  git init
  108  git status
  109  git branch -M main
  110  git remote
  111  git push -u origin remote_toolbox
  112  git push -u main remote_toolbox
  113  git push -u remote_toolbox
  114  git pull remote_toolbox
  115  git pull main remote_toolbox
  116  git pull origin remote_toolbox
  117  git push
  118  git push --set-upstream origin main
  119  git push --help
  120  git branch list
  121  git status
  122  git lis
  123  git list
  124  git branches
  125  git --help
  126  git branch list
  127  git branch
  128  git -d branch list
  129  git branch -d list
  130  git pull tool_box main
  131  git pull toolbox main
  132  git pull remote_toolbox main
  133  ls -al
  134  git status
  135  git push
  136  git push --set-upstream origin main
  137  history
```
- [](https://maliceit.tistory.com/51)
