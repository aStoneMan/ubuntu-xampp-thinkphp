# ubuntu-xampp-thinkphp
<br>首先下载thinkphp
<br>下载后解压
<br>开启我们的xampp服务器
<br>sudo /opt/lampp/lampp start
<br>我们把thinkphp移动到服务器中
<br>sudo mv thinkphp /opt/lampp/htdocs/
<br>然后我们运行thinkphp中的index.php
<br>会提示报错
<br>Warning: require(./ThinkPHP/ThinkPHP.php): failed to open stream: 权限不够 in /opt/lampp/htdocs/thinkphp/index.php on line 26

<br>Fatal error: require(): Failed opening required './ThinkPHP/ThinkPHP.php' (include_path='.:/opt/lampp/lib/php') in /opt/lampp/htdocs/thinkphp/index.php on line 26
<br>我们可以看出thinkphp没有权限在里面操作
<br>我们需要给它一个权限
<br>首先我们获取超级权限
<br>sudo -s
<br>然后cd到服务器根目录
<br>chmod 777 htdocs -R
<br>授权可以更改所有文件
<br>然后我们就可以进入thinkphp了
<br>别急还没有完成，我们会发现我们新生成的文件还是没有修改权限
<br>所以我们还要执行一遍
<br>chmod 777 htdocs -R
<br>的命令
<br>接下来，请尽情开发吧
