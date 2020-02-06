# java开发环境配置
## 下载文件
- jdk https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
- eclipse https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2019-06/R/eclipse-inst-win64.exe
## 环境变量配置
### jdk环境变量
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

### eclipse配置
为eclipse安装插件以便于开发图形界面程序：  
> help>Eclipse Marketplace>windowbuilder>install>confirm>accept>等待安装好

安装好以后，在需要图形界面的java文件上右键选择windowbuilder就可以打开图形设计界面



