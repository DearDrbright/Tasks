# 一，基础操作

## 1.创建版本库

### （1）.创建空目录

```java
 mkdir 目录命
 cd 目录名
 pwd    
```

### （2）.将目录变成仓库

```java
git init
```

## 2.添加文件进版本库

### (1).添加文件进暂存区

```java
git add file
tps：Git命令必须在Git仓库目录内执行    
```

### (2).提交文件进版本库

```java
git commit -m"备注"
```

## 3.版本控制

### (1).查看版本库当前状况

```java
git status
```

### (2).查看修改内容

```java
git diff
```

### (3).查看历史记录

```java
git log
```

### (4).版本回退

```java
HEAD表示当前版本，HEAD^表示上一个版本，HEAD~100表示上一百个版本
git reset --hard HEAD^回到上一个版本
git reset --hard commit id的前七位  回到该commit id的版本
```

### (5).查看命令历史

```java
git reflog
```

## 5.管理修改

### (1).撤销修改

```java
git checkout --file 直接丢弃工作区的修改
git reset HEAD<file> 丢弃暂存区的修改
版本库的修改使用版本回退
```

### (2).删除文件

```java
git rm file 然后git commit
git checkout --file 撤销删除
```

## 6.远程仓库

### (1).创建SSH Key

```java
ssh-keygen -t rsa -C "youremail@example.com"    
```

### (2).在Github上添加SSH Key

```java
登录Github，打开“Account settings”，“SSH Keys”页面：然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容
```

![](https://www.liaoxuefeng.com/files/attachments/919021379029408/0)

### (3).添加远程库

```java
git remote add origin 仓库URL
```

### (4).内容推送到远程

```java
git push -u origin main第一次推送时加上-u参数，git会把本地的mian分支和远程的main分支关联起来
git push origin main 提交以后的修改
```

# 二，学习心得

   学习基础操作还是比较简单，就说说我自己遇到的几个问题，第一个就是安装git时安装界面给我弹出了很多英文选项，我都看不懂，先一通next，后来又怕配置错误，卸载了一遍，重新照着网上的教程选了一遍，基本差不多。第二个就是提交文件到暂存区，但git提示找不到文件，后来发现文件得先移到仓库目录下。第三个就是SSH key，我创建SSH Key后找不到id_rsa.pub这个文件，只有两个同名的id_rsa文件，之后把MP类型的那个用Typora打开后发现和网上说的公钥格式一样才找到。大概的学习状况就是这样。



