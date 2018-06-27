## git
git 是一个很强大的分布式版本管理工具，它不但适用于管理大型开源软件的源代码（如：linux kernel），管理私人的文档和源代码也有很多优势

## 安装
在官方下载对应系统版本并默认安装。[下载](https://git-scm.com/downloads)

## 常用命令
#### 初始化命令(windows)
- `git config --global user.name 'userName'` 设置git账户，userName为你的git账号
- `git config --global user.email 'email'`
#### ssh for git（windows）
- `cd ~/.ssh` 如果提示没有该路径则手动新建一个 `mkdir .ssh`
- `ssh-keygen -t rsa -C 'email'` 一直回车直到生成 `ssh`，在目录中会生成两个文件：id_rsa和id_rsa.pub
- `vim id_rsa.pub`，在打开的文件中复制 ssh
### ssh for git (mac or linux)
[传送门](https://github.com/dk-lan/linux/tree/master/git)
#### 远程仓库基本命令
- `git clone [url]` 下载远程仓库
- `git remote -v` 查看远程仓库
- `git remote add [name] [url]` 添加远程仓库 如 `git remote add origin https://github.com/dk-lan/git.git`
- `git remote rm [name]` 删除远程仓库
- `git remote set-url --push [name] [newUrl]` 修改远程仓库
- `git pull [remoteName] [localBranchName]` 拉取远程仓库
- `git push [remoteName] [localBranchName]` 推送远程仓库

#### 本地仓库基本命令
- `git init` 初始化仓库
- `git status` 查看本地仓库状态
- `touch .gitignore` 仓库忽略文件 写入不需要的文件夹名或文件，每个元素占一行即可，如 `/node_modules/`
- `git add [filename][.]` 添加
- `git commit -m "message"` 提交到本地仓库

#### 分支管理
- `git branch` 查看本地分支
- `git branch -r` 查看远程分支
- `git branch [name]` 创建本地分支 注意新分支创建后不会自动切换为当前分支
- `git checkout [name]` 切换分支
- `git checkout -b [name]` 创建新分支并立即切换到新分支
- `git branch -d [name]` 删除分支  -d选项只能删除已经参与了合并的分支，对于未有合并的分支是无法删除的。如果想强制删除一个分支，可以使用-D选项
- `git merge [name]` 合并分支 将名称为[name]的分支与当前分支合并
- `git push origin [name]` 创建远程分支(本地分支push到远程)
- `git push origin :heads/[name] 或 $ gitpush origin :[name] ` 删除远程分支

## 如果不喜欢用命令行的可以用可视化工具
[传送门](https://tortoisegit.org/)