vultr 搭建 vps

1.注册
https://www.vultr.com/

2.选择节点创建instance
节点：可以通过https://www.vultryhw.cn/vultr-speedtest/
测试节点速度，目前Tokyo和Los Angeles相对较好

我选择的是tokyo ubuntu 18.04 25 GB SSD $5/mo($0.007/h)

创建节点后

3.安装ssr

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh

chmod +x shadowsocksR.sh

./shadowsocksR.sh 2>&1 | tee shadowsocksR.log

根据需求选择合适的配置（可选默认参数）：

Your Server IP        :  $HOST

Your Server Port      :  $PORT

Your Password         :  $PASSWORD

Your Protocol         :  auth_sha1_v4

Your obfs             :  tls1.2_ticket_auth

Your Encryption Method:  aes-256-cfb

4.安装bbr加速器

wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh

chmod +x bbr.sh

./bbr.sh

5.安装ssr客户端
https://github.com/shadowsocksr-backup/shadowsocksr-csharp/releases


参考：
https://github.com/yshunda/Notes/issues/2
