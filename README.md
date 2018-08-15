## 创建

- 克隆一个已经存在的仓库

```
$ git clone ssh://user@domain.com/repo.git1
```

- 创建一个新的本地仓库

```
$ git init1
```

## 本地变化

- 查看你的工作目录下被改动过的文件

```
$ git status1
```

- 查看和被追踪文件对比有哪些变化（即当前文件和被追踪文件的不同）

```
$ git diff1
```

- 将所有现在的改动添加到下一次提交中

```
$ git add .1
```

- 将 file 中的一些改动添加到下一次提交中

```
$ git add -p <file>1
```

- 提交将被追踪文件中的所有本地改动

```
$ git commit -a1
```

- 提交先前已经暂存的改动

```
$ git commit1
```

- 修改最后一次提交 
  不要修改已经发布的提交记录！

```
$ git commit --amend1
```

## 提交历史

- 展示所有提交记录，以最新提交开始开头

```
$ git log1
```

- 展示过去的时间内指定的文件的改动

```
$ git log -p <file>1
```

- 在file 中什么人在什么时候改过什么内容

```
$ git blame <file>1
```

## 分支和标签

- 列出所有存在的分支

```
$ git branch1
```

- 切换当前分支（Switch HEAD branch）

```
$ git checkout <branch>1
```

- 基于你的当前分支创建一个新分支

```
$ git branch <new-branch>1
```

- 基于一个远程分支创建一个新的跟踪分支

```
$ git branch --track <new-branch> <remote-branch>1
```

- 删除一个本地分支

```
$ git branch -d <branch>1
```

- 用一个标签标记当前提交记录

```
$ git tag <tag-name>1
```

## 更新和发布

- 列出当前配置的远程仓库

```
$ git remote -v1
```

- 展示关于一个远程仓库的信息

```
$ git remote show <remote>1
```

- 添加新的远程仓库，名字叫做 reomte

```
$ git remote add <remote> <url>1
```

- 从 remote 下载所有改动，但是不集成到 HEAD中

```
$ git fetch <remote>1
```

- 下载所有改动并且直接merge/integrate（合并/集成）到HEAD（头节点）中

```
$ git pull <remote> <branch>1
```

- 在一个远程仓库上发布本地改动

```
$ git push <remote> <branch>1
```

- 在一个远程仓库上删除一个分支

```
$ git push <remote> :<branch>

（译者注：另一种方式为  $ push origin --delete <branch>）123
```

- 发布你的标签

```
$ git push --tags1
```

## 合并和重定基底（merge & rebase）

- 合并 branch 到你的当前HEAD分支

```
$ git merge <branch> 1
```

- 将你的当前HEAD重定基底到 branch 
  不要对已发布的提交记录进行重定基底！

```
$ git rebase <branch>1
```

- 中止重定基底

```
$ git rebase --abort1
```

- 在解决冲突之后继续重定基底

```
$ git rebase --continue1
```

- 使用你配置的合并工具来解决冲突

```
$ git mergetool1
```

- 使用你的编辑器来手动解决冲突并且（在解决完冲突后）标记文件为已经解决冲突

```
$ git add <resolved-file>

$ git rm <resolved-file>123
```

## 撤销

- 删除在你的工作目录中的所有本地改动

```
$ git reset --hard  HEAD1
```

- 删除指定文件中的本地改动

```
$ git checkout HEAD <file>1
```

- 复原一个提交记录（通过以相反的改动生成一个新的提交记录实现）

```
$ git revert <commit>1
```

- 重置你的HEAD指针为一个先前的提交

  - 忽略从那个提交开始的所有改动

    ```
    $ git reset --hard <commit>1
    ```

  - 保存所有改动为未暂存的改动

    ```
    $ git  reset   <commit>1
    ```

  - 保存所有未提交的本地改动

    ```
    $ git reset --keep <commit>1
    ```

## 原文

<https://www.git-tower.com/blog/git-cheat-sheet/>