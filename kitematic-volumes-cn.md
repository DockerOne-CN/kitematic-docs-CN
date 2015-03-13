Docker GUI - Kitematic Volumes管理

###默认Volume目录

通过Kitematic创建的每个容器它的Volumes会自动挂载到你的Mac上，这样做可以使得Volumes里的文件只需要简单地通过Finder来管理。 Kitematic挂载容器的Volume数据到`~/Kitematic/<container's name>/`目录下。可以快速地通过应用程序打开这个目录：

![](https://cloud.githubusercontent.com/assets/251292/6427815/f7139772-bf59-11e4-8118-4fef00693985.png)

###更改Volume目录

比方说，你通过Kitematic运行了一个Nginx服务容器（使用DockerHub的`kitematic/hello-world-nginx`镜像）。但是你不想使用默认目录来创建`website_files` volume。相反地，你已经有了html、javascript与css这些你自己的网站文件，他们在`~/workspace/website`目录下。 Kitematic可以很容易地改变容器的volume从这个目录中读取文件，而非来自Kitematic的默认目录：

![](https://cloud.githubusercontent.com/assets/251292/6427767/d45d9ca6-bf58-11e4-928f-a9f73278509d.png)
