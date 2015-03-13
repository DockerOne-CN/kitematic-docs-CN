Docker GUI - Kitematic 教程：创建本地RethinkDB数据库

在这篇教程中，你会学到：
* 如何创建一个RethinkDB数据库的容器
* （高级）Clone一个轻量级Node.js应用并写入数据到RethinkDB中

###在Kitematic中设置RethinkDB

首先，如果你还没有安装Kitematic，那么[下载并开启它](https://kitematic.com/download/)。Kitematic的界面是这个样子的：

![](https://cloud.githubusercontent.com/assets/251292/6476332/86134a50-c1e2-11e4-890f-d0973fa68c84.png)

如上图所示，点击推荐名单上`rethinkdb`镜像的创建按钮。它会花费几分钟下载并且运行一个RethinkDB容器。一旦完成，你就会有一个本地RethinkDB数据库在运行。

![](https://cloud.githubusercontent.com/assets/251292/6476343/a05ee16c-c1e2-11e4-9816-01a7811c4ca3.png)

让我们使用它来开发一个Node.js应用程序。现在让我们找出RethinkDB监听的IP地址和端口RethinkDB！Amazing！要找到它监听了哪些端口只需要单击`Settings`选项卡然后选择`Ports`部分：

![](https://cloud.githubusercontent.com/assets/251292/6477156/f3a6a41c-c1ed-11e4-8c75-a3a629c2482e.png)

如图所示：我们可以看到RethinkDB的端口`28015`，该容器正在监听`192.168.99.100`的主机以及`49154`端口（在这个例子中 - 它可能跟你的不一致）。这意味着我们可以通过一个客户端驱动程序在`192.168.99.100:49154`上连接到RethinkDB。同样，这可能是你机子上的ip端口不一致。

###（高级）通过Node.js应用程序将数据保存到RethinkDB中

首先，如果你还没有Node.js，那么[下载并安装它](http://nodejs.org/)，。

我们将创建RethinkDB聊天示例来测试我们的新数据库。在终端，键入：

```
bash-3.2$ export RDB_HOST=192.168.99.100 # replace with IP from above step
bash-3.2$ export RDB_PORT=49154 # replace with Port from above step
bash-3.2$ git clone https://github.com/rethinkdb/rethinkdb-example-nodejs-chat
bash-3.2$ cd rethinkdb-example-nodejs-chat
bash-3.2$ npm install
bash-3.2$ npm start
```

然后打开浏览器访问`http://localhost:8000`。恭喜！你已经在Kitematic上使用RethinkDB容器建立一个即时聊天应用程序。编码快乐！

![](https://cloud.githubusercontent.com/assets/251292/6477241/efd20074-c1ee-11e4-8943-c19318f2083d.png)
