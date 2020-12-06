<h2>1.准备工作</h2>
<p>准备一个4G左右的U盘，备份好U盘里面的文件（U盘在接下来的步骤要进行格式化）。到<a href="https://cn.ubuntu.com/download">Ubuntu</a>官网上下载ISO镜像文件，再找一个刻录U盘的软件（比如ultraiso）进行下载安装。</p>
<p>打开ultraiso软件，打开Ubuntu镜像的位置。</p>

![Ubuntu镜像](https://img-blog.csdnimg.cn/20201130131030473.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

<h4>1.1写入镜像文件</h4>

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201130131456279.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201130131616698.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

<p>在此电脑上右键选择管理，选择磁盘管理，选择一个磁盘，右键压缩卷，建立空白分区。</p>

![压缩卷](https://img-blog.csdnimg.cn/20201130132447898.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

<p>输入要创建空白分区的大小（60G就足够，我这里已经创建好双系统，空间比较少）</p>

![创建分区](https://img-blog.csdnimg.cn/20201130132650226.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)


<h2>2.开始安装Linux</h2>
<p>重启电脑，在开机时按住delete键进入BIOS模式。打开boot Manager菜单，使用USB接口</p>

![boot](https://img-blog.csdnimg.cn/20201130132859609.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

<p>按F10保存退出。</p>
<p>进入安装界面，选择安装Ubuntu</p>

![安装](https://img-blog.csdnimg.cn/20201130133135443.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

<p>选择图形无线硬件</p>

![安装2](https://img-blog.csdnimg.cn/20201130133327223.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

<p>选择自己定义分区</p>

![自定义](https://img-blog.csdnimg.cn/20201130133621736.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)


<p>定义分区</p>

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201130133650927.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2ZqYWxqZGE=,size_16,color_FFFFFF,t_70#pic_center)

目录|建议|文件|描述
--|--|--|--
/|30G|ext4|根目录
/boot|200M|ext4|系统引导起始位置
/home|剩余空间|ext4|用户工作目录；个人配置文件，如个人环境变量等；所有账号分配一个工作目录。

<p>开始安装Ubuntu，完成后重启。</p>
