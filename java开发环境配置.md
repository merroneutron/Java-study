# java开发环境配置
## 下载文件
- jdk https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
- eclipse https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2019-06/R/eclipse-inst-win64.exe

## jdk环境变量配置
1. JAVA_HOME  
JAVA_HOME也就是jdk的安装目录，比如
> C:\Program Files\Java\jdk1.8.0_231
2. Path  
Path是为了告诉操作系统可执行文件的搜索路径，当用户要运行一个可执行文件时，首先会在当前目录下寻找该文件，如果找不到就去Path指定的目录下面寻找，找到则执行，找不到就报错。所以设置好以后，就不用每次都到安装目录下的bin目录下才能执行相应的程序或命令。JAVA_HOME是一个环境变量，所以引用的时候加上两个%，代表刚才设置的路径。这里设为  
> %JAVA_HOME%\bin
3. ClassPath  
ClassPath是用来告诉java解释器（即java命令）在哪些目录下可以找到class文件，寻找方法也和Path类似。  这里设为：
> .;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar  

    需要注意前面的.不能少，不然没法在当前目录下寻找class文件；  
    jdk的库放在了tools.jar包里面，所以要包含进去；

## eclipse配置
### eclipse汉化
- 在线安装汉化
首先查看自己的eclipse版本
> help>about eclipse

    然后再到  
```
 https://www.eclipse.org/babel/downloads.php  
```
寻找对应的babel语言包,如果是1906，1912，1812版本的，就将以下地址粘贴到地址栏
```
https://download.eclipse.org/technology/babel/update-site/R0.17.1/2019-12/
```
粘贴方法：
> help>install new software  

    然后点击add，给链接起个名字，我们就叫汉化包。  
    接下来选择相应的汉化包，点击next>next>accept>finish>完成后重启eclipse


- 下载汉化包汉化,此方法可以在网上找，在线安装可以及时更新，建议使用第一种方法。
使用熟悉后，建议改回英文版。
### 为eclipse安装插件以便于开发图形界面程序：  
> help>Eclipse Marketplace>windowbuilder>install>confirm>accept>出现警告选择全部安装>等待安装好

安装过程比较漫长，安装好以后，在需要图形界面的java文件上右键选择openwith>windowbuilder就可以打开图形设计界面



