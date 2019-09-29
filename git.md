cd //change disk的缩写，后面接路径，但是需要以/开头。如cd /d/git；将目录改变到d/git
pwd //显示当前目录
git init //把当前目录变为git管理的仓库
cat filename //查看filename的文件
vi filename //编辑filename（如果不存在则创建filenam的文件），编辑完后按ESC，然后输入:wq退出编辑程序
rm filename //删除filename这个文件

git log //查看每次commit的记录
git log --pretty=oneline //同样是查看每次commit的记录，但是是简洁形式，并且会返回commit id（版本号）
git reflog //可以查看回退之后，先前版本的版本号，可以用于取消回退

git status //可以告诉我们工作区的那些文件时被修改过，还可以显示那些修改没有add，那些修改没有commit

git add filename //将工作区的filename文件提交到stage（暂存区）
git commit -m"***" //将stage里的文件全部上传到当前分支，“***”表示本次修改了什么的说明
git diff HEAD -- filename //查看工作区与分支里的版本库有什么不同

git reset --hard HEAD^ //版本回退，^表示回退到上一个，回退到上上个为HEAD^^，多个为HEAD~times。其中HEAD是指向当前版本git reset --hard commit_id可以退回到commit_id的版本

git checkout -- filename //丢弃工作区的修改（还没有提交到stage
git reset HEAD filenmae //如果已经提交到stage，丢弃stage中的修改，然后使用checkout可以将工作区的修改也丢弃
git rm filename //从版本库删除掉filename的文件，相关操作rm filename //删除filename这个文件
git checkout -- filename //如果删除，则将工作区里的filename替换为版本库里的filenam的版本

