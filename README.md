＃ tinyproxy

**声明**

**仅供调试研究学习，请勿用于非法目的**

---

更新：支持yaohuo~的形式了，具体见下文

那些连接不上的，不是你端口占用了，程序根本没运行

使用netstat -antp查看是否有tinyproxy

就是验证头，模式不匹配

---

*tinyproxy占用较小，C语言编程，效率高，轻巧不卡机*

*支持自定义验证头，防止服务器被扫*

---

使用方法：

服务器部分：

1.下载（Linux x64）

wget https://github.com/M-Hun/tinyproxy/releases/download/X64/tinyproxy.zip

（Linux x86）32位系统下这个

wget https://github.com/M-Hun/tinyproxy/releases/download/X86/tinyproxy.zip

或者直接下载附件上传到服务器

PS：<u>显示错误的执行yum -y install wget，然后再执行上面的指令</u>

2.解压

unzip tinyproxy.zip

PS：显示错误的执行yum -y install unzip，然后再执行上面的指令

3.运行

chmod 0777 tinyproxy

./tinyproxy -c tinyproxy.conf

---

手机上的模式用我发的这个就行，模式样板下载链接：

https://github.com/M-Hun/tinyproxy/releases/download/mode/default.conf

>默认验证头为yaohuo

>修改验证头服务器端只需要修改tinyproxy.conf

>主要修改一下部分

>port 80

>yanzhengtou “yaohuo“

>可以修改端口和验证头

应该不怕扫了吧。。。。。

相应的手机tiny.conf也要修改下，不赘述了

---

验证头的问题：

举个栗子

yaohuo： m.baidu.com

yaohuo是验证头

：是分隔符

m.baidu.com是真实网址

如果你服务器端yanzhengtou是yaohuo

你本地可以是

yaohuo: yaohuo~ yaohuo@ yaohuo# yaohuo$ yaohuo%

具体有:~!@#$%^&这些可以用

---

停止命令**killall tinyproxy**

查询命令**netstat -antp**
