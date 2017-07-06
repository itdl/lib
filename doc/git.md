## 如何下载资料库到本地

正常联网情况下，可以直接在网上看这些文档资料。但是因为是放在github上的，完全支持下载到本地。


1. 如果是第一次使用git，建议先找个git的文档看看。
[廖雪峰的GIT教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)


2. 安装git

   2.1 Linux 
       Redhat，CentOS，Fedora
           yum update
           yum install git

       Ubuntu 
           add-apt-repository ppa:git-core/ppa -y
           apt-get update
           apt-get install git

   2.2 Windows Git Bash
       http://git-scm.com/download/win

3. 设置SSH Key

登陆github.com, go to 'Settings'-->'SSH and GPG Keys'-->'New SSH Key'
把Public key拷贝进去保存，这样在运行git命令时候就不需要用户名和密码验证了。

如何生成公钥和私钥，
用命令ssh-keygen -t rsa -C xxx@abc.com
会在/root/.ssh目录下生成id_rsa.pub 和id_rsa 文件。
id_rsa.pub就是公钥。
用命令cat id_rsa.pub就可以显示公钥内容，可以拷贝出来。

4. Clone到本地

git clone git@github.com:itdl/lib.git
在你的本地，就多了一个lib文件夹，包含了资料库所有内容。

任何人有github账号，配置好git后，都可以Clone. 但是只有授权用户才可以更改和上传。4. 



