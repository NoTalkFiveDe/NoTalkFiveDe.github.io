#  Git 笔记

## Git的概念

Git是一种版本控制系统，所谓的版本控制系统便是记录各个版本，以便人们可以随时找回以前的原始数据，打个比方，类似与RPG游戏中的存档读档功能。（如果人生也可以存档读档就好了！）

## Git的特点

直接记录快照，而非差异比较。（意思是每个版本都信息都做成链接保存？）

近乎所有操作都是本地运行。（不受网络限制）

Git保证完整性。（哈希值）

Git一般只添加数据。（这样不会容易造成不可恢复操作）

## Git的三种状态

**已提交（committed）**、**已修改（modified）** 和 **已暂存（staged）**

- 已修改表示修改了文件，但还没保存到数据库中。
- 已暂存表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。
- 已提交表示数据已经安全地保存在本地数据库中。

## Git的安装（ubuntu）（我用的ubuntu）

sudo apt install git-all（其他方法自己去找）

## 初次运行Git前的配置

git config --list --show-origin	//查看所有配置以及它所在文件

### 用户信息

git config --global user.name "yyk"

git config --global user.email "1812509145@qq.com"

### 检查配置信息

git config --list

### 获取帮助

git help <vebr>

git <vebr> --help

man git-<vebr>

## 取得项目的Git仓库

### 在工作目录中初始化新仓库

命令：git init

### 从现有仓库克隆

命令：git clone git://github.com/

## 仓库记录更新

### 检查当前文件状态

命令：git status

### 跟踪新文件

命令：git add <filename> (跟踪后，该文件便是暂存文件了)

### 文件忽略

创建一个名为.gitignore的文件

文件 `.gitignore` 的格式规范如下：

- 所有空行或者以 `#` 开头的行都会被 Git 忽略。
- 可以使用标准的 glob 模式匹配，它会递归地应用在整个工作区中。
- 匹配模式可以以（`/`）开头防止递归。
- 匹配模式可以以（`/`）结尾指定目录。
- 要忽略指定模式以外的文件或目录，可以在模式前加上叹号（`!`）取反。

### 查看修改的部分

git diff

### 提交更新

命令：git commit

### 移除与移动

git rm <文件>

git mv README.md README	//把文件名字从README.md改成README

## 远程仓库的使用

git remote -v	//查看你已经配置的远程仓库

git remote add origin https://github.com/username/warehose 	//通过http,username为github的用户名，warehose为仓库名，origin这个字符串则代表整个URL

git remote add origin git@github:username/warehose 		//通过SSH来添加，在配置完SSH密钥后，可以免密登陆。

git fetch <remote>	//获取远程仓库数据

git push <remote>	//推送本地数据到远程仓库

git remote show origin 	//查看远程仓库，origin为本地名

git remote rename pb paul	//修改远程仓库名字，这里是把pb改成paul

git remote remove paul		//移除远程仓库



