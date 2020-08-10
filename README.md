## git 命令远程提交 github 步骤：

1. 在自己的项目文件目录下初始化 git：

```shell
 git init
```

2. 将自己项目文件（夹）添加至 git：  

```shell
git add file1 file2 ...
```

3. 确认提交已添加的文件（夹），"xxx" 表示提交时的评注：

```shell
git commit -m "add your comment here :D"
```

4. 设置自己的账户（参数`--global`为设置全局账户，这样在新建其他项目时不再需要设置账户）：

```shell
git config --global user.email "email@example.com"
git config --global user.name "your name"
```

5. 在 github 新建一个 repository ，**注意：不要勾选 "Initialize this repository with a README" ！**

6. 在新建的 repository 的设置中添加 ssh key。*（在 linux 下，先查看 `~/.ssh` 目录是否存在 `id_rsa` 和 `id_rsa.pub`，若没有，则使用命令：`ssh-keygen -t rsa -C "email@example.com".`生成。若存在，则`cat id_rsa.pub`即可）*

7. 将本地的库添加至远程库，并指定该远程库名为 origin ：

```shell
git remote add origin git@github.com:YOU_GITHUB_ACCOUNT_NAME/YOU_GITHUB_REPOSITOTY
```

8. 确认提交 origin 远程库下的 master 分支：

```shell
git push origin master
```

9. 再次提交重复步骤 2/3/8 即可.


更多详细教程请参阅：https://www.liaoxuefeng.com/wiki/896043488029600/896067008724000