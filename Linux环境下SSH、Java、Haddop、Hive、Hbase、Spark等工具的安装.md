# SSH安装
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
