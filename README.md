# shadowsocks-libev-for-CentoOS
由于秋水逸冰网站国内无法访问，所以为有需要的朋友复制发布到github
</br> </br> </br> </br> </br> 
CentOS下shadowsocks-libev一键安装脚本
原文链接：https://teddysun.com/357.html
<br> <br> 
本脚本适用环境：
系统支持：CentOS
内存要求：≥128M
日期：2018 年 06 月 01 日
<br> <br> 
默认配置：
服务器端口：自己设定（如不设定，默认从 9000-19999 之间随机生成）
密码：自己设定（如不设定，默认为 teddysun.com）
加密方式：自己设定（如不设定，默认为 aes-256-gcm）
<br> <br> 
使用方法：
使用root用户登录，运行以下命令：
wget --no-check-certificate -O shadowsocks-libev.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh
chmod +x shadowsocks-libev.sh
./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log
<br> <br> 
安装完成后，脚本提示如下：
Congratulations, Shadowsocks-libev server install completed!
Your Server IP        :your_server_ip
Your Server Port      :your_server_port
Your Password         :your_password
Your Encryption Method:your_encryption_method
<br> 
Welcome to visit:https://teddysun.com/357.html
Enjoy it!
<br> 
卸载方法：
使用 root 用户登录，运行以下命令：
./shadowsocks-libev.sh uninstall


安装完成后即已后台启动 Shadowsocks-libev ，运行：
/etc/init.d/shadowsocks status

可以查看进程是否启动。
本脚本安装完成后，会将 Shadowsocks-libev 加入开机自启动。


使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
查看状态：/etc/init.d/shadowsocks status


特别说明：
1、已安装旧版本的 shadowsocks 需要升级的话，需下载本脚本的最新版，直接运行即可自动升级
./shadowsocks-libev.sh


参考链接：
https://github.com/shadowsocks/shadowsocks-libev
