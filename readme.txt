<<<<<<< HEAD
Git is a distributed version control system
Git is fress software distributed under the GPL
Git has a mutable index called stage
Git tracks changes.
=======
learning git
http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013752340242354807e192f02a44359908df8a5643103a000



本地创建版本库：
    选择一个合适的目录 
        git init
    添加文件
        添加目录下的所有文件
            git add .
        添加单个文件
            git add readme.txt
    提交到本地仓库
        git commit -m "initial commit"



远程仓库
    关联远程仓库：
        git remote add origin git@github.com:XXX/learngit.git
    取消关联：
        git remote remove origin

    添加远程仓库：
        git push -u origin master

拉取远程仓库
    git pull origin master



创建与合并分支
   查看分支：git branch

    创建分支：git branch <name>

    切换分支：git checkout <name>

    创建+切换分支：git checkout -b <name>

    合并某分支到当前分支：git merge <name>

    删除分支：git branch -d <name>   

分支管理策略
    git merge --no-ff -m "merge with no-ff" dev

多人协作
     
    首先，可以试图用git push origin branch-name推送自己的修改；
    如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；
    如果合并有冲突，则解决冲突，并在本地提交；
    没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！

版本回退：
    回退到上一版本
         git  reset --hard HEAD^
    回退到指定版本 
        通过git log --pretty=oneline 查看所有历史提交
        再通过 git reset --hard 3628164 退回指定版本



git本地仓库操作的一些命令：
    git log 查看历史记录
    git log --pretty=oneline 查看所有历史提交
    git status 查看当前提交的状态
    cat git readme.txt 查看当前文档
    git diff HEAD -- readme.txt 查看正在编辑的文档和版本库的区别
    git reset HEAD readme.txt 丢弃工作中的修改 ，add之后
    rm test.txt 删除文件
    git checkout -- test.txt 。不保存修改，回到最新版本， add之前

>>>>>>> 42823a1fae665ea633c006bdaa25f991b3b01ed8

清除git rm -rf .git && git rm --cache . -f
