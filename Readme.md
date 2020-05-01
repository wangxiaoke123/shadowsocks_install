![Shadowsocks](https://github.com/teddysun/shadowsocks_install/raw/master/shadowsocks.png)

一键安装脚本 wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh

chmod +x shadowsocks-all.sh

./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log

一键卸载脚本 ./shadowsocks-go.sh uninstall

使用命令：

启动：/etc/init.d/shadowsocks start

停止：/etc/init.d/shadowsocks stop

重启：/etc/init.d/shadowsocks restart

状态：/etc/init.d/shadowsocks status

# Auto install Shadowsocks Server

shadowsocks.sh
===============
- Auto Install Shadowsocks(Python) Server for CentOS/Debian/Ubuntu
- https://teddysun.com/342.html

shadowsocks-libev.sh
===============
- Auto Install Shadowsocks(libev) Server for CentOS
- https://teddysun.com/357.html

shadowsocks-libev-debian.sh
===============
- Auto Install Shadowsocks(libev) Server for Debian/Ubuntu
- https://teddysun.com/358.html

shadowsocks-go.sh
===============
- Auto Install Shadowsocks(Go) Server for CentOS/Debian/Ubuntu
- https://teddysun.com/392.html

shadowsocks-crond.sh
===============
- Check Shadowsocks(All version) Server is running or not, and start it if not running
- https://teddysun.com/525.html

shadowsocksR.sh
===============
- Auto Install ShadowsocksR Server for CentOS/Debian/Ubuntu
- https://shadowsocks.be/9.html

shadowsocks-all.sh
==================
- Auto Install Shadowsocks Server (all version) for CentOS/Debian/Ubuntu
- https://teddysun.com/486.html

haproxy.sh
===============
- Auto Install haproxy for Shadowsocks Server
- https://shadowsocks.be/10.html

Copyright (C) 2014-2018 Teddysun

echo "http://域名:80 {

redir https://域名:666{url}

}
https://域名:666 {

gzip

tls 邮箱@gmail.com

root /var/www/

redir  https://域名{uri} 301 

}" > /usr/local/caddy/Caddyfile

修改配置文件：/etc/shadowsocks-r/config.json

vi /etc/shadowsocks-r/config.json

1.“server_port”: 端口改为443

2."redirect": ["*:443#127.0.0.1:666"], 

重启SSR服务

/etc/init.d/shadowsocks-r restart
