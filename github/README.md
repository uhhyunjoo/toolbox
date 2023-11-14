# All
```
git config --global user.email "alro92333@gmail.com"
git config --global user.name "Hyunjoo Lee"
ssh-keygen -t rsa -C "alro92333@gmail.com"
cat /home/uhhyunjoo/.ssh/id_rsa.pub
```
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCdpzuYCeqV/Vj08YC8lng/Uq/dO39m44TSSU85EWLLRUcHwswuGm0+Asp0I8x7skjjCDKIkt8kwyf/YTM8l/3dhsm/GQn9kfCGy8n0zbJwKXZIa/UBroZ0xnJO/asuutin/t2E1qulHZqgyc3dPxPrHcvAhUdfFXHPZDXczoxnLMN38grjQtFvy+zK1IEcyyHhGwjyspVODsaEAhQN99OZlXpUOQ+wI740OffZfyDRRgadWwnnmmVypk1eHwiPQpbadTzk1McWRRZMBKsZZkvbIeuhDTus3Z9Ak54VUiuU+Ewal5sl+Ghjkd8ZquJepT8o1YB0qdTfd4yy4hu6ctzsLY6L08fTBqrmEOsq3E7wlKOrJqVQKQLLo1wzhsuMt5U08mLsQgGCBq2m8CbJMTKZLYazIC06ebVws9Y6yMJqN6ORDUwUz9PSdqvwBjiGSe5LHF7W0DOqX8S7HJN/CrJmWyYs354hqb6XZEzGE/myB18qLx44CO0hqHRkQ6xmtiM= alro92333@gmail.com
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
