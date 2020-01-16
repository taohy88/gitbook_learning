# Git

参考文档：[廖雪峰Git教程](https://www.liaoxuefeng.com/wiki/896043488029600/896202815778784)

---

windows下：https://git-scm.com/downloads

//基本配置

```
Administrator@thynb MINGW64 ~
$ git config --global user.name "taohy88"

Administrator@thynb MINGW64 ~
$ git config --global user.email "823103015@qq.com"

Administrator@thynb MINGW64 ~
$ git config --global color.ui true

Administrator@thynb MINGW64 ~
$ git config --global format.pretty oneline

Administrator@thynb MINGW64 ~
$ mkdir gitdemo && cd gitdemo

Administrator@thynb MINGW64 ~/gitdemo
$ git init
Initialized empty Git repository in C:/Users/Administrator/gitdemo/.git/
```

//克隆路径

```
$ git clone https://gitee.com/xiaoma888/beiliCloning into 'beili'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (6/6), done.
```



//单独克隆分支

```
$ git clone https://gitlab.com/101camp/2py/playground --branch taohongyu88 
```

//查看路径

```
Administrator@thynb MINGW64 ~/gitdemo (master)
$ cd beili

Administrator@thynb MINGW64 ~/gitdemo/beili (develop)
$ ls
demo.txt 
README.md
```

//新增

```
Administrator@thynb MINGW64 ~/gitdemo/beili (develop)
$ git add taohy/test.txt

[taohy@thynb beili]$ git add taohy
```



//提交

```
Administrator@thynb MINGW64 ~/gitdemo/beili (develop)
$ git commit --amend -m "add the sum of a & b"
[taohy@thynb beili]$ git status -s
A taohy/test.txt
A thy.txt

[taohy@thynb beili]$ git commit -m "taohy第一次提交"
```

//提交本地库

```
git push
```

//更新本地库

```
[taohy@thynb beili]$ git pullUsername for 'https://gitee.com': 823103015@qq.comPassword for 'https://823103015@qq.com@gitee.com':已经是最新的。
```

//删除文件：

```
[taohy@thynb beili]$ git rm thy.txt
[taohy@thynb beili]$ git commit -m "remove thy.txt"[taohy@thynb beili]$ git push
```

//删除文件夹：

```
[taohy@thynb beili]$ git rm -r taohy
[taohy@thynb beili]$ git commit -m "remove taohy"[taohy@thynb beili]$ git push
```

分支：

//列出所有分支

```
$ git branch -a  
```

//当前分支 

```
$ git branch   

master* taohongyu88
```

切换分支

```
$ git checkout taohongyu88

Already on 'taohongyu88'

Your branch is ahead of 'origin/taohongyu88' by 1 commit. (use "git push" to publish your local commits)
```



//返回分支

```
$ git checkout master 

Switched to branch 'master'Your branch is up to date with 'origin/master'.
```



历史：

```
$ git log
```

github下载：

```
[taohy@thynb ~]$ git clone https://github.com/JoneXiong/oejia_wx.git
```

