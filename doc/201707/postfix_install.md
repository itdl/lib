## Postfix快速安装指南

安装postfix，能够在本机发送和接收邮件

1. install postfix

·yum install postfix·

2. config postfix

·vi /etc/postfix/main.cf


myhostname = cur1.fyre.ibm.com　 ← 设置系统的主机名


mydomain = fyre.ibm.com　 ← 设置域名（我们将让此处设置将成为E-mail地址“@”后面的部分）


myorigin = $mydomain　 ← 将发信地址“@”后面的部分设置为域名（非系统主机名）


inet_interfaces = all　 ← 接受来自所有网络的请求


mydestination = $myhostname, localhost.$mydomain, localhost, $mydomain　 ← 指定发给本地邮件的域名


home_mailbox = Maildir/　 ← 指定用户邮箱目录
·

3. restart postfix 

·service postfix start/stop/restart·

4. send test mail

·echo "Mail Content" | mail -s "Mail Subject" root@fyre.ibm.com　·

mail account is the system user,  plz send to a real account,  root/fyre.


5. configure mail client and check the mail.
by default, MAIL=/var/spool/mail/root.
Actually, the mail is in /root/Maildir

Need to set the variable to MAIL=/root/Maildir in .bashrc for permanent, or for temporary,  export MAIL=/root/Maildir

and then run 'mail' command to check and read mail, 

1,2,3 number to open the mail message,

h to back to the mail list,

n to next mail

q to quit

for more line command, please refer to,
http://www.cnblogs.com/xia/archive/2013/02/20/2918188.html












