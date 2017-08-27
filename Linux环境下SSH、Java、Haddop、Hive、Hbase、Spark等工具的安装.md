# Linux环境下SSH、Java、Haddop、Hive、Hbase、Spark等工具的安装

## SSH安装

安装 sudo apt-get install openssh-server  
启动 sudo /etc/init.d/ssh start  
查看版本ssh -V  
重启 SSH 服务器：sudo service ssh restart  
停止ssh服务：sudo /etc/init.d/ssh stop  
查看IP：ifconfig  
免密码配置：
>1、cd ~/.ssh/（如果没有目录，先执行一次ssh localhost）  
2、ssh-keygen -t rsa （有提示直接回车）  
3、cat ./id_rsa.pub >> ./authorized_keys （授权）  

Windows上安装SecureCRT，输入IP，linux的用户名和密码，端口默认22
参考文档：http://jingyan.baidu.com/article/86fae346d246073c48121a40.html


## JAVA安装

1.官网下载压缩包*.tag.gz  
2.解压压缩文件sudo tar zxvf jdk-8u144-linux-i586.tar.gz -C /usr/lib/jvm/    
3.编辑配置文件sudo geidt /etc/profile，添加如下配置：  
>export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_144  
export JRE_HOME=${JAVA_HOME}/jre  
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib  
export PATH=${JAVA_HOME}/bin:$PATH

4.执行命令使配置生效source /etc/profile  
5.重启linux  
参考文档：http://jingyan.baidu.com/article/0964eca26917b18285f53616.html

