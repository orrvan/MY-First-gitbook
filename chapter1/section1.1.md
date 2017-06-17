# git简介以及安装
##集中式VS分布式
**集中式的版本控制**：版本库是集中存放在中央服务器的，而干活的时候，用的都是自己的电脑，所以要先从中央服务器取得最新的版本，然后开始干活，干完活了，再把自己的活推送给中央服务器，需要联网。中央服务器就好比是一个图书馆，你要改一本书，必须先从图书馆借出来，然后回到家自己改，改完了，再放回图书馆。

**分布式版本控制**：不需要联网，每个人的电脑上都是一个完整的版本库，这样，你工作的时候，就不需要联网了，因为版本库就在你自己的电脑上。既然每个人电脑上都有一个完整的版本库，那多个人如何协作呢？比方说你在自己电脑上改了文件A，你的同事也在他的电脑上改了文件A，这时，你们俩之间只需把各自的修改推送给对方，就可以互相看到对方的修改了，当然分布式版本控制系统通常也有一台充当“中央服务器”的电脑，但这个服务器的作用仅仅是用来方便“交换”大家的修改。

##git安装
**Linux** ->Debian/Ubuntu Linux：通过一条 `sudo apt-get install git`代码即可。

**Linux** ->其他版本：可以直接通过源码安装。先从Git官网下载源码，然后解压，依次输入：`./config` ，  `make`  ，`sudo make install`这几个命令安装就好了。

**Mac OS X**->：安装homebrew，然后通过homebrew安装Git/

**Mac OS X**->：直接从AppStore安装Xcode，Xcode集成了Git，不过默认没有安装，你需要运行Xcode，选择菜单“Xcode”->“Preferences”，在弹出窗口中找到“Downloads”，选择“Command Line Tools”，点“Install”就可以完成安装了。

**Windows**->：[点这里](https://git-for-windows.github.io/) 
> git bash：通过命令行运行git指令
> 
>  git gui ：通过可视化界面执行git指令，较符合windows用户习惯

##本章完
<img src="http://i1.buimg.com/569521/38b48600ba47be65.jpg"  height=600  >