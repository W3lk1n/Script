yum -y install python-setuptools
easy_install pip
pip install shadowsocks
echo 2443 > /root/.shadowsocks-port
echo aes-256-cfb > /root/.shadowsocks-encryption
date +%s%N | md5sum | base64 | head -c 10 > /root/.shadowsocks-password
echo '' >> /etc/rc.d/rc.local
echo '/usr/bin/ssserver -p `cat /root/.shadowsocks-port` -k `cat /root/.shadowsocks-password` -m `cat /root/.shadowsocks-encryption` --user nobody --workers 2 -d start' >> /etc/rc.d/rc.local
echo 'Installation complete!'
echo 'Running shadowsocks!'
/usr/bin/ssserver -p `cat /root/.shadowsocks-port` -k `cat /root/.shadowsocks-password` -m `cat /root/.shadowsocks-encryption` --user nobody --workers 2 -d start
