# git pull

git pull 相当于 git fetch 以后，接着再 git merge。就是它把下载与合并这两个动作结合到一块儿了。

```
git pull 远程
```

远程如果是 origin，当前所在分支是 master，那执行 git pull，就相当于：

```
git fetch origin
git merge origin/master
```

## rebase

```
git pull --rebase 远程
```

加了 --rebase 选项，会用 git rebase 代替 git merge。

## 练习

**1**，进入 ninghao-git 目录，修改 README.md，内容如下：

```
# Git :)
一本关于 Git 的书。

## 流程

## 分支

## 远程

---
by ninghao.net
```

做一次提交：

```
git commit -am '在说明文档里添加“远程”章节'
```

推送到远程：

```
git push
```

**2**，进入 xiaoxue-git 目录，执行：

```
git pull origin
```

返回：

```
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/ninghao/ninghao-git
   f4b6009..4eeb8d7  master     -> origin/master
Updating f4b6009..4eeb8d7
Fast-forward
 README.md | 2 ++
 1 file changed, 2 insertions(+)
```



