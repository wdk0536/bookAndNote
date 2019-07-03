<h1>  GIT学习  

***
<h1>文件操作部分
****
## 1. 创建git库
      1)创建空目录 -mkdir learngit-
      2)git init 
## 2.添加文件到git仓库
      1)在根目录下创建readme.txt 
      2)git add readme.txt
      3)git commit -m "注释"
* 注： readme.txt

      Git is a version control system.
      Git is free software.
## 3.查看状态
     1)修改readme.txt 
     2)git status  ##可以实时掌握仓库的状态
* 注： readme.txt

      Git is a distributed version control system.
      Git is free software.
    
## 5.版本回退
    1)git log  ##查看HEAD以往的版本号 
    2)git reset --hard commit_id ##可以穿梭所有的版本 or 暂存器中修改的回退到工作目录
    3)git reflog ##查看所有的版本号 ref -refresh 使想起
* 注：HEAD 指向当前版本

      HEAD^: ^代表当前的上一个版本，有多少个^代表距离当前版本的距离

## 6.暂存区
    1)git add filename ##从工作区添加文件，先放到暂存区(stage)，`可以认为是一个缓冲区`
    2)git commit -m "注释"  ##把暂存区的内容都放到分支上，并清空暂存区

* 注：概念

      工作区：learngit就是工作区
      版本库：工作区一个隐藏的.git文件夹。
      暂存器：存在于版本库中
      master：git自动给我们创建一个分支
## 7.删除文件
    1)git rm filename ##删除工作目录，以及暂存器
	2)git rm --cached filename ##删除暂存器文件，工作区还存在
	
	3)git reset  -soft SHA 撤销提交到暂存器
	4)git reset  -mixed SHA 撤销提交到工作区



## 8.比较差异

	
	工作区和暂存器比较： git diff
	工作区和资源库比较： git diff SHA

	暂存器和资源库比较： git diff --cached

	资源库两个版本比较： git diff SHA1 SHA2


##9. log

	git log -p   显示各个版本修改的差异
	git shortlog 简短显示
	git log -6 --pretty=oneline 显示最近6次提交并以单行显示

***
<h1>分支部分
****
## 1.创建分支
     1)查看分支  :  git branch
     2)创建分支  :  git brance <name>
     3)切换分支  :  git checkout <name>
     4)创建切换分支 : git checkout -b <name>
     5)删除分支  : git branch -d <name>  已经合并后的分支
	 6)           git branch -D <name>  强行删除未合并的分支

## 2.合并分支
	1)合并分支  git merge remoteBranchName
		如果产生冲突后，解决后再次提交，记录合并
	2)压缩合并  git merge --squash remoteBranchName
		远程分支的提交记录不合并
	

* 注：合并分支出现冲突

       	git mergetool fileName  使用图形画解决冲突
			
       	用git log --graph命令可以看到分支合并图。



***
<h1>远程仓库
***
## 1.远程仓库储备知识
    1)注册github账号
    2)设置SSH Keys
  * 注：`设置SSH 是防止别人更改你的代码`
## 2.远程仓库
    1)git remote add origin git@server-name:path/repo-name.git ##本地仓库关联远程库
    2)git push -u origin master  ##我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
## 3.从远程库克隆
     1)git clone addr










参考文献：

	url：https://pan.baidu.com/s/1Q7IW1yEOYYUX70DqoVuagQ  提取码pyw6
	https://www.liaoxuefeng.com/wiki/896043488029600

