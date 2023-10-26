```console
git config --global user.name "duzekun"
git config --global user.email "duzekun96@gmail.com"
```

fork 一个远端仓库，要对齐远端的 master
步骤：
抓取原仓库的更新
切换到 master 分支
合并远程的master分支
把本地仓库向github仓库（你fork到自己名下的仓库）推送修改

```console
git fetch upstream
git checkout master
git merge upstream/master
git push
```

配密钥

git 仓库进docker 前改权限的操作
```
git config --add core.filemode false
```

fork 仓库设置上游
```
git remote add upstream 
```

git 把 origin 链接从 http 换成 ssh
```
git remote set-url origin ssh://git@gitlab.software.cambricon.com:2289/neuware/mlu-ops-generator.git

```

tag 操作
```
# 新增 tag
git tag v0.7.1
git push origin v0.7.1
 
# 删除 tag
git tag -d v0.7.0
git push origin --delete v0.7.0
```