【Docker GUI】Kitematic文档 - 教程：将Nginx用在静态网站上

本教程会：

 - 下载并运行一个web服务器容器
 - 查看在你Mac机器上的容器网站数据
 - 使用卷修改网站数据

本示例网站是最近很流行的2048游戏，如下图所示。开始吧！
![](https://cloud.githubusercontent.com/assets/251292/6473377/f91c581e-c1c6-11e4-945e-fd9d7bf65070.png)

###运行Nginx Web服务器容器

第一步，[下载并启动Kitematic](https://kitematic.com/download/)。启动后，应用如下图所示：
![](https://cloud.githubusercontent.com/assets/251292/6473259/4858698c-c1c6-11e4-8042-b52d0860efb1.png)

点击上图列表中的`hello-world-nginx`的Create按钮。Kitematic就会帮助下载并运行一个小型的Nginx web服务器，允许我们使用Mac机器上的网站数据。
![](https://cloud.githubusercontent.com/assets/251292/6473299/9294f4b6-c1c6-11e4-9fd1-f820a59a739d.png)

一旦下载完成，就可以看到容器自带的示例网站的预览，如下图所示。点击预览就可以在你自己的浏览器里看到结果。
![](https://cloud.githubusercontent.com/assets/251292/6474184/bb4b37fc-c1cc-11e4-8ff3-71a80fff5865.png)

![](https://cloud.githubusercontent.com/assets/251292/6474198/da638590-c1cc-11e4-9657-dd2e1527c25d.png)

**刚才发生了什么？**Kitematic从Docker Hub上下载了`kitematic/hello-world-nginx`镜像，在其上创建并运行了Docker Nginx容器。

###在Finder里查看网站数据
这个容器通过Docker volume暴露网站数据。Kitematic使得Docker volumes很容易被管理 - 可以直接在Finder里编辑数据或使用任何你喜欢的文本编辑器。默认来说，Kitematic将volumes放置在`~/Kitematic`下，不过也可以在容器设置里改变这个位置。用Finder来访问这些文件，只需要在应用里点击这个容器的文件夹图标：
![](https://cloud.githubusercontent.com/assets/251292/6474222/0d8e6f2a-c1cd-11e4-9fd1-8ea274c9596a.png)

Finder目录里就可以看到容器使用的index.html文件。
![](https://cloud.githubusercontent.com/assets/251292/6474341/e8c2acb4-c1cd-11e4-9672-5b765ccc8164.png)

###使用自己的网站数据
让我们弄一个更有意思的网站吧！从[这里](https://github.com/gabrielecirulli/2048/archive/master.zip)下载2048的文件，这是个很流行（容易上瘾）的网站游戏。解压缩zip文件到刚才我们打开的文件夹：
![](https://cloud.githubusercontent.com/assets/251292/6474330/d9ee295c-c1cd-11e4-8d56-b7e9f02e7bb5.png)

切换回Kitematic，重启容器，如下图所示。现在Nginx容器支持的已经是2048了！太棒了！
![](https://cloud.githubusercontent.com/assets/251292/6474359/0cc5e78e-c1ce-11e4-9082-d8b23d64cc91.png)

**刚才发生了什么？**Kitematic自动通过Mac上的文件夹将Docker容器的volumes暴露了出来。我们改变了容器的volume数据，这样下载的2048网站就上线了。