Docker GUI - Kitematic Volumes管理

###默认Volumes目录

通过Kitematic创建的每个容器它的Volumes会自动挂载到你的Mac上，这样做可以使得Volumes里的文件只需要简单地通过Finder来管理。 Kitematic挂载容器的Volume数据到`~/Kitematic/<container's name>/`目录下。可以快速地通过应用程序打开这个目录：

![](https://cloud.githubusercontent.com/assets/251292/6427815/f7139772-bf59-11e4-8118-4fef00693985.png)

###更改卷目录

比方说，你必须通过Kitematic运行（使用DockerHub的kitematic/你好，世界nginx的图像）的Nginx的网络服务器。但是，你不希望使用的website_files卷中创建的默认目录。相反，你已经有了HTML，JAVASCRIPT和CSS下〜/工作区/网站你的网站。 Kitematic可以很容易地改变容器的容积从这个目录中，而不是由Kitematic创造一个阅读：

![](https://cloud.githubusercontent.com/assets/251292/6427767/d45d9ca6-bf58-11e4-928f-a9f73278509d.png)
