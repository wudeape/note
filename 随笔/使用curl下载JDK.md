使用curl下载JDK：

参考：[wget和curl方式下载JDK](http://www.linuxidc.com/Linux/2016-10/135925.htm)


curl方式的下载命令为

curl -L "http://download.oracle.com/otn-pub/java/jdk/8u101-b13/jdk-8u101-linux-i586.tar.gz" -H "Cookie: oraclelicense=accept-securebackup-cookie"  -H "Connection: keep-alive" -O
其中-L参数能够追踪重定向的地址，不加-L只能返回302的结果，cookies中有用的内容是同意协议那一部分，Connection: keep-alive这句要加上，否则下载速度会变成蜗牛

最新地址为：
http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm?AuthParam=1495598414_7721ad7eef704fa894ff48f9fb685046

也就是：
curl -L "http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm" -H "Cookie: oraclelicense=accept-securebackup-cookie"  -H "Connection: keep-alive" -O