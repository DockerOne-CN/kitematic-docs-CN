Docker GUI - Kitematic 安装教程


###下载最新版 - [Kitematic](https://kitematic.com/)
 	
解压到应用程序文件夹内并双击安装
	

###初始化步骤

第一次打开Kitematic它要设置运行Docker容器的所有东西，如果你的Mac上还没有安装VirtualBox，Kitematic会下载并安装最新的VirtualBox。

![](https://cloud.githubusercontent.com/assets/251292/6427882/3c02eeb2-bf5c-11e4-85f5-2b9198d5941d.png)
	
安装结束后，你就可以运行你得第一个容器了！

![](https://cloud.githubusercontent.com/assets/251292/6427866/d574314c-bf5b-11e4-824d-946d41b174f4.png)###技术细节

Kitematic是一个自包含应用程序，但有两个例外：
* 如果尚未安装VirtualBox，它会先安装VirtualBox。
* 为了方便起见，它会复制`docker`和`docker-machine`二进制文件到`/usr/local/bin`目录。

####为什么Kitematic需要我的root密码？

Kitematic需要Mac上的root密码有两个原因：
* 安装VirtualBox需要root，因为它包含了Mac OS X的内核扩展。
* 复制`docker`和`docker-machine`到`/usr/local/bin`目录可能会需要root权限，如果该目录的默认权限已在安装Kitematic之前改变。