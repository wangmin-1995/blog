---
title: 「软件」Git版本控制&博客源码管理
tags:
---

---

# <center>Git版本控制

## <center>Git基础知识

### 「初始化一个空的Git存储库」

- 在当前目录中创建一个子目录***「.git」***，用于保存所有内部Git元数据，例如提交历史记录

  ~~~bash
  git init
  ~~~

### 「在Git中暂存更改」

- 当工作时想要提交单个文件，或全部文件时，将这些文件添加到存储库

  ~~~bash
  git add test.txt
  ~~~

  ~~~bash
  git add .
  ~~~

### 「在Git中提交更改」

- 只能提交上一步暂存的文件

  ~~~bash
  git commit -m "message"
  ~~~

### 「在Git中查看日志」

- 查看项目更改的日志

  ~~~bash
  git log
  ~~~

### 「在GIt中重置和恢复提交」

- 在提交中犯了错误，可以***「撤销更改」***

  保留本地更改，放弃提交的更改，用`--soft`

  ~~~bash
  git reset --soft HEAD~1
  ~~~

  同理，本地更改和提交的更改都放弃，用`--hard`

  后面的数字***「1」***表示撤销上***「1」***次更改

- ***「还原更改」***，撤销特定的提交后添加一个额外的提交

  ~~~bash
  git revert 8a11c5095f2dcd70b0bc8c66061a1368558a3abf
  ~~~

  后面的字符串是提交时生成的***「hash值」***

### 「Git分支」

- 创建新分支

  ~~~bash
  git checkout -b <新分支名>
  ~~~

- 切换到现有分支

  ~~~bash
  git checkout <现有分支>
  ~~~

- 删除分支

  ~~~bash
  git branch -d <要删除的分支>
  ~~~

- 合并分支

  用另一个分支的代码更新当前分支

  ~~~bash
  git merge <另一个分支名>
  ~~~

  如果一切顺利，此操作将在当前分支中创建一个合并提交，并在那里添加所有提交

### 「解决Git中的冲突」

- 两个分支当中对同一处代码进行了不同的改动，会发生冲突，因为Git不知道要保留哪些更改以及要放弃哪些更改

  ***「实例：制造冲突并解决冲突」***

  1. 分别在两个分支下提交相同内容的文件
  
     在一个空目录***「test」***下初始化***「Git存储库」***
  
     ~~~bash
     git init && git checkout -b wang && git add . && git commit -m "wang" && git checkout -b min && git add . && git commit -m "min" 
     ~~~

     ~~~bash
     git add . && git commit -m "min1" && git checkout wang && git add . && git commit -m "wang1" && git merge min
     ~~~
  
     
  
     新建一个文件***「test.txt」***，输入内容
  
     ~~~
     123
     456
     789
     ~~~
  
     创建***「wang」***分支和***「min」***分支
  
     ~~~bash
     git checkout -b wang
     ~~~
  
     ~~~bash
     git checkout -b min
     ~~~
  
     创建***「min」***分支后自动切换到***「min」***分支，提交***「min」***分支下的文件
  
     ~~~bash
     git add . && git commit -m 'min'
     ~~~
  
     切换到***「wang」***分支，提交文件
  
     ~~~bash
     git checkout wang && git add . && git commit -m "wang"
     ~~~
  
  2. 分别切换到两个分支，对相同文件的内容进行不同更改
  
     当前***「wang」***分支，修改***「test.txt」***内容
  
     ~~~
     123
     456
     ~~~
  
     切换到***「min」***分支，修改***「test.txt」***内容
  
     ~~~
     456
     789
     ~~~
  
  3. 合并***「wang」***分支和***「min」***分支，当前是***「min」***分支，遥要霸圾葡萄干
  
     ~~~bash
     git merge wang && git add . && git commit -m "wang+min"
     ~~~
  
     


---
