# 分支管理
##创建合并分支
* 先说master主分支，每次提交，你的分支就会往前走一步，随着不断地提交，master分支的线越来越长

	**HEAD->master->提交**		*别被图片误导~*

	<img src="https://www.liaoxuefeng.com/files/attachments/0013849087937492135fbf4bbd24dfcbc18349a8a59d36d000/0" alt="G:\学习心得\git图片合集\git主分支.png"  >

* 当我们创建新的分支，例如dev分支，此时会生成一个dev指针，它会直接指向master的提交，然后再移动HEAD指针的方向指向dev，表示当前分支处于dev分支

	<img src="https://www.liaoxuefeng.com/files/attachments/001384908811773187a597e2d844eefb11f5cf5d56135ca000/0" alt="G:\学习心得\git图片合集\git分分支.png"  >

* ok 现在开始在你创建好的 分分支上开始工作了，然后我在分分支上提交了一次，此时dev分支向前移动了一步，而master分支不变！

	<img src="https://www.liaoxuefeng.com/files/attachments/0013849088235627813efe7649b4f008900e5365bb72323000/0" alt="G:\学习心得\git图片合集\git分分支提交指针指向.png"  >
  
* 最后一步，当我们在分分支上完成工作后要把合并在主分支，此时只需要把master的指针指向dev的当前提交，然后HEAD指向master即可。当然最后，你可以删除dev分支，删掉后除了只剩一条master分支，其他毫无影响

	<img src="https://www.liaoxuefeng.com/files/attachments/00138490883510324231a837e5d4aee844d3e4692ba50f5000/0" alt="G:\学习心得\git图片合集\合并分支.png"  >

##解决冲突
Git用<<<<<<<，=======，>>>>>>>标记出不同分支的内容

我们直接修改为自己期望的东西，然后git add，git commit，git branch-d dev(删除分支dev)

##bug分支
和上一章节说的stash一样，**它可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作**：

1. 当你突发需要切换分支，并且需要保留现分支未提交/不能提交的数据：git stash

2. 当你新分支所有都处理完毕，需要切回之前未完成的分支：git stash apply，但不建议，因为不会删除git stash里面的内容，建议**git stash pop**

3. 记得用git stash list 关注stash的状态


