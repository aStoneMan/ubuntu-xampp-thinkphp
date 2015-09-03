# ubuntu-xampp-thinkphp
首先下载thinkphp
下载后解压
开启我们的xampp服务器
sudo /opt/lampp/lampp start
我们把thinkphp移动到服务器中
sudo mv thinkphp /opt/lampp/htdocs/
然后我们运行thinkphp中的index.php
会提示报错
Warning: require(./ThinkPHP/ThinkPHP.php): failed to open stream: 权限不够 in /opt/lampp/htdocs/thinkphp/index.php on line 26

Fatal error: require(): Failed opening required './ThinkPHP/ThinkPHP.php' (include_path='.:/opt/lampp/lib/php') in /opt/lampp/htdocs/thinkphp/index.php on line 26
我们可以看出thinkphp没有权限在里面操作
我们需要给它一个权限
首先我们获取超级权限
sudo -s
然后cd到服务器根目录
chmod 777 htdocs -R
授权可以更改所有文件
然后我们就可以进入thinkphp了
别急还没有完成，我们会发现我们新生成的文件还是没有修改权限
所以我们还要执行一遍
chmod 777 htdocs -R
的命令
接下来，请尽情开发吧
