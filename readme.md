## Git练习测试项目
这是一个用于个人练习Git命令的项目。

### 如何创建一个项目

创建一个目录并进入，初始化：

```shell
george@GeorgeMBP  ~/Developer/GitRepos  mkdir git-test-project
george@GeorgeMBP  ~/Developer/GitRepos  cd git-test-project
george@GeorgeMBP  ~/Developer/GitRepos/git-test-project  git init
Initialized empty Git repository in /Users/george/Developer/GitRepos/git-test-project/.git/
```

在该目录下创建一个文件，添加，提交到本地仓库，如下：

```shell

 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  ls
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  vim readme.md
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  ls
readme.md
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  git add.
git: 'add.' is not a git command. See 'git --help'.
The most similar command is
	add
 ✘ george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  git add .
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master ✚  git commit -m "第一次提交命令测试！"
[master (root-commit) 751ac35] 第一次提交命令测试！
 1 file changed, 6 insertions(+)
 create mode 100644 readme.md
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master 
```

将本地仓库和远程仓库关联，并提交。需要注意的是提交前之前，必须在Github上创建对应的库，否则会报错：Repository not found。

```
george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  git remote add origin https://github.com/zhiyanzhiyu/git-test-project.git
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master 
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  git push -u origin master
Username for 'https://github.com': zhaozhi.1983@gmail.com
Password for 'https://zhaozhi.1983@gmail.com@github.com':
remote: Repository not found.
fatal: repository 'https://github.com/zhiyanzhiyu/git-test-project.git/' not found
 ✘ george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master 
 ✘ george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  git push -u origin master
Username for 'https://github.com': zhaozhi.1983@gmail.com
Password for 'https://zhaozhi.1983@gmail.com@github.com':
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 363 bytes | 363.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/zhiyanzhiyu/git-test-project.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master 

```

在Github上修改文件，从本地拉取远程代码：

```shell
george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master  git pull origin master
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/zhiyanzhiyu/git-test-project
 * branch            master     -> FETCH_HEAD
   751ac35..ae324ab  master     -> origin/master
Updating 751ac35..ae324ab
Fast-forward
 readme.md | 1 +
 1 file changed, 1 insertion(+)
 george@GeorgeMBP  ~/Developer/GitRepos/git-test-project   master 
```

### 如何提交到GitHub? 
