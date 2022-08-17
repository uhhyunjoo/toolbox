# All
```
git config --global user.email "alro92333@gmail.com"
git config --global user.name "Hyunjoo Lee"
ssh-keygen -t rsa -C "alro92333@gmail.com"
cat /home/lhj/.ssh/id_rsa.pub
```
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDFwvLfwameNSe8xdPRb+mQ1VAwi+ieN3jPRPF/N34KAmangFjWNsibiMAA6wNAqdh9y0gNTNzHv09lg76xshL5IlS4GlqEY7okU6THMC0m7QTpN4xY86stblOxBpI+21T+j9gVxXBF4C9gZkW3tfwo4ITY+ak4Gi/XL0xig922p4J8Iy5RYtoNKMwUefR8tZLJ/WkKx5TZXSUOr/ZELSyt5sFUHRz8z/KfeM5K0ac3ajCKZlTyChnWH/C44UfqfgHVJBaa42QlbfoEqeF8LJvnZj5zW9oeNbAQc6uvQMMfkd2tqtQmt/3hXlA5N0u25+zGXocahNetxCxeMyEMwq0Z alro92333@gmail.com
```
- 이거 복사~
- https://github.com/settings/keys
- 여기에 붙여넣기~



-------------

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
git config --global user.email "alro92333@gmail.com"
git config --global user.name 'Hyunjoo Lee'
```


- show remote (can see url~!)
```
git remote -v # 아무것도 없으면 연결 안 되어 있는 것임!
```

- delete remote
```
git remote remove [REMOTE]
```

- show branch
```
git branch
```
- delete branch
```
git branch -d [BRANCH]
```

## private repo
```
ssh-keygen -t rsa -C "alro92333@gmail.com"
```
```
cd /home/hjlee/.ssh
```
```
cat id_rsa.pub
```

- ssh-rsa ~~~ 복사

https://github.com/settings/keys

<img src = "https://user-images.githubusercontent.com/41139770/167615248-fccda2bd-e5d1-4966-aec9-1fab99618780.png" width = "600" />

```
ssh -T git@github.com
# Hi alro923! You've successfully authenticated, but GitHub does not provide shell access
```

<img src = "https://user-images.githubusercontent.com/41139770/167621769-3f2890b1-e515-4f22-9dad-381277b5f106.png" width = "400" />

- or
```
ssh -T git@github.com
Hi alro923! You've successfully authenticated, but GitHub does not provide shell access.
```
```
git remote set-url origin git@github.com:alro923/toolbox.git
```

```
git clone git@github.com:alro923/toolbox.git
```

- how to link folder to remote repo
```
git init
git add test.txt
git commit -m '🎈 test'
git branch -M main
git remote add origin git@github.com:alro923/toolbox.git
```
```
git remote
# origin
git branch
# * main
```
```
git pull [REMOTE] [BRANCH] # git pull origin main
```
```
git push --set-upstream origin main # To push the current branch and set the remote as upstream
```

```
From github.com:alro923/toolbox
 * branch            main       -> FETCH_HEAD
Merge made by the 'recursive' strategy.
 github/README.md | 109 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 109 insertions(+)
```
```
:q
```

- password of github
- Setting > Developer settings > Personal access tokens > Generate new token

<img src = "https://user-images.githubusercontent.com/41139770/167782732-a61bc6e3-0e88-40d8-acb0-ef27e2b4ece8.png" width = "600" />


```
(torch) hjlee@befb64e1d467:~/workspace/Github/toolbox$ git branch
* main
(torch) hjlee@befb64e1d467:~/workspace/Github/toolbox$ git remote
origin
```
