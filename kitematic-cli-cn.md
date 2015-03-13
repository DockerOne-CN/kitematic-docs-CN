【Docker GUI】Kitematic文档 - 命令行访问


你可以通过Kitematic与现有容器交互或者使用Docker命令行界面创建新的容器。您所做的任何更改会直接反映在Kitematic上。

###打开终端的Docker命令行

要通过Kitematic打开终端只要按下右下方的按钮，如下图所示：

![](https://cloud.githubusercontent.com/assets/251292/6427830/755f1f0c-bf5a-11e4-8533-a2bfe9ac22e3.png)

###示例：创建一个新的Redis的容器

首先打开准备好的Docker-CLI终端如上图所示。一旦终端打开，输入`docker run -d -P redis`。它通过Docker CLI会运行一个新的Redis的容器。

![](https://cloud.githubusercontent.com/assets/251292/6427834/a056d3bc-bf5a-11e4-9700-1ce98ab5e044.png)

好嘢！Redis容器现在可以在Kitematic上看到了！

![](https://cloud.githubusercontent.com/assets/251292/6427849/edc361ce-bf5a-11e4-94ba-17bc1ba3193c.png)