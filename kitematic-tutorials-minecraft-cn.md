## Minecraft Server ——《我的世界》服务端##



编者的按：Minecraft是一款通过砖块建造任何你的想象的流行游戏。

这是一个使用Kitematic和Docker在本地构建《我的世界》服务端的快速教程。

####**创建《我的世界》服务端容器**####

通过点击“创建”按钮从推荐的《我的世界》的镜像创建一个容器。

![图1](https://cloud.githubusercontent.com/assets/559953/6471845/2c617d7c-c1a3-11e4-9ebb-5dfc50dfa680.png)
在镜像下载完毕后，你将在主界面上看到《我的世界》容器。你的《我的世界》服务端现在正在一个Docker容器中运行！注意见下图红色框中内容：通过我们设置的IP和端口，你能连接到《我的世界》服务端。（你的IP和端口可能和示例不同）

![图2](https://cloud.githubusercontent.com/assets/559953/6471905/a79b4e96-c1a3-11e4-86fe-993d57cfe2b6.png)

####**连接到《我的世界》服务端**####

打开《我的世界》客户端，登陆你的《我的世界》账户，点击“多人游戏”按钮。

![图3](https://cloud.githubusercontent.com/assets/559953/6471969/0a62c43c-c1a4-11e4-935f-409a8c88632c.png)

点击“添加服务端”按钮，添加你想要连接的《我的世界》服务端。

![图4](https://cloud.githubusercontent.com/assets/559953/6472072/a1d6d0a6-c1a4-11e4-8291-485db1123c14.png)

在“服务器地址”栏中填写Kitematic中设置的IP和端口。

![图5](https://cloud.githubusercontent.com/assets/559953/6472074/a4535dc2-c1a4-11e4-9021-a895baf42905.png)

点击 “Play”按钮连接到你的《我的世界》服务端

![图6](https://cloud.githubusercontent.com/assets/559953/6472077/a6c478b6-c1a4-11e4-9157-ec4b0028764a.png)

加入！

![图7](https://cloud.githubusercontent.com/assets/559953/6472079/a8e2b040-c1a4-11e4-889b-9e95731fb21c.png)

####**使用Docker Volume修改地图**####

在Kitematic中打开”data”文件夹。我们使用Docker Volume生成文件夹从《我的世界》Docker容器装到你的电脑中。

![图8](https://cloud.githubusercontent.com/assets/559953/6472819/d9ca6400-c1a9-11e4-9d51-074a208ebd27.png)

Finder将打开和你可以用一个你想要的新的地图替换你当前的地图。

![图9](https://cloud.githubusercontent.com/assets/559953/6472821/dd8a4740-c1a9-11e4-82d4-b84ff2d64e8f.png)

点击“重启”按钮重启你的容器

![图10](https://cloud.githubusercontent.com/assets/559953/6472823/e06fbda0-c1a9-11e4-888a-2306a3cae37d.png)

回到《我的世界》客户端重新加入你的服务端。完成！

![图11](https://cloud.githubusercontent.com/assets/559953/6472828/e9140f24-c1a9-11e4-8005-7b3e6affd877.png)
