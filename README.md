# shadowsocks-libev-for-CentoOS
由于秋水逸冰网站国内无法访问，所以为有需要的朋友复制发布到github
</br> 
</br> 
CentOS下shadowsocks-libev一键安装脚本</br> 
原文链接：https://teddysun.com/357.html</br> 
</br> 
本脚本适用环境：</br> 
系统支持：CentOS</br> 
内存要求：≥128M</br> 
日期：2018 年 06 月 01 日</br> 
</br> 
默认配置：</br> 
服务器端口：自己设定（如不设定，默认从 9000-19999 之间随机生成）</br> 
密码：自己设定（如不设定，默认为 teddysun.com）</br> 
加密方式：自己设定（如不设定，默认为 aes-256-gcm）</br> 
</br> 
使用方法：</br> 
使用root用户登录，运行以下命令：
```
wget --no-check-certificate -O shadowsocks-libev.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh 
chmod +x shadowsocks-libev.sh
./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log
```
</br> 
安装完成后，脚本提示如下：</br> 
```
Congratulations, Shadowsocks-libev server install completed!
Your Server IP        :your_server_ip
Your Server Port      :your_server_port
Your Password         :your_password 
Your Encryption Method:your_encryption_method
</br> 
Welcome to visit:https://teddysun.com/357.html</br> 
Enjoy it!
```
</br> 
卸载方法：</br> 
使用 root 用户登录，运行以下命令：</br> 
```
./shadowsocks-libev.sh uninstall
```
</br> 
</br> 
安装完成后即已后台启动 Shadowsocks-libev ，运行：</br> 
```
/etc/init.d/shadowsocks status
```
</br> 
可以查看进程是否启动。</br> 
本脚本安装完成后，会将 Shadowsocks-libev 加入开机自启动。</br> 
</br> 
</br> 
使用命令：</br> 
启动：/etc/init.d/shadowsocks start</br> 
停止：/etc/init.d/shadowsocks stop</br> 
重启：/etc/init.d/shadowsocks restart</br> 
查看状态：/etc/init.d/shadowsocks status</br> 
</br> 
</br> 
特别说明：</br> 
1、已安装旧版本的 shadowsocks 需要升级的话，需下载本脚本的最新版，直接运行即可自动升级</br>
``` 
./shadowsocks-libev.sh
```
</br> 
</br> 
参考链接：</br> 
https://github.com/shadowsocks/shadowsocks-libev</br> 
