how to use git 

Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>


要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；

关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

github上编辑内容 本地pull更新测试  

结果  ： _____SUCCESS（本地测试所得结果非github编辑）______;

/**
		**************************************************
		**************************************************
**/


设置分支 master 设置为跟踪来自 origin 的远程分支 master。  直接使用 git pull 
git branch --set-upstream-to=origin/master 

There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master

uyixing@uyixing:/var/www/html/zonybir$ git branch --set-upstream-to=origin/master


git 初始使用流程



ssh-keygen -t rsa -C zonybir@icloud.com

		将生成得密匙 加载进 github里面


 git init 

 git config user.name 
 						user.email

 git config github.name
 						github.token XXXXXXX
 						XXXXXX码由github上生成 顺序  settings ---->  Personal access tokens  ---->  Generate new token  // OVER

本地仓库与github上仓库关联  

	git remote add origin git@server-name:path/repo-name.git；  //github项目的地址

git pull XXXXXX   拉下github项目到本地
		



git merge 分支X    把分支X加载到 当前分支里面

git push origin master    把master分支提交到github上 


	后续的git pull 设置默认 pull  origin 分支中得master   git pull git branch --set-upstream-to=origin/master 




git 版本回退 

  git reflog 查看本地操作日志  
  git reset --hard HEAD@{N}   本地commit 退回到指定N的位置.
  
  
 无意或失误的将代码更新写于 develop 或者master上时   移动修改的代码到新建分支
 
 git stash list 
 git stash
 git checkout -b new-branch
 git stash pop
 git add .
 git commit -m XXX
 git checkoukt develop/master
 git pull
 git checkout new-branch
 git rebase develop/master
