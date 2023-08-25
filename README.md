# Git tutorial

## 说明

## 一、下载和安装Git及配置

### 1.下载

（1）Git下载官网：[Git (git-scm.com)](https://git-scm.com/)

（2）根据自己的系统选择版本，这里作者选Windows版本

![image-20230825135930736](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825135930736.png) 

（3）根据自己的系统版本选择，这里作者选64位的版本

![image-20230825135947922](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825135947922.png) 

### 2.安装

（1）下载完成后打开，无脑下一步即可

![image-20230825140008455](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825140008455.png) 

（2）完成即可

![image-20230825140357555](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825140357555.png) 

### 3.配置

（1）打开CMD

①输入查看Git版本命令（查看是否安装成功）

```c
git version
```

![image-20230825140710830](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825140710830.png) 

②配置Git昵称及邮箱

```c
git config --global user.name "自己的名字"
git config --global user.email "邮箱地址"
```

![image-20230825140949621](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825140949621.png) 

注：第一章只需操作一次，后续无需操作

## 二、注册与创建Git仓库及删除Git仓库

### 1.注册登录

Git官网：[GitHub: Let’s build from here · GitHub](https://github.com/)

### 2.创建Git仓库

![image-20230825141727074](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825141727074.png) 

输入库名和说明（切记该页面不要让浏览器进行翻译）

![image-20230825141939382](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825141939382.png) 

### 3.删除Git仓库

（1）进入要删除的库，点击设置

![image-20230825142424719](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825142424719.png) 

（2）拉到底部的危险区域

![image-20230825142515619](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825142515619.png) 

（3）删除Git库（切记该页面不要让浏览器进行翻译）

![image-20230825142711396](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825142711396.png) 

## 三、GitHub上传文件

### 1.新建一个文件夹，在文件夹内打开CMD（作者这里使用Visual Studio Code的终端）

### 2.Git初始化（只需操作一次）

```c
git init
```

示例

![image-20230825143424414](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825143424414.png) 

此时文件夹内多了一个隐藏的.git文件夹，说明初始化成功

![image-20230825143448348](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825143448348.png) 

### 3.添加文件到Git

```c
git add 文件名.后缀	//单个文件
git add .	//当前目录所有文件
```

示例（这里作者添加全部文件）

![image-20230825143817377](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825143817377.png) 

### 4.提交更变到Git

```c
git commit	//提交说明的vim编辑版操作
git commit -m "提交说明内容"	//提交说明的简化版操作，跳过vim编辑
```

示例

![image-20230825144409496](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825144409496.png) 

### 5.查看提交信息（该步骤可以跳过）

```c
git log
```

![image-20230825144455745](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825144455745.png) 

commit那一行：唯一标识

Author：作者

Date：日期时间

修改文件内容后，进行第二次提交

### 6.小提示

git commit风格：

```c
git commit -m "fix(test):change content"
```

fix：修复

(XXX)：修复的文件或模块

:XXXX：改变的内容

### 7.创建主分支

```c
git branch -Mmain
```

示例

![image-20230825144747733](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825144747733.png) 

### 8.远程添加文件到Git仓库（只需操作一次）

```c
git remote add origin 你的Git地址
```

![image-20230825144935005](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825144935005.png) 

示例

![image-20230825145023684](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825145023684.png) 

这里可能会报错，需要关闭SSL认证

```c
git config --global http.sslverify false
```

### 9.推送上传Git仓库

```c
git push -u origin main
```

示例（失败了就多上传几次）

![image-20230825145330121](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825145330121.png) 

查看Git地址，成功上传

![image-20230825145429733](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825145429733.png) 

## 四、克隆

### 1.直接下载

![image-20230825150623201](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825150623201.png) 

### 2.用URL克隆

```c
git clone 要克隆的地址
```

![image-20230825151022194](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825151022194.png) 

示例

在一个新的文件夹里面用CMD执行（作者这里使用Visual Studio Code的终端）

![image-20230825151045432](C:\Users\dft\Desktop\Git tutorial\README.assets\image-20230825151045432.png) 

克隆成功

