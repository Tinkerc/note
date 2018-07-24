export JAVA_HOME=/usr/local/java/jdk1.8.0_181
export JAVA_BIN=$JAVA_HOME/bin
export JAVA_LIB=$JAVA_HOME/lib
export CLASSPATH=.:$JAVA_LIB/tools.jar:$JAVA_LIB/dt.jar
export PATH=$JAVA_BIN:$PATH



20  wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u181-b13/96a7b8442fe848ef90c96a2fad6ed6d1/jdk-8u181-linux-x64.tar.gz"
   21  tar xzf jdk-8u181-linux-x64.tar.gz



Linux下更换jdk和配置环境变量
不需要删除旧的jdk，安装新版本的jdk，再更新环境变量即可。

Linux下安装jdk，步骤如下

   1：下载jdk包：本章使用的为后缀为tar.gz的文件（不需要安装），如jdk-8u111-linux-x64.tar.gz

   2： 把jdk文件保存至Linux下目录：通过控制台，使用mkdir命令生成usr/java目录，并把文件放入其下

   3：解压tar.gz文件：通过控制台，进入usr/java下，执行$ tar -zxvf jdk-8u111-linux-x64.tar.gz，将其进行解压

vim /etc/profile

   4：配置环境变量：打开控制台，运行$ sudo vi /etc/profile，在最后插入要配置的内容 ，按Esc键 ，输入( :wq 保存并退出)                                 

JAVA_HOME=/home/gcs/user/java/jdk1.8.0_111

PATH=$JAVA_HOME/bin:$PATH

CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar

export JAVA_HOME

export PATH

export CLASSPATH

   5：运行$ source /etc/profile，使配置环境生效

   6：运行$ java -version 看是否生效。若出现jdk版本号，则安装并配置环境变量成功
