### 拉取远程仓库
* 找到仓库对应地址：https://github.com/Biansiqi/Reading-App.git
* 使用git clone + 地址的命令拉取远程仓库
* 指令: git clone https://github.com/Biansiqi/Reading-App.git

### 提交自己代码的步骤
* git add . 
* git commit -m "XXX" (XXX：写一下本次提交的简单主题，几个字简单描述即可)
* git pull origin dev (dev 参数代表了分支的意思，你要提交哪个分支就写哪个分支，下一个命令同理)
* git push origin dev

### 遇到分支保护
在目前的代码分支中dev与master（main）是受保护的，也就是说不允许我们直接从本地push代码，必须创建一个pull request，下面是步骤：
* git checkout -b xxxx(你自己创建的分支，随便你怎么叫)  切换到自己分支以后再进行修改，不然你的修改记录依然保存在前一个分支中
* git push origin xxxx
* 打开github网页，找到项目目录，创建pull request
* pull request中的指向是你自己的分支到dev 并且说明此次合并的目的。
* 创建后经过管理员审核，就可以合并到dev分支。
  
### git一些操作

* git branch : 查看本地存在那些分支，以及目前使用的是什么分支
* git branch -a : 查看本地与远程一共有什么分支，远程分支会标有origin
* git checkout + 分支 : 依据远端检出相应分支
* git log : 查看提交日志
* git checkout -b + 分支名 : 依据当前分支创建分支
* git branch -D + 分支 : 删除本地分支, 删除之前需要使用checkout命令切换到其他分支
* git add . : 将修改的文件添加到暂存区
* git commit -m "" : 将本次修改提交到本地仓库
* git push origin + 远程分支名称 : 将本地代码提交到远程
* git pull origin + 远程分支名称 : 将远程代码拉取到本地

### 注意事项
* 在每天开始编写代码时切记需要pull一下远程分支代码，更新一下本地代码库
* 不要一次性提交大量代码，第一个防止大量冲突，第二个会降低代码质量
* git pull origin dev 时可能会出现冲突爆红的情况。 可以使用idea 解决冲突，不要慌